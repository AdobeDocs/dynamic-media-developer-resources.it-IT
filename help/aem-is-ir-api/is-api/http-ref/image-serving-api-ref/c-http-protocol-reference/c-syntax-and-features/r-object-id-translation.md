---
description: Image Server fornisce un meccanismo per tradurre gli ID di oggetti esterni in ID di oggetti (catalogo) specifici per le impostazioni internazionali. L'applicazione principale consente di fornire contenuto specifico della lingua e contenuto condiviso tra più lingue senza che l'applicazione client debba conoscere gli ID oggetto specifici della lingua.
solution: Experience Manager
title: Traduzione ID oggetto
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 7a3bd6a1-2ad4-4da2-944c-489b7d18fdc1
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '696'
ht-degree: 9%

---

# Traduzione ID oggetto{#object-id-translation}

Image Server fornisce un meccanismo per tradurre gli ID di oggetti esterni in ID di oggetti (catalogo) specifici per le impostazioni internazionali. L&#39;applicazione principale consente di fornire contenuto specifico della lingua e contenuto condiviso tra più lingue senza che l&#39;applicazione client debba conoscere gli ID oggetto specifici della lingua.

L’applicazione può essere scritta utilizzando solo gli ID oggetto globali; Image Server sostituisce automaticamente le immagini specifiche per le impostazioni internazionali e altri contenuti, se disponibili.

Il *`locale`* è specificato nelle richieste Image Server con `locale=` comando.

>[!NOTE]
>
>La traduzione degli ID oggetto è applicabile solo per l’utilizzo basato su catalogo di Image Server. I nomi dei file non possono essere tradotti.

## Ambito {#section-66fcd5bd467c4eeaa1574583cbe9756d}

Tutti i riferimenti alle voci nei cataloghi di contenuto statico, SVG e immagine vengono considerati per i font di traduzione e i riferimenti al profilo ICC non vengono tradotti. Oltre al *`object`* nel percorso di [!DNL /is/image] e [!DNL /is/static requests], questi comandi e attributi del catalogo sono soggetti alla traduzione ID: `src=`, `mask=`, `template=`, `defaultImage=`, `attribute::DefaultImage`, e `attribute::Watermark`.

## Mappa di traduzione ID {#section-9e417b352c314dfe94e831fdd62cddc8}

`attribute::LocaleMap` definisce le regole utilizzate dal server per determinare l’ID del contenuto localizzato, dato come input l’ID dell’oggetto generico e `locale=` valore.

`attribute::LocaleMap` è costituito da un elenco di input *lingue* (corrisponde ai valori specificati con `locale=`), ciascuno con nessuno o più suffissi delle impostazioni internazionali di output ( `*`locSuffixes`*`).

Ad esempio: `attribute::LocaleMap` potrebbe presentarsi così:

`en,_E,|en_us,_E,|en_uk,_E,|fr,_F,|de,_D,|de_at,_D,|de_de,_D,|,_E,`

La richiesta `/is/image/myCat/myImg?locale=de_de` restituisce l’immagine associata alla voce di catalogo `myCat/myImg_D` (supponendo che esista una voce di catalogo).

Fai riferimento alla descrizione di `attribute::LocaleMap` per i dettagli.

## Il processo di traduzione {#section-1f64db17e9f644d88e09853670e14a16}

Nell&#39;esempio precedente, il server cerca prima il *`locale`* &quot; `de_de`&quot; nella mappa di traduzione ID. Quindi scorre il *`locSuffixes`* associato a questa voce-in questo caso &quot; `_D`&quot; e &quot;&quot; (suffisso vuoto). Per ogni iterazione, il suffisso viene aggiunto all&#39;ID immagine e l&#39;ID risultante viene testato per l&#39;esistenza nel catalogo. Se individuata, viene utilizzata tale voce di catalogo, altrimenti viene testata la successiva. In questo esempio, vengono selezionate le voci seguenti: `myCat/myImg_D`, e `myCat/myImg`. Se non viene trovata alcuna corrispondenza, il server restituisce un errore o un’immagine predefinita (se configurata).

## Impostazioni internazionali sconosciute {#section-b2f3c83f2dc845d69b5908107b775537}

