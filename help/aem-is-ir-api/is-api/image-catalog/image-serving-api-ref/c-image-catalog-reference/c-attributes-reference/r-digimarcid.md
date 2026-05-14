---
description: Informazioni utente Digimarc. Specifica le informazioni utente per l'incorporamento Digimarc.
solution: Experience Manager
title: DigimarcId
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: ac09c8cd-cb68-4b70-b1b4-9d4ca0166c7f
TQID: 'https://experienceleague.adobe.com/2kkvN1RLEhbDEmN4cA6lE5nGe9d-T3qcdxgGqF7L3Ig'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 134
ht-degree: 2%

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
