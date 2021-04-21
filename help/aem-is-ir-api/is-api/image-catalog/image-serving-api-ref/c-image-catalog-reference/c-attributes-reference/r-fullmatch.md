---
description: Opzione di corrispondenza del catalogo.
solution: Experience Manager
title: FullMatch
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '166'
ht-degree: 2%

---


# FullMatch{#fullmatch}

Opzione di corrispondenza del catalogo.

Una voce di catalogo è specificata come una coppia `*`rootId`*/ *`imageId`*` nelle richieste HTTP. Durante l&#39;analisi, viene selezionato un catalogo se `*`rootId`*` corrisponde al valore `attribute::RootId` del catalogo e il record del catalogo è identificato dalla corrispondenza di `*`imageId`*` con un valore `catalog::Id`. Se viene trovato un catalogo, ma non è presente una voce di catalogo corrispondente a `*`imageId`*`, il server può eseguire una delle due operazioni seguenti:

Se `attribute::FullMatch` non è impostato, il server utilizza gli attributi del catalogo corrispondente. In questo caso, `*`rootId`*` viene sostituito da `attribute::RootPath` (o `default::RootPath`, se non specificato in questo catalogo).

Se è impostato `attribute::FullMatch`, il server ignora completamente il catalogo, come se non fosse stata rilevata alcuna corrispondenza al catalogo, e continua utilizzando gli attributi di catalogo predefiniti. In questo caso, `*`rootId`*` rimane parte del percorso (preceduto da `default::RootPath`).

## Proprietà {#section-25e021dbe6574d00aadd08a7fa0b6e81}

Bandiera. Imposta su 0 per il comportamento predefinito o su 1 per abilitare il comportamento di corrispondenza completa.

## Predefinito {#section-01c9ea1f1f1d4fd3b5f92799ec8383ff}

Ereditato da `default::FullMatch` se non definito o se vuoto.

## Consultate anche {#section-42da0ba53e0b4c089c62108785faf5a9}

[attributo::RootId](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootid.md#reference-13653312925e4a08b90f99961d53f546) ,  [catalogo::Id](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-id-cat.md)
