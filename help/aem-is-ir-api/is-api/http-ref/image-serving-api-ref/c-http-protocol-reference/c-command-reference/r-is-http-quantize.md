---
title: quantificare
description: Quantizzazione colore. Specifica gli attributi di quantizzazione del colore per la conversione dell'output GIF.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 71d59961-848e-4d78-875e-066e842ac1bf
source-git-commit: 97fbf820590b53de5a1e6ce904e44d6b0ef9a214
workflow-type: tm+mt
source-wordcount: '231'
ht-degree: 1%

---

# quantificare{#quantize}

Quantizzazione colore. Specifica gli attributi di quantizzazione del colore per la conversione dell&#39;output GIF.

` quantize= *`tipo`*[, *`dithering`*[, *`numColors`*[, *`colorList`*]]]`

<table id="table_A669A9058C8043A5BAE80B03A13B015B"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> tipo </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {adaptive|web|mac} </span> </p> <p>Specifica il tipo di tavolozza. </p> <p>Imposta su <span class="codeph"> adattivo </span> per calcolare una palette ottimale per l'immagine. </p> <p>Impostare su <span class="codeph"> Web </span> o <span class="codeph"> mac </span> per scegliere una tavolozza predefinita. </p> <p> <p>Nota: il tipo di pallet </span> mac <span class="codeph"> è supportato solo per i formati GIF e PNG8, ma non per i formati GIF-Alpha e PNG8-Alpha.</p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> dithering </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {diffuso|off} </span> </p> <p>Specifica le opzioni di dithering. </p> <p>Imposta su <span class="codeph"> diffusione </span> per la diffusione dell'errore Floyd-Steinberg </p> <p>Impostare su <span class="codeph"> di </span> per disabilitare il dithering.</p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> numColors </span> </span> </p> </td> 
   <td colname="col2"> <p>Numero di colori di output (2-256) </p> <p>Specifica quanti colori includere nella tavolozza adattiva </span> di <span class="codeph">.</p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> colorList </span> </span> </p> </td> 
   <td colname="col2"> <p>Elenco separato da virgole di colori RGB obbligatori in formato esadecimale6 </p> <p>Consente di specificare i colori da includere in una tavolozza </span> adattiva <span class="codeph">. Se il numero di colori specificati è inferiore a <span class="codeph"> <span class="varname"> numColors </span> </span>, verranno calcolati colori aggiuntivi in base al contenuto dell'immagine.</p> </td> 
  </tr> 
 </tbody> 
</table>

## Proprietà {#section-8ab5035055b24b858270d260912a7f3d}

Attributo della richiesta. Viene applicato indipendentemente dall&#39;impostazione del livello corrente. Utilizzato solo se `fmt=gif`, `fmt=gif-alpha`, `fmt=png8` o `fmt=png8-alpha`. Altrimenti ignorato.

I colori specificati con *`colorList`* devono essere costituiti da valori RGB in formato hex6 (vedere [color](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-color-commandref.md) senza prefisso `0x`. Non sono consentiti altri identificatori di colore. Il modificatore *`numColors`* deve essere 2-256.

## Predefinito {#section-ca3e817617244e8798ccff67b2023a32}

`quantize=adaptive,diffuse,256`

## Esempio {#section-e34aca7587d548a7ae9d4266b80c9451}

Generare una miniatura GIF utilizzando la tavolozza `web` e senza dithering:

`http:// *`*Server*`*/myRootId/myImageId?req=tmb&fmt=gif&quantize=web,off`

Converte l&#39;immagine in un GIF bitonale con trasparenza dei colori chiave. E, forza i colori a bianco e nero:

`http:// *`*Server*`*/myRootId/myImageId?fmt=gif-alpha&wid=100&quantize=adaptive,off,2,000000,ffffff`

## Consultate anche {#section-ea5e8de6084540cf86010370a4d0f01f}

[fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a) , [colore](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md)
