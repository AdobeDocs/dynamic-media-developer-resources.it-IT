---
description: La localizzazione delle stringhe di testo consente ai cataloghi delle immagini di contenere più rappresentazioni specifiche delle impostazioni internazionali per lo stesso valore stringa.
seo-description: La localizzazione delle stringhe di testo consente ai cataloghi delle immagini di contenere più rappresentazioni specifiche delle impostazioni internazionali per lo stesso valore stringa.
seo-title: Localizzazione della stringa di testo
solution: Experience Manager
title: Localizzazione della stringa di testo
topic: Scene7 Image Serving - Image Rendering API
uuid: bdff2403-e3bb-4b3f-a8d7-bb108c1fbee8
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '685'
ht-degree: 3%

---


# Localizzazione della stringa di testo{#text-string-localization}

La localizzazione delle stringhe di testo consente ai cataloghi delle immagini di contenere più rappresentazioni specifiche delle impostazioni internazionali per lo stesso valore stringa.

Il server restituisce al client la rappresentazione che corrisponde alle impostazioni internazionali specificate con `locale=`, evitando così la localizzazione sul lato client e consentendo alle applicazioni di cambiare lingua semplicemente inviando il valore `locale=` appropriato con le richieste di testo IS.

## Ambito {#section-a03f48e3bc0e4ab281909a2bd441a3c2}

La localizzazione delle stringhe di testo viene applicata a tutti gli elementi stringa che includono il token di localizzazione ` ^loc= *`locId`*^` nei seguenti campi del catalogo:

