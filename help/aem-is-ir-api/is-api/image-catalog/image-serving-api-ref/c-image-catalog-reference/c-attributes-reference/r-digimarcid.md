---
description: Informazioni utente Digimarc. Specifica le informazioni utente per l'incorporamento Digimarc.
solution: Experience Manager
title: DigimarcId
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: ac09c8cd-cb68-4b70-b1b4-9d4ca0166c7f
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '133'
ht-degree: 3%

---

# DigimarcId{#digimarcid}

Informazioni utente Digimarc. Specifica le informazioni utente per l&#39;incorporamento Digimarc.

## Proprietà {#section-1e11a36d9e0b4bf3858c4ab15fe7a272}

Cinque o sei numeri interi separati da virgole. Il terzo e il quarto numero non vengono più utilizzati:

`creator-id, creator-pin, durability [ , chroma ]`

`creator-id` e `creator-pin` vengono forniti da Digimarc al momento dell&#39;acquisto del servizio. I valori non utilizzati devono essere lasciati vuoti.

`durability` specifica la forza di incorporamento della filigrana Digimarc. Può essere 1, 2, 3 o 4, con 1 che indica la durata più debole e 4 la durata più elevata.

Impostare `chroma` su 1 per codificare la filigrana nei dati di crominanza dell&#39;immagine oppure su 0 (impostazione predefinita) per codificarla nella luminanza. Questa impostazione viene ignorata durante l&#39;output di immagini in scala di grigio.

## Predefinito {#section-d6ecb6e95a7b4232bd612834ea49e6bc}

Ereditato da `default::DigimarcId` se non definito o se vuoto.

## Esempio {#section-8469ae1c27b4461da3d53fbabc32d3c5}

Specifica un ID creatore Digimarc di prova con durata impostata su 4.

`DigimarcId= 404407,32,,,4`

## Consultate anche {#section-75d4d2afd1df4127b31b1a82f30079d8}

[catalog::DigimarcInfo](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-digimarcinfo-cat.md#reference-4925764ed683466bb7af4b807c86f8ba)
