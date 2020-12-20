---
description: Quantizzazione del colore. Specifica gli attributi di quantizzazione del colore per la conversione dell’output in formato GIF.
seo-description: Quantizzazione del colore. Specifica gli attributi di quantizzazione del colore per la conversione dell’output in formato GIF.
seo-title: quantificare
solution: Experience Manager
title: quantificare
topic: Scene7 Image Serving - Image Rendering API
uuid: 4e9c4807-59bc-4eb9-bcab-0bf0cfdf56d4
translation-type: tm+mt
source-git-commit: 94a26628ec619076f0942e9278165cc591f1c150
workflow-type: tm+mt
source-wordcount: '233'
ht-degree: 2%

---


# quantizzare{#quantize}

Quantizzazione del colore. Specifica gli attributi di quantizzazione del colore per la conversione dell’output in formato GIF.

` quantize= *``*[, *``*[, *``*[, *`typedithernumColorscolorList`*]]]`

<table id="table_A669A9058C8043A5BAE80B03A13B015B"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> type  </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {adattivo|web|mac}  </span> </p> <p>Specifica il tipo di palette. </p> <p>Impostare su <span class="codeph"> adattivo </span> per calcolare una palette ottimale per l'immagine. </p> <p>Impostare su <span class="codeph"> Web </span> o <span class="codeph"> mac </span> per scegliere una palette predefinita. </p> <p> <p>Nota:  Il tipo di pallet <span class="codeph"> mac </span> è supportato solo per i formati GIF e PNG8, ma non per i formati GIF-Alpha e PNG8-Alpha. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> dithering  </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {diffondere|disattivare}  </span> </p> <p>Specifica le opzioni di dithering. </p> <p>Impostare su <span class="codeph"> diffondere </span> per la diffusione di errori Floyd-Steinberg </p> <p>Impostare su <span class="codeph"> off </span> per disabilitare il dithering. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> numColors  </span> </span> </p> </td> 
   <td colname="col2"> <p>Numero di colori di uscita (2-256) </p> <p>Specifica quanti colori includere nella palette <span class="codeph"> adattiva </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> colorList  </span> </span> </p> </td> 
   <td colname="col2"> <p>Elenco separato da virgole di colori RGB forzati in formato ex6 </p> <p>Consente di specificare i colori da includere in una palette <span class="codeph"> adattiva </span>. Se il numero di colori specificato è inferiore a <span class="codeph"> <span class="varname"> numColors </span> </span>, vengono calcolati colori aggiuntivi in base al contenuto dell'immagine. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Proprietà {#section-8ab5035055b24b858270d260912a7f3d}

Attributo di richiesta. Si applica indipendentemente dall’impostazione del livello corrente. Utilizzata solo se `fmt=gif`, `fmt=gif-alpha`, `fmt=png8` o `fmt=png8-alpha`. Ignorato in caso contrario.

I colori specificati con ` *`colorList`*` devono essere costituiti da valori RGB in formato esadecimale 6 (vedere ` [color](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-color-commandref.md#reference-b044954ec6184253b8831579466b4423)`) senza il prefisso &#39; `0x`&#39;. Non sono consentiti altri identificatori di colore. *`numColors`* deve essere compreso tra 2 e 256.

## Predefinito {#section-ca3e817617244e8798ccff67b2023a32}

`quantize=adaptive,diffuse,256`

## Esempio {#section-e34aca7587d548a7ae9d4266b80c9451}

Generare una miniatura GIF utilizzando la palette `web` senza dithering:

` http:// *`server`*/myRootId/myImageId?req=tmb&fmt=gif&quantize=web,off`

Convertite l’immagine in un GIF biconale con trasparenza a colori chiave e forzate i colori in bianco e nero:

` http:// *`server`*/myRootId/myImageId?fmt=gif-alpha&wid=100&quantize=adaptive,off,2,000000,ffffff`

## Consultate anche {#section-ea5e8de6084540cf86010370a4d0f01f}

[fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a) ,  [colore](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md)
