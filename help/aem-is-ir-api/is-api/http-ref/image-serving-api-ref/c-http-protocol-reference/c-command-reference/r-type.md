---
title: tipo
description: Filtro del tipo di contenuto statico. Specifica una stringa di filtro per il contenuto statico distribuito tramite /is/content.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 9015d5f4-e42c-43e0-af85-fc9c278448e7
source-git-commit: 6a4c1f4425199cfa6088fc42137552748c1a9dcf
workflow-type: tm+mt
source-wordcount: '105'
ht-degree: 2%

---

# tipo{#type}

Filtro del tipo di contenuto statico. Specifica una stringa di filtro per il contenuto statico distribuito tramite /is/content.

`type= *`val`*`

<table id="simpletable_B66354A826434A678F3DBC686A0F1436"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> val</span> </p> </td> 
  <td class="stentry"> <p>Digita la stringa del filtro. </p></td> 
 </tr> 
</table>

Il server confronta `val` con il valore di `catalog::Type` dell&#39;elemento di contenuto statico richiesto. L&#39;elemento viene restituito al client se i valori corrispondono (distinzione maiuscole/minuscole). In caso contrario viene restituito un errore.

## Proprietà {#section-529b088434a44a9f86a64ef548d2925b}

Supportato solo per le richieste di contenuto statico (non di immagine) servite tramite. Ignorato se `catalog::Type` è vuoto o non definito.

## Predefinito {#section-e9e8f51d0a01452183ccb510efd87d46}

Non viene applicata alcuna corrispondenza del tipo se `type=` non è specificato o è vuoto.

## Consultate anche {#section-da60777a46a74f1bbfa5b2f3b240eb0f}

[Distribuzione di contenuti statici (non immagine)](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-serving-static-non-image-content.md#reference-cbe50e697fdf4c7bbb0084f98b7739da), [catalog:::UserType](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-usertype-cat.md)
