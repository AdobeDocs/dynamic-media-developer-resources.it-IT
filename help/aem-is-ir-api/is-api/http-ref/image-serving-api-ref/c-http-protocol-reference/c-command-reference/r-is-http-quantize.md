---
title: quantificare
description: quantizzazione del colore. Specifica gli attributi di quantizzazione del colore per la conversione dell'output in GIF.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 71d59961-848e-4d78-875e-066e842ac1bf
source-git-commit: 7c4492b583e7bd6fb87229c4566f1d9493c8a650
workflow-type: tm+mt
source-wordcount: '223'
ht-degree: 2%

---

# quantificare{#quantize}

quantizzazione del colore. Specifica gli attributi di quantizzazione del colore per la conversione dell&#39;output in GIF.

` quantize= *`type`*[, *`dietesi`*[, *`numColors`*[, *`colorList`*]]]`

<table id="table_A669A9058C8043A5BAE80B03A13B015B"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> type </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {adattivo|web|mac} </span> </p> <p>Specifica il tipo di palette. </p> <p>Imposta su <span class="codeph"> adattivo </span> per calcolare una palette ottimale per l’immagine. </p> <p>Imposta su <span class="codeph"> web </span> o <span class="codeph"> mac </span> per scegliere una palette predefinita. </p> <p> <p>Nota: La <span class="codeph"> mac </span> Il tipo di pallet è supportato solo per i formati GIF e PNG8, ma non per i formati GIF-Alpha e PNG8-Alpha. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> dietesi </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {diffusa|disattivata} </span> </p> <p>Specifica le opzioni di dithering. </p> <p>Imposta su <span class="codeph"> diffondere </span> per la diffusione dell'errore Floyd-Steinberg </p> <p>Imposta su <span class="codeph"> off </span> per disabilitare il dithering. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> numColors </span> </span> </p> </td> 
   <td colname="col2"> <p>Numero di colori di uscita (2-256) </p> <p>Specifica quanti colori sono inclusi nel <span class="codeph"> adattivo </span> tavolozza. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> colorList </span> </span> </p> </td> 
   <td colname="col2"> <p>Elenco separato da virgole dei colori RGB forzati in formato esadecimale6 </p> <p>Consente di specificare i colori da includere in un <span class="codeph"> adattivo </span> tavolozza. Se il numero di colori specificato è inferiore a <span class="codeph"> <span class="varname"> numColors </span> </span>, vengono calcolati colori aggiuntivi in base al contenuto dell’immagine. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Proprietà {#section-8ab5035055b24b858270d260912a7f3d}

Attributo di richiesta. Si applica indipendentemente dall&#39;impostazione del livello corrente. Utilizzato solo se `fmt=gif`, `fmt=gif-alpha`, `fmt=png8`oppure `fmt=png8-alpha`. Ignorato altrimenti.

I colori specificati con *`colorList`* deve essere costituito da valori RGB in formato esadecimale6 (vedi [color](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-color-commandref.md) senza `0x` Prefisso. Non sono consentiti altri identificatori di colore. *`numColors`* deve essere compreso tra 2 e 256.

## Predefinito {#section-ca3e817617244e8798ccff67b2023a32}

`quantize=adaptive,diffuse,256`

## Esempio {#section-e34aca7587d548a7ae9d4266b80c9451}

Genera una miniatura di GIF utilizzando `web` tavolozza senza dithering:

` http:// *`server`*/myRootId/myImageId?req=tmb&fmt=gif&quantize=web,off`

Converti l&#39;immagine in un GIF biconale con trasparenza dei colori chiave e forza i colori in bianco e nero:

` http:// *`server`*/myRootId/myImageId?fmt=gif-alpha&wid=100&quantize=adaptive,off,2,000000,ffffff`

## Consultate anche {#section-ea5e8de6084540cf86010370a4d0f01f}

[fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a) , [color](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md)
