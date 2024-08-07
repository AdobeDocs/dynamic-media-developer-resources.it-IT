---
description: Opzione di corrispondenza catalogo.
solution: Experience Manager
title: FullMatch
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 1a267c48-a8eb-426a-a70a-bdb9f5f20efb
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '160'
ht-degree: 1%

---

# FullMatch{#fullmatch}

Opzione di corrispondenza catalogo.

Una voce di catalogo è specificata come coppia `*`rootId`*/ *`imageId`*` nelle richieste HTTP. Durante l&#39;analisi, viene selezionato un catalogo se `*`rootId`*` corrisponde al valore `attribute::RootId` del catalogo e il record del catalogo è identificato dalla corrispondenza di `*`imageId`*` con un valore `catalog::Id`. Se viene trovato un catalogo ma non esiste una voce corrispondente a `*`imageId`*`, il server può eseguire una delle due operazioni seguenti:

Se `attribute::FullMatch` non è impostato, il server utilizza gli attributi del catalogo corrispondente. In questo caso, `*`rootId`*` è sostituito da `attribute::RootPath` (o `default::RootPath`, se non specificato in questo catalogo).

Se `attribute::FullMatch` è impostato, il server ignora completamente il catalogo, come se non fosse stato trovato alcun catalogo corrispondente, e continua a utilizzare gli attributi di catalogo predefiniti. In questo caso, `*`rootId`*` rimane parte del percorso (preceduto da `default::RootPath`).

## Proprietà {#section-25e021dbe6574d00aadd08a7fa0b6e81}

Bandiera. Imposta su 0 per il comportamento predefinito o su 1 per abilitare il comportamento di corrispondenza completa.

## Predefinito {#section-01c9ea1f1f1d4fd3b5f92799ec8383ff}

Ereditato da `default::FullMatch` se non definito o se vuoto.

## Consultate anche {#section-42da0ba53e0b4c089c62108785faf5a9}

[attributo::RootId](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootid.md#reference-13653312925e4a08b90f99961d53f546) , [catalogo::Id](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-id-cat.md)