<table id="table_83344EFCB5B5418184E0A0B43D0B23F7"> 
 <thead> 
  <tr> 
   <th class="entry"> <b>Campo catalogo</b> </th> 
   <th class="entry"> <b>Elemento stringa nel campo</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> catalogo::ImageSet  </span> </p> </td> 
   <td> <p>Qualsiasi sottoelemento contenente una stringa traducibile (delimitata da qualsiasi combinazione di separatori ',' ';' ':' e/o l'inizio/fine del campo). </p> <p> Un valore di colore <span class="codeph"> 0xrggbb </span> all'inizio di un campo localizzabile è escluso dalla localizzazione e passato senza modifiche. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalogo:Mappa  </span> </p> </td> 
   <td> <p>Qualsiasi valore di attributo tra virgolette singole o doppie, ad eccezione dei valori degli attributi <span class="codeph"> coords= </span> e <span class="codeph"> shape= </span>. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalogo::Target  </span> </p> </td> 
   <td> <p>Il valore di qualsiasi destinazione <span class="codeph">.*.label </span> e <span class="codeph"> target.*.userdata </span> proprietà. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalogo::UserData  </span> </p> </td> 
   <td> <p>Il valore di qualsiasi proprietà. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Sintassi stringa {#section-d12320edf300409f8e17565b143acafc}

Gli elementi *`string`* abilitati per la localizzazione nel catalogo immagini sono costituiti da una o più stringhe localizzate, ciascuna delle quali è preceduta da un token di localizzazione.

<table id="simpletable_CEFDAE8395E6493E902D58A7E5A25BC7"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> stringElement  </span> </span> </p> </td> 
  <td class="stentry"> <p>[ <span class="varname"> defaultString </span>]*{ <span class="varname"> localizationToken </span> <span class="varname"> localizedString </span>} </p> </td> 
 </tr> 
</table>

<table id="simpletable_0A687FA72C4C4C1AAFFCB43143C1AB3B"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> localizationToken  </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> ^loc=  <span class="varname"> locStr  </span> ^  </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> locId  </span> </span> </p> </td> 
  <td class="stentry"> <p>ID internazionale interno per la <span class="varname"> localizedString </span> che segue <span class="varname"> localizationToken </span>. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> localizedString  </span> </span> </p> </td> 
  <td class="stentry"> <p>Stringa localizzata. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> defaultString  </span> </span> </p> </td> 
  <td class="stentry"> <p>Stringa da utilizzare per le lingue sconosciute. </p> </td> 
 </tr> 
</table>

*`locId`* Deve essere ASCII e non può includere &#39;^&#39;.

&#39;^&#39; può trovarsi in qualsiasi punto delle sottostringhe con o senza codifica HTTP. Il server corrisponde all&#39;intero pattern *`localizationToken`* `^loc=locId^` per separare le sottostringhe.

*`stringElements`* che non includono almeno uno  *`localizationToken`* non sono considerati per la localizzazione.

## La mappa di traduzione {#section-f7ce3df91b724adf95cee44eac4915d4}

`attribute::LocaleStrMap` definisce le regole utilizzate dal server per determinare quali  *`localizedStrings`* restituire al client. È costituito da un elenco di input *`locales`* (corrispondenti ai valori specificati con `locale=`), ciascuno con uno o più ID di lingua interni ( *`locId`*). Ad esempio:

`attribute::LocaleStrMap= en,E|nl,N|de,D|,`

I valori vuoti *`locId`* indicano che la *`defaultString`* deve essere restituita, se disponibile.

Per ulteriori informazioni, fare riferimento alla descrizione di `attribute::LocaleStrMap`.

## Il processo di traduzione {#section-a2a8a3e5850f4f7c9d2318267afe98a2}

Data la mappa di traduzione di esempio sopra e la richiesta `/is/image/myCat/myItem?req=&locale=nl`, il server cerca prima &quot; `nl`&quot; nella mappa delle impostazioni internazionali. La voce corrispondente `nl,N` indica che per ogni *`stringElement`* deve essere restituito il *`localizedString`* contrassegnato con `^loc=N^`. Se la *`localizationToken`* non è presente nella *`stringElement`*, viene restituito un valore vuoto.

Supponiamo che `catalog::UserData` per `myCat/myItem` contenga quanto segue (le interruzioni di riga inserite per chiarezza):

`val1=111?? str1=Default1^loc=N^Dutch1^loc=D^German1?? val2=value2?? str2=^loc=E^English2^loc=N^Dutch2^loc=D^German2?? str3=Default3^loc=N^Dutch3^loc=D^German3`

Il server restituirebbe quanto segue in risposta alla nostra richiesta di esempio:

`val1=111 str1=Dutch1 val2=value2 str2=Dutch2 str3=Dutch3`

## Impostazioni internazionali sconosciute {#section-26dfeefbd60345de94bbfeaaf7741223}

Nell&#39;esempio precedente, `attribute::LocaleStrMap` ha una voce con un valore *`locale`* vuoto. Il server utilizza questa voce per gestire tutti i valori `locale=` che non sono specificati in modo esplicito nel mapping di traduzione.

La mappa di traduzione di esempio specifica che in questo caso la *`defaultString`* deve essere restituita se disponibile. Pertanto, se questa mappa di traduzione fosse applicata alla richiesta `/is/image/myCat/myItem?req=&locale=ja`, verrebbe restituito quanto segue:

`val1=111 str1=Default1 val2=value2 str2= str3=Default3`

## Esempi {#section-ae6ff7fb90754b839f04ed08aadffa3f}

**Famiglie di lingua**

Più valori *`locId`* possono essere associati a ciascun *`locale`* nella mappa di traduzione. Questo consente di supportare varianti specifiche per paese o regione (ad esempio Inglese USA e Inglese Regno Unito) per selezionare *`stringElements`* mentre si gestisce la maggior parte dei contenuti con impostazioni internazionali di base comuni (ad esempio Inglese Internazionale).

Per il nostro esempio, vogliamo aggiungere il supporto per l&#39;inglese specifico per gli Stati Uniti ( ` *`locId`* EUS`) e per l&#39;inglese specifico per il Regno Unito ( ` *`locId`* EUK`), per supportare l&#39;ortografia alternativa occasionale. Se l&#39;EUK o l&#39;EUS non esistessero, ci ritroveremmo di nuovo all&#39;E. Allo stesso modo, le varianti tedesche specifiche per l&#39;Austria ( `DAT`) potrebbero essere rese disponibili dove necessario, mentre restituiscono il tedesco comune *`localizedStrings`* (contrassegnato con `D`) per la maggior parte del tempo.

`attribute::LocaleStrMap` si presenterà così:

`en,E|en_us,EUS,E|en_uk,EUK,E|de,D|de_at,DAT,D|de_de,D`

La tabella seguente descrive l&#39;output di alcune combinazioni rappresentative *`stringElement`* e *`locale`*:

<table id="table_A6B67587C5F44B5E9CD0E7ED29A81198"> 
 <thead> 
  <tr> 
   <th class="entry"> <i>stringElement</i> </th> 
   <th class="entry"> <i>locale</i> </th> 
   <th class="entry"> <p>Stringa di output </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> ^loc=E^Inglese^loc=D^Tedesco  </span> </p> </td> 
   <td> <p> en,en_us, en_uk </p> <p> de, de_at, de_de </p> <p>tutti gli altri </p> </td> 
   <td> <p>Inglese </p> <p>Tedesco </p> <p>- </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> ^loc=E^English^loc=UKE^UK-English^loc=D^German^loc=DAT^Austrian  </span> </p> </td> 
   <td> <p> en, en_us </p> <p> en_uk </p> <p> de, de_de </p> <p>de_at </p> <p>tutti gli altri </p> </td> 
   <td> <p>Inglese </p> <p>Inglese Regno Unito </p> <p>Tedesco </p> <p>Austriaco </p> <p>- </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> ^ loc=it^English^loc=USE^US-English^loc=D^German^loc=DDE^Deutsch  </span> </p> <p> Tenere presente che per questo esempio il codice <span class="varname"> locId </span> DDE non esiste nell'attributo <span class="codeph">::LocaleStrMap </span>, pertanto la sottostringa associata a questo <span class="varname"> locId </span> non viene mai restituita. </p> </td> 
   <td> <p> en, en_uk </p> <p> en_us </p> <p> de, de_at, de_de </p> <p>tutti gli altri </p> </td> 
   <td> <p>Inglese </p> <p>Inglese USA </p> <p>Tedesco </p> <p>- </p> </td> 
  </tr> 
 </tbody> 
</table>

