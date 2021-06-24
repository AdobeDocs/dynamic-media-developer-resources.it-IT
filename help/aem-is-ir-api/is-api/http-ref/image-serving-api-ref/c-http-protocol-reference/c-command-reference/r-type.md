---
description: Filtro del tipo di contenuto statico. Specifica una stringa di filtro per il contenuto statico distribuito tramite /is/content.
solution: Experience Manager
title: Testo
feature: Dynamic Media Classic, SDK/API
role: Developer,Business Practitioner
exl-id: 9015d5f4-e42c-43e0-af85-fc9c278448e7
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '112'
ht-degree: 5%

---

# Testo{#type}

Filtro del tipo di contenuto statico. Specifica una stringa di filtro per il contenuto statico distribuito tramite /is/content.

`type= *`val`*`

<table id="simpletable_B66354A826434A678F3DBC686A0F1436"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> val</span> </p> </td> 
  <td class="stentry"> <p>Digitare la stringa del filtro. </p></td> 
 </tr> 
</table>

Il server confronterà val con il valore di `catalog::Type` dell’elemento di contenuto statico richiesto. L’elemento viene restituito al client se i valori corrispondono (con distinzione tra maiuscole e minuscole), altrimenti viene restituito un errore.

## Proprietà {#section-529b088434a44a9f86a64ef548d2925b}

Supportato solo per richieste di contenuto statico (non-image) servite tramite . Ignorato se `catalog::Type` è vuoto o non è definito.

## Predefinito {#section-e9e8f51d0a01452183ccb510efd87d46}

Se `type=` non è specificato o è vuoto, non viene applicata alcuna corrispondenza al tipo.

## Consultate anche {#section-da60777a46a74f1bbfa5b2f3b240eb0f}

[Serving Static (Non-Image) Contents](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-serving-static-non-image-content.md#reference-cbe50e697fdf4c7bbb0084f98b7739da),  [catalog::UserType](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-usertype-cat.md)
