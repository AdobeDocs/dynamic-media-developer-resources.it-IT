---
title: illum
description: Selettore mappa di illuminazione. Specifica la mappa di illuminazione con cui preferisce eseguire il rendering di questo materiale.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: e1af2397-8eae-4b77-abb1-61ba8cb866f3
TQID: 'https://experienceleague.adobe.com/U8GuX11t9om906OWWj6GwWVopwJcYDfH-FNmVxlIBpg'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 80
ht-degree: 3%

---

# illum{#illum}

Selettore mappa di illuminazione. Specifica la mappa di illuminazione con cui preferisce eseguire il rendering di questo materiale.

`illum=-1|0|1|2`

Se la mappa di illuminazione specificata non è disponibile nella vignettatura di destinazione, viene utilizzata la mappa disponibile più vicina.

`illum=-1` Specifica che la mappa di illuminazione viene selezionata automaticamente in base al valore `gloss=`.

## Proprietà {#section-aace8466566e4cf1a0c5a6c0167245c9}

Attributo materiale. Ignorato se la vignettatura non definisce mappe di illuminazione multiple.

## Predefinito {#section-c96ecfb232074e80b6a29076f5199403}

`illum=-1`

## Consultate anche {#section-9132e60381c64aa3a8ed1319690db55e}

[gloss=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-gloss.md#reference-325aef2ee51e4e1584a06047427340ca)
