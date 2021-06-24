---
description: Utilizzato da MetadataField/type, saveMetadataFieldParam/fieldType e createMetadataField/fieldType.
solution: Experience Manager
title: Tipi di campi metadati
feature: Dynamic Media Classic, SDK/API, Metadati
role: Developer,Administrator
exl-id: cbbe55f2-bd22-44f5-9440-f58fb45b8d9a
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '101'
ht-degree: 0%

---

# Tipi di campi metadati{#metadata-field-types}

Utilizzato da MetadataField/type, saveMetadataFieldParam/fieldType e createMetadataField/fieldType.

Sintassi

## Valori {#section-1d8f05dbeff74bfdbd5960ccc7347557}

* [!DNL `Untyped`]
* [!DNL `Boolean`]
* [!DNL `BooleanTag`]: Un caso speciale di  [!DNL `SingleFixedTag`] con un dizionario non modificabile inizializzato ai valori  [!DNL `True`] e  [!DNL `False`].

* [!DNL `Color`]
* [!DNL `Date`]
* [!DNL `Dimension`]
* [!DNL `FileName`]
* [!DNL `Float`]
* [!DNL `Int`]
* [!DNL `MultiFixedTag`]: Zero o più valori stringa da un dizionario chiuso. Solo gli utenti amministratori possono modificare il dizionario.
* [!DNL `MultiTag`]: Zero o più valori stringa.
* [!DNL `SingleFixedTag`]: Un singolo valore di stringa da un dizionario chiuso. Se `setAssetMetadata` o `batchSetAssetMetadata` vengono chiamati con un valore non presente nel dizionario, verrà restituito un errore. Solo gli utenti amministratori possono modificare il dizionario.

* [!DNL `SingleTag`]: Qualsiasi valore di stringa singolo.
* [!DNL `String`]
