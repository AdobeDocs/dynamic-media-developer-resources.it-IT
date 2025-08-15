---
title: Localizzazione stringa di testo
description: La localizzazione delle stringhe di testo consente ai cataloghi di immagini di contenere più rappresentazioni specifiche per le impostazioni internazionali per lo stesso valore di stringa.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: f105c7f2-b544-4c08-bb91-4916e485572d
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '644'
ht-degree: 0%

---

# Localizzazione stringa di testo{#text-string-localization}

La localizzazione delle stringhe di testo consente ai cataloghi di immagini di contenere più rappresentazioni specifiche per le impostazioni internazionali per lo stesso valore di stringa.

Il server restituisce al client la rappresentazione corrispondente alla lingua specificata con `locale=`, evitando la localizzazione lato client e consentendo alle applicazioni di cambiare lingua semplicemente inviando il valore `locale=` appropriato con le richieste di testo IS.

## Ambito {#section-a03f48e3bc0e4ab281909a2bd441a3c2}

La localizzazione delle stringhe di testo viene applicata a tutti gli elementi stringa che includono il token di localizzazione ` ^loc= *`locId`*^` nei seguenti campi catalogo:

<table id="table_83344EFCB5B5418184E0A0B43D0B23F7"> 
 <thead> 
  <tr> 
   <th class="entry"> <b>Campo catalogo</b> </th> 
   <th class="entry"> <b>Elemento stringa nel campo</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p> Catalogo <span class="codeph">::Set di immagini </span> </p> </td> 
   <td> <p>Qualsiasi sottoelemento contenente una stringa traducibile (delimitata da qualsiasi combinazione di separatori ',' ';' ':' e/o l'inizio/la fine del campo). </p> <p> Un valore di colore <span class="codeph"> 0xrggbb </span> all'inizio di un campo localizzabile è escluso dalla localizzazione e trasmesso senza modifiche. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalogo::Mappa </span> </p> </td> 
   <td> <p>Qualsiasi valore di attributo racchiuso tra virgolette singole o doppie, ad eccezione dei valori degli attributi <span class="codeph"> coords= </span> e <span class="codeph"> shape= </span>. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalogo::Destinazioni </span> </p> </td> 
   <td> <p>Il valore di qualsiasi destinazione <span class="codeph">.*.label </span> e destinazione <span class="codeph">.*.userdata </span>, proprietà. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> Catalogo <span class="codeph">::Dati utente </span> </p> </td> 
   <td> <p>Il valore di qualsiasi proprietà. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Sintassi stringa {#section-d12320edf300409f8e17565b143acafc}

Gli elementi *`string`* abilitati per la localizzazione nel catalogo immagini sono costituiti da una o più stringhe localizzate, ciascuna preceduta da un token di localizzazione.

<table id="simpletable_CEFDAE8395E6493E902D58A7E5A25BC7"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> elemento stringa </span> </span> </p> </td> 
  <td class="stentry"> <p>[ <span class="varname"> defaultString </span>]*{ <span class="varname"> localizationToken </span> <span class="varname"> localizedString </span>} </p> </td> 
 </tr> 
</table>

<table id="simpletable_0A687FA72C4C4C1AAFFCB43143C1AB3B"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> localizationToken </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> ^loc= <span class="varname"> locStr </span> ^ </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> locId </span> </span> </p> </td> 
  <td class="stentry"> <p>ID delle impostazioni locali interno per <span class="varname"> localizedString </span> dopo questo <span class="varname"> localizationToken </span>. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> stringa localizzata </span> </span> </p> </td> 
  <td class="stentry"> <p>Stringa localizzata. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> defaultString </span> </span> </p> </td> 
  <td class="stentry"> <p>Stringa da utilizzare per le lingue sconosciute. </p> </td> 
 </tr> 
</table>

*`locId`* deve essere ASCII e non può includere &#39;^&#39;.

&#39;^&#39; può verificarsi ovunque nelle sottostringhe con o senza codifica HTTP. Il server corrisponde all&#39;intero pattern *`localizationToken`* di `^loc=locId^` a sottostringhe separate.

*`stringElements`*, che non includono almeno un *`localizationToken`*, non sono considerati per la localizzazione.

## La mappa di traduzione {#section-f7ce3df91b724adf95cee44eac4915d4}

`attribute::LocaleStrMap` definisce le regole utilizzate dal server per determinare quali *`localizedStrings`* restituire al client. È costituito da un elenco di input *`locales`* (corrispondente ai valori specificati con `locale=`), ciascuno con uno o più ID delle impostazioni locali interni ( *`locId`*). Ad esempio:

`attribute::LocaleStrMap= en,E|nl,N|de,D|,`

I valori *`locId`* vuoti indicano che *`defaultString`* deve essere restituito, se disponibile.

Per ulteriori informazioni, vedere la descrizione di `attribute::LocaleStrMap`.

## Il processo di traduzione {#section-a2a8a3e5850f4f7c9d2318267afe98a2}

Dato l&#39;esempio di mappa di traduzione riportato sopra e la richiesta `/is/image/myCat/myItem?req=&locale=nl`, il server cerca prima &quot; `nl`&quot; nella mappa delle impostazioni internazionali. La voce corrispondente `nl,N` indica che per ogni *`stringElement`*, devono essere restituiti i *`localizedString`* contrassegnati con `^loc=N^`. Se *`localizationToken`* non è presente in *`stringElement`*, viene restituito un valore vuoto.

Supponiamo che `catalog::UserData` per `myCat/myItem` contenga le seguenti (interruzioni di riga inserite per maggiore chiarezza):

`val1=111?? str1=Default1^loc=N^Dutch1^loc=D^German1?? val2=value2?? str2=^loc=E^English2^loc=N^Dutch2^loc=D^German2?? str3=Default3^loc=N^Dutch3^loc=D^German3`

Il server restituisce quanto segue in risposta alla richiesta di esempio:

`val1=111 str1=Dutch1 val2=value2 str2=Dutch2 str3=Dutch3`

## Impostazioni internazionali sconosciute {#section-26dfeefbd60345de94bbfeaaf7741223}

Nell&#39;esempio precedente, `attribute::LocaleStrMap` ha una voce con un valore *`locale`* vuoto. Il server utilizza questa voce per gestire tutti i valori `locale=` che non sono esplicitamente specificati altrimenti nella mappa di traduzione.

L&#39;esempio di mappa di traduzione specifica che in questo caso deve essere restituito *`defaultString`*, se disponibile. Pertanto, se questa mappa di traduzione viene applicata alla richiesta `/is/image/myCat/myItem?req=&locale=ja`, viene restituito quanto segue:

`val1=111 str1=Default1 val2=value2 str2= str3=Default3`

## Esempi {#section-ae6ff7fb90754b839f04ed08aadffa3f}

**Famiglie di lingue**

È possibile associare più valori *`locId`* a ogni *`locale`* nella mappa di traduzione. Il motivo è che consente il supporto di varianti specifiche per paese o per regione (ad esempio, inglese US rispetto all&#39;inglese UK) per selezionare *`stringElements`*, gestendo la maggior parte dei contenuti con impostazioni locali di base comuni (ad esempio, inglese International).

Ad esempio, è stato aggiunto il supporto per l&#39;inglese specifico per gli Stati Uniti ( `*`locId`* EUS`) e per l&#39;inglese specifico per il Regno Unito ( `*`locId`* EUK`), per supportare l&#39;ortografia alternativa occasionale. Se EUK o EUS non esiste, viene restituito a E. Analogamente, le varianti tedesche specifiche per l&#39;Austria ( `DAT`) potrebbero essere rese disponibili dove necessario, restituendo il tedesco comune *`localizedStrings`* (contrassegnato con `D`) la maggior parte delle volte.

`attribute::LocaleStrMap` sarà simile al seguente:

`en,E|en_us,EUS,E|en_uk,EUK,E|de,D|de_at,DAT,D|de_de,D`

La tabella seguente descrive l&#39;output per alcune combinazioni rappresentative *`stringElement`* e *`locale`*:

<table id="table_A6B67587C5F44B5E9CD0E7ED29A81198"> 
 <thead> 
  <tr> 
   <th class="entry"> <i>elementoStringa</i> </th> 
   <th class="entry"> <i>impostazioni locali</i> </th> 
   <th class="entry"> <p>Stringa di output </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> ^loc=E^Inglese^loc=D^Tedesco </span> </p> </td> 
   <td> <p> en, en_us, en_uk </p> <p> de, de_at, de_de </p> <p>tutti gli altri </p> </td> 
   <td> <p>Inglese </p> <p>Tedesco </p> <p>- </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> ^loc=E^Inglese^loc=UKE^Inglese-Regno Unito^loc=D^Tedesco^loc=DAT^Austriaco </span> </p> </td> 
   <td> <p> en, en_us </p> <p> en_uk </p> <p> de_de </p> <p>de_at </p> <p>tutti gli altri </p> </td> 
   <td> <p>Inglese </p> <p>Inglese (Regno Unito) </p> <p>Tedesco </p> <p>Austriaco </p> <p>- </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> ^ loc=en^English^loc=USE^US-English^loc=D^German^loc=DDE^Deutsch </span> </p> <p> Per questo esempio, il DDE <span class="varname"> locId </span> non esiste nell'attributo <span class="codeph">::LocaleStrMap </span> e pertanto la sottostringa associata a questo locId <span class="varname"> </span> non viene mai restituita. </p> </td> 
   <td> <p> en, en_uk </p> <p> en_us </p> <p> de, de_at, de_de </p> <p>tutti gli altri </p> </td> 
   <td> <p>Inglese </p> <p>Inglese (Stati Uniti) </p> <p>Tedesco </p> <p>- </p> </td> 
  </tr> 
 </tbody> 
</table>
