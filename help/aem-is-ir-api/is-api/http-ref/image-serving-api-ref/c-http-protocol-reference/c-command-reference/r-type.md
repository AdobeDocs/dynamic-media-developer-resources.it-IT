---
description: Filtro del tipo di contenuto statico. Specifica una stringa di filtro per il contenuto statico distribuito tramite /is/content.
seo-description: Filtro del tipo di contenuto statico. Specifica una stringa di filtro per il contenuto statico distribuito tramite /is/content.
seo-title: Testo
solution: Experience Manager
title: Testo
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 44906190-516c-481c-9714-bb19d77af33c
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '123'
ht-degree: 4%

---


# type{#type}

Filtro del tipo di contenuto statico. Specifica una stringa di filtro per il contenuto statico distribuito tramite /is/content.

`type= *`val`*`

<table id="simpletable_B66354A826434A678F3DBC686A0F1436"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> val</span> </p> </td> 
  <td class="stentry"> <p>Digitare la stringa del filtro. </p></td> 
 </tr> 
</table>

Il server confronterà val con il valore di `catalog::Type` dell&#39;elemento di contenuto statico richiesto. L&#39;elemento viene restituito al client se i valori corrispondono (con distinzione tra maiuscole e minuscole), in caso contrario viene restituito un errore.

## Proprietà {#section-529b088434a44a9f86a64ef548d2925b}

Supportato solo per le richieste di contenuto statico (non immagini) servite da. Ignorato se `catalog::Type` è vuoto o non è definito.

## Predefinito {#section-e9e8f51d0a01452183ccb510efd87d46}

Non viene applicata alcuna corrispondenza di tipo se `type=` non è specificato o è vuoto.

## Consultate anche {#section-da60777a46a74f1bbfa5b2f3b240eb0f}

[Contenuti](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-serving-static-non-image-content.md#reference-cbe50e697fdf4c7bbb0084f98b7739da) statici (non-immagine),  [catalogo::UserType](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-usertype-cat.md)
