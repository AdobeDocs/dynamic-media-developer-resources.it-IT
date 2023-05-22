---
title: Scade
description: Durata predefinita cache client.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 6d9cca06-f675-4ae4-a187-9cd716e7c554
source-git-commit: 8454991568374ecd1c4babdd3210250ea7988c4c
workflow-type: tm+mt
source-wordcount: '103'
ht-degree: 2%

---

# Scade{#expiration}

Durata predefinita cache client. Specifica un intervallo di scadenza predefinito nel caso in cui un record catalogo non contenga un `catalog::Expiration` o `vignette::Expiration` valore. Oppure, se si accede direttamente a un file di vignettatura o a un file di materiale, anziché tramite un record di catalogo.

## Proprietà {#section-8e2bade105ec4905ae5c4911f500279f}

Numero reale, `0` o superiore. Numero di ore mancanti alla scadenza dalla generazione dei dati di risposta. Imposta su `0` per far scadere sempre immediatamente l’immagine di risposta, disattivando in modo efficace il caching dei client. Imposta su `-1` da contrassegnare come *non scadere mai*.

## Predefinito {#section-18cfce46edb441bfae7dd9d3e0217ba9}

Ereditato da `default::Expiration` se non è definita o se è vuota.

## Consultate anche {#section-ecfe21ff789c4b298344ebf7c647b7e7}

[catalogo::scadenza](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-expiration-dataref.md#reference-5e93943abff54c93bf85aae3b911a3ce) , [vignettatura::scadenza](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-vignette-map-reference/r-ir-expiration-vignette.md#reference-df80829da93e4c0ab3f97a1792d9c74c)
