---
description: Informazioni utente Digimarc. Specifica le informazioni utente per l'incorporamento Digimarc.
seo-description: Informazioni utente Digimarc. Specifica le informazioni utente per l'incorporamento Digimarc.
seo-title: DigimarcId
solution: Experience Manager
title: DigimarcId
topic: Scene7 Image Serving - Image Rendering API
uuid: 23f1952f-71b7-4b2a-917d-8161ea855ac9
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# DigimarcId{#digimarcid}

Informazioni utente Digimarc. Specifica le informazioni utente per l&#39;incorporamento Digimarc.

## Proprietà {#section-1e11a36d9e0b4bf3858c4ab15fe7a272}

Cinque o sei numeri interi separati da virgola. Il terzo e il quarto numero non sono più utilizzati:

`creator-id, creator-pin, durability [ , chroma ]`

L&#39; `creator-id` e `creator-pin` viene fornito da Digimarc al momento dell&#39;acquisto del servizio. I valori non utilizzati devono essere lasciati vuoti.

`durability` specifica l&#39;intensità di incorporamento della filigrana Digimarc. Può essere 1, 2, 3 o 4, con 1 che indica una durata più debole e 4 la durata più elevata.

Impostate `chroma` su 1 per codificare la filigrana nei dati di crominanza dell’immagine oppure su 0 (impostazione predefinita) per codificarla nella luminanza. Questa impostazione viene ignorata durante l’output delle immagini in scala di grigio.

## Predefinito {#section-d6ecb6e95a7b4232bd612834ea49e6bc}

Ereditato da `default::DigimarcId` se non definito o se vuoto.

## Esempio {#section-8469ae1c27b4461da3d53fbabc32d3c5}

Specificate un ID creatore Digimarc di prova con durata impostata su 4.

`DigimarcId= 404407,32,,,4`

## Consultate anche {#section-75d4d2afd1df4127b31b1a82f30079d8}

[catalogo::DigimarcInfo](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-digimarcinfo-cat.md#reference-4925764ed683466bb7af4b807c86f8ba)
