---
description: Set di immagini. Specifica un valore del set di immagini da utilizzare per la generazione della risposta req=set.
solution: Experience Manager
title: imageSet
feature: Dynamic Media Classic, SDK/API
role: Developer,Business Practitioner
exl-id: 318c658d-7126-40f6-870b-11294a3f6f5f
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '125'
ht-degree: 8%

---

# imageSet{#imageset}

Set di immagini. Specifica un valore del set di immagini da utilizzare per la generazione della risposta req=set.

`imageSet=val`

<table id="simpletable_F697691D166C407D82233664814F4663"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> val</span></span> </p> </td> 
  <td class="stentry"> <p>Stringa del set di immagini. </p></td> 
 </tr> 
</table>

Per evitare il valore e garantire che eventuali modificatori inclusi non vengano interpretati come parte della stringa di query URL, l’intero valore deve essere racchiuso tra parentesi graffe. Se il record del catalogo è specificato nel percorso netto, questo valore del modificatore sostituisce `catalog::ImageSet` dal record principale. Per una descrizione della sintassi del set di immagini valida, consulta la documentazione `catalog::ImageSet` .

## Proprietà {#section-66e7bb7bf4664cbcac6f7ebb2f0d3a4f}

Attributo di richiesta. Facoltativo. Sostituisce `catalog::ImageSet` dal record principale.

## Predefinito {#section-e8622ff40408450fb79d028f8d37fa6b}

Nessuno.

## Esempio {#section-68513d3c601f477399602a0741dab390}

Specifica il set di immagini da utilizzare con la richiesta `req=set`:

`http://server/myRootId?imageSet={asset1,asset2,asset3}&req=set`

## Consultate anche {#section-7e0320b2e09d475897082711a8f023a9}

[catalogo::ImageSet](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-imageset-cat.md) ,  [req=set](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76), Richieste set di  [file multimediali](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-media-set-requests.md#reference-f2f2aa11208b47609fe17848d3b86a0b)
