---
description: Image Serving fornisce un meccanismo per tradurre gli ID oggetti esterni in ID oggetto (catalogo) specifici per le impostazioni internazionali. L’applicazione principale consiste nel fornire contenuto specifico per le impostazioni internazionali e contenuto condiviso tra più impostazioni internazionali senza che l’applicazione client debba conoscere gli ID oggetto specifici per le impostazioni internazionali.
solution: Experience Manager
title: Traduzione ID oggetto
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '706'
ht-degree: 9%

---


# Traduzione ID oggetto{#object-id-translation}

Image Serving fornisce un meccanismo per tradurre gli ID oggetti esterni in ID oggetto (catalogo) specifici per le impostazioni internazionali. L’applicazione principale consiste nel fornire contenuto specifico per le impostazioni internazionali e contenuto condiviso tra più impostazioni internazionali senza che l’applicazione client debba conoscere gli ID oggetto specifici per le impostazioni internazionali.

L’applicazione può essere scritta utilizzando solo ID oggetto globali e Image Serving sostituisce automaticamente le immagini specifiche delle impostazioni internazionali e altri contenuti, se disponibili.

Il *`locale`* viene specificato nelle richieste di Image Server con il comando `locale=` .

>[!NOTE]
>
>La traduzione degli ID oggetto è applicabile solo per l&#39;uso basato su catalogo di Image Serving. Impossibile tradurre i nomi dei file.

## Ambito {#section-66fcd5bd467c4eeaa1574583cbe9756d}

Tutti i riferimenti alle voci nei cataloghi di immagini, SVG e contenuti statici sono considerati per i font-traduzione e i riferimenti di profilo ICC non sono tradotti. Oltre al *`object`* nel percorso di [!DNL /is/image] e [!DNL /is/static requests], questi comandi e attributi del catalogo sono soggetti alla traduzione ID: `src=`, `mask=`, `template=`, `defaultImage=`, `attribute::DefaultImage` e `attribute::Watermark`.

## Mappa di traduzione ID {#section-9e417b352c314dfe94e831fdd62cddc8}

`attribute::LocaleMap` definisce le regole utilizzate dal server per determinare l&#39;ID del contenuto localizzato, dato che come input l&#39;ID dell&#39;oggetto generico e il  `locale=` valore.

`attribute::LocaleMap` è costituito da un elenco di  *impostazioni internazionali di input*  (corrispondenti ai valori specificati con  `locale=`), ciascuna con uno o più suffissi internazionali di output (  `*`locSuffixes`*`).

Ad esempio, `attribute::LocaleMap` potrebbe essere simile al seguente:

`en,_E,|en_us,_E,|en_uk,_E,|fr,_F,|de,_D,|de_at,_D,|de_de,_D,|,_E,`

La richiesta `/is/image/myCat/myImg?locale=de_de` restituirebbe l&#39;immagine associata alla voce di catalogo `myCat/myImg_D` (supponendo che esista una voce di catalogo simile).

Per ulteriori informazioni, fare riferimento alla descrizione di `attribute::LocaleMap` .

## Il processo di traduzione {#section-1f64db17e9f644d88e09853670e14a16}

Dato l&#39;esempio precedente, il server cerca prima il *`locale`* &quot; `de_de`&quot; nella mappa di traduzione ID. Esegue quindi l&#39;iterazione sui valori *`locSuffixes`* associati a questa voce, in questo caso &quot; `_D`&quot; e &quot;&quot; (suffisso vuoto). Per ogni iterazione, il suffisso viene aggiunto all’ID immagine e l’id risultante viene verificato se è presente nel catalogo. Se trovato, viene utilizzata la voce di catalogo, altrimenti viene testata la voce successiva. Per questo esempio, vengono verificate le seguenti voci: `myCat/myImg_D` e `myCat/myImg`. Se non viene trovata alcuna corrispondenza, il server restituisce un errore o un&#39;immagine predefinita (se configurata).

## Impostazioni internazionali sconosciute {#section-b2f3c83f2dc845d69b5908107b775537}

Nell’esempio precedente, `attribute::LocaleMap` include un *`locale`* vuoto che definisce la regola di traduzione predefinita, utilizzata per valori `locale=` sconosciuti (ovvero quelli non elencati esplicitamente nella mappa di traduzione). Se questa mappa di traduzione è stata applicata alla richiesta `/is/image/myCat/myImg?locale=ja`, viene risolta in `myCat/myImg_E`, se esiste, o in altro modo `myCat/myImg`.

