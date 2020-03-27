---
description: Utilizzato da MetadataField/type, saveMetadataFieldParam/fieldType e createMetadataField/fieldType.
seo-description: Utilizzato da MetadataField/type, saveMetadataFieldParam/fieldType e createMetadataField/fieldType.
seo-title: Tipi di campi metadati
solution: Experience Manager
title: Tipi di campi metadati
topic: Scene7 Image Production System API
uuid: 57d292bb-848a-4e6e-bd08-4e6af1f9fc72
translation-type: tm+mt
source-git-commit: 2bd5b17e473ec53844b4bbcb4f13580b2d6bfaf4

---


# Tipi di campi metadati{#metadata-field-types}

Utilizzato da MetadataField/type, saveMetadataFieldParam/fieldType e createMetadataField/fieldType.

Sintassi

## Valori {#section-1d8f05dbeff74bfdbd5960ccc7347557}

* [!DNL `Untyped`]
* [!DNL `Boolean`]
* [!DNL `BooleanTag`]: Un caso speciale di [!DNL `SingleFixedTag`] un dizionario non modificabile inizializzato sui valori [!DNL `True`] e [!DNL `False`].

* [!DNL `Color`]
* [!DNL `Date`]
* [!DNL `Dimension`]
* [!DNL `FileName`]
* [!DNL `Float`]
* [!DNL `Int`]
* [!DNL `MultiFixedTag`]: Zero o più valori stringa da un dizionario chiuso. Solo gli utenti admin possono modificare il dizionario.
* [!DNL `MultiTag`]: Zero o più valori stringa.
* [!DNL `SingleFixedTag`]: Un singolo valore di stringa da un dizionario chiuso. Se `setAssetMetadata` o `batchSetAssetMetadata` vengono chiamati con un valore non presente nel dizionario, verrà restituito un errore. Solo gli utenti admin possono modificare il dizionario.

* [!DNL `SingleTag`]: Un qualsiasi valore di stringa singolo.
* [!DNL `String`]