Nell’esempio precedente, `attribute::LocaleMap` include un elemento vuoto *`locale`* che definisce la regola di traduzione predefinita, utilizzata per gli elementi sconosciuti `locale=` valori (ovvero, quelli non elencati in modo esplicito nella mappa di traduzione). Se questa mappa di traduzione è stata applicata alla richiesta `/is/image/myCat/myImg?locale=ja`, si risolverebbe in `myCat/myImg_E`, se esiste, o in altro modo `myCat/myImg`.

Se una mappa di traduzione non specifica una regola di traduzione predefinita, viene restituito un errore per tutte le richieste con sconosciuto `locale=` valori.

## Esempi {#section-cc40bb00ee9248bb8cb23e17d7a5984c}

**Ricerca su più livelli**

È spesso auspicabile raggruppare le lingue (ad esempio, europeo, mediorientale e nordamericana) per rispettare gli standard regionali. Ciò può essere ottenuto con una ricerca su più livelli.

Per questo esempio, vogliamo supportare le raccolte per uso occidentale e mediorientale. Entrambe le raccolte sono basate sulla raccolta di immagini generica e per entrambe alcune immagini sono aggiunte o modificate. Entrambe le raccolte vengono quindi ulteriormente perfezionate per specifiche impostazioni internazionali ( `m1`, `m2` per due varianti mediorientali, e `w1`, `w2`, e `w3` per tre lingue occidentali), tranne per il fatto che le immagini sono condivise per `w1` e `w3`. Le lingue sconosciute sono associate solo alla raccolta generica e non hanno accesso alle immagini per lingue specifiche.

`attribute::LocaleMap: w1,-W,|w2,-W2,-W,|w3,-W,|m1,-M1,-M,|m2,-M2,-M,|,`

La tabella seguente illustra quali voci di catalogo vengono considerate e l’ordine in cui vengono considerate per l’ID di input generico `myImg`:

<table id="table_97EB13E3DB9B48D3A4184D5ECC8E9F86"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> <i>locale</i> </b> </th> 
   <th class="entry"> <b>ID catalogo in cui eseguire la ricerca</b> </th> 
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
   <td> <p> <span class="codeph"> myImg </span> </p> </td> 
  </tr> 
 </tbody> 
</table>

**Cerca ID specifici**

Alcune convenzioni di denominazione delle immagini potrebbero non supportare internamente ID immagine generici. Gli ID generici della richiesta devono sempre essere mappati su un ID specifico nel catalogo; spesso l’ID specifico esatto potrebbe non essere noto.

In questo esempio, le immagini per tutte le lingue possono avere `_1`, `_2`, o `_3` suffisso. Le immagini specifiche delle lingue francesi possono avere `_22` o `_23` e le immagini specifiche delle lingue tedesche possono avere `_470` o `_480` suffisso.

`attribute::LocaleMap: ,_1,_2,_3|fr,_22,_23,_1,_2,_3|de,_470,_480,_1,_2,_3| de_at,_470,_480,_1,_2,_3| de_de,_470,_480,_1,_2,_3`

La tabella seguente illustra quali voci di catalogo vengono considerate e l’ordine in cui vengono considerate per l’ID di input generico `myImg`:

<table id="table_A7EE4AA0F1C24284B83CC4B40622D24F"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> <i>locale</i> </b> </th> 
   <th class="entry"> <b>ID di output in cui eseguire la ricerca</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> fr </span> </p> </td> 
   <td> <p> <span class="codeph"> myImg_22, myImg_23, myImg_1, myImg_2,myImg_3 </span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> de </span>, <span class="codeph"> de_at </span>, <span class="codeph"> de_de </span> </p> </td> 
   <td> <p> <span class="codeph"> myImg_470, myImg_480, myImg_1, myImg_2,myImg_3 </span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>tutti gli altri </p> </td> 
   <td> <p> <span class="codeph"> myImg_1, myImg_2, myImg_3 </span> </p> </td> 
  </tr> 
 </tbody> 
</table>

## Consultate anche {#section-05893816c66a406d89f9bfd6ace8d47a}

[attribute::LocaleMap](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-localemap.md#reference-49bbf598f8ea47c3a563755cef306318) , [attribute::DefaultLocale](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultlocale.md#reference-69462ad9923f464f80c2c012342a6b6b), [locale=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-locale.md#reference-8a846b2fbc004a12821b956ed3b25cfb), [req=xlate](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76)