Se una mappa di traduzione non specifica una regola di traduzione predefinita, verrà restituito un errore per tutte le richieste con valori `locale=` sconosciuti.

## Esempi {#section-cc40bb00ee9248bb8cb23e17d7a5984c}

**Ricerca a più livelli**

Spesso è opportuno raggruppare le impostazioni internazionali (ad esempio, europee, mediorientali, nordamericane) per soddisfare gli standard regionali. Questo può essere ottenuto con una ricerca a più livelli.

Per questo esempio, vogliamo supportare le raccolte per uso occidentale e medio orientale. Entrambe le raccolte sono basate sulla raccolta di immagini generica e per entrambe alcune immagini sono aggiunte o modificate. Entrambe le raccolte vengono quindi perfezionate ulteriormente per specifiche impostazioni internazionali ( `m1`, `m2` per due varianti medio-orientali e `w1`, `w2` e `w3` per tre impostazioni internazionali occidentali), tranne per il fatto che le immagini sono condivise per `w1` e `w3`. Le lingue sconosciute sono associate solo alla raccolta generica e non hanno accesso alle immagini per lingue specifiche.

`attribute::LocaleMap: w1,-W,|w2,-W2,-W,|w3,-W,|m1,-M1,-M,|m2,-M2,-M,|,`

La tabella seguente illustra le voci di catalogo da considerare e l’ordine in cui vengono considerate per l’ID di input generico `myImg`:

<table id="table_97EB13E3DB9B48D3A4184D5ECC8E9F86"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> <i>locale</i> </b> </th> 
   <th class="entry"> <b>ID catalogo da cercare</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> w1, w3 </span> </p> </td> 
   <td> <p> <span class="codeph"> myImg-W, myImg </span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> w2 </span> </p> </td> 
   <td> <p> <span class="codeph"> myImg-W2, myImg-W, myImg </span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> m1 </span> </p> </td> 
   <td> <p> <span class="codeph"> myImg-M1, myImg-M, myImg </span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> m2 </span> </p> </td> 
   <td> <p> <span class="codeph"> myImg-M2, myImg-M, myImg </span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>tutti gli altri </p> </td> 
   <td> <p> <span class="codeph"> myImg  </span> </p> </td> 
  </tr> 
 </tbody> 
</table>

**Ricerca di ID specifici**

Alcune convenzioni di denominazione delle immagini potrebbero non supportare internamente ID immagine generici. Gli ID generici della richiesta devono sempre essere mappati su un ID specifico nel catalogo; spesso l&#39;ID specifico esatto potrebbe non essere noto.

In questo esempio, le immagini per tutte le lingue possono avere il suffisso `_1`, `_2` o `_3`. Le immagini specifiche per le impostazioni internazionali francesi possono avere il suffisso `_22` o `_23` e le immagini specifiche per le impostazioni internazionali tedesche possono avere il suffisso `_470` o `_480`.

`attribute::LocaleMap: ,_1,_2,_3|fr,_22,_23,_1,_2,_3|de,_470,_480,_1,_2,_3| de_at,_470,_480,_1,_2,_3| de_de,_470,_480,_1,_2,_3`

La tabella seguente illustra le voci di catalogo considerate e l’ordine in cui vengono considerate per l’ID di input generico `myImg`:

<table id="table_A7EE4AA0F1C24284B83CC4B40622D24F"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> <i>locale</i> </b> </th> 
   <th class="entry"> <b>ID di output per la ricerca</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> fr </span> </p> </td> 
   <td> <p> <span class="codeph"> myImg_22, myImg_23, myImg_1, myImg_2,myImg_3 </span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> de  </span>,  <span class="codeph"> de_at  </span>,  <span class="codeph"> de_de  </span> </p> </td> 
   <td> <p> <span class="codeph"> myImg_470, myImg_480, myImg_1, myImg_2,myImg_3 </span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>tutti gli altri </p> </td> 
   <td> <p> <span class="codeph"> myImg_1, myImg_2, myImg_3 </span> </p> </td> 
  </tr> 
 </tbody> 
</table>

## Consultate anche {#section-05893816c66a406d89f9bfd6ace8d47a}

[attributo::LocaleMap](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-localemap.md#reference-49bbf598f8ea47c3a563755cef306318) ,  [attributo::DefaultLocale](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultlocale.md#reference-69462ad9923f464f80c2c012342a6b6b),  [locale=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-locale.md#reference-8a846b2fbc004a12821b956ed3b25cfb),  [req=xlate](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76)
