---
description: Set di immagini. Specifica un valore del set di immagini da utilizzare per la generazione della risposta req=set.
seo-description: Set di immagini. Specifica un valore del set di immagini da utilizzare per la generazione della risposta req=set.
seo-title: imageSet
solution: Experience Manager
title: imageSet
topic: Dynamic Media Image Serving - Image Rendering API
uuid: ecfb3905-e3ef-4ab8-a2c4-2c3f200e0f0f
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '135'
ht-degree: 9%

---


# imageSet{#imageset}

Set di immagini. Specifica un valore del set di immagini da utilizzare per la generazione della risposta req=set.

`imageSet=val`

<table id="simpletable_F697691D166C407D82233664814F4663"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> val</span></span> </p> </td> 
  <td class="stentry"> <p>Stringa set di immagini. </p></td> 
 </tr> 
</table>

Per evitare il valore e assicurarsi che gli eventuali modificatori inclusi non vengano interpretati come parte della stringa di query URL, l’intero valore deve essere racchiuso tra parentesi graffe. Se il record del catalogo è specificato nel percorso di rete, il valore del modificatore sostituisce `catalog::ImageSet` dal record principale. Per una descrizione della sintassi del set di immagini valida, consultate la documentazione di `catalog::ImageSet`.

## Proprietà {#section-66e7bb7bf4664cbcac6f7ebb2f0d3a4f}

Attributo di richiesta. Facoltativo. Ignora `catalog::ImageSet` dal record principale.

## Predefinito {#section-e8622ff40408450fb79d028f8d37fa6b}

Nessuno.

## Esempio {#section-68513d3c601f477399602a0741dab390}

Specificate il set di immagini da usare con la richiesta `req=set`:

`http://server/myRootId?imageSet={asset1,asset2,asset3}&req=set`

## Consultate anche {#section-7e0320b2e09d475897082711a8f023a9}

[catalogo::ImageSet](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-imageset-cat.md) ,  [req=set](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76), richieste di set di  [file multimediali](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-media-set-requests.md#reference-f2f2aa11208b47609fe17848d3b86a0b)
