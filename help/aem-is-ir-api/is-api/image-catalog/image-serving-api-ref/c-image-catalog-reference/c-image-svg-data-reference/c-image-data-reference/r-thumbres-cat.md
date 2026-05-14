---
description: Risoluzione delle miniature. Specifica la risoluzione dell'oggetto per l'immagine miniatura.
solution: Experience Manager
title: ThumbRes
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 1b462b7e-076d-433e-a5d2-e254396c4659
TQID: 'https://experienceleague.adobe.com/A7vuk3uRPTC-EUgmh4OhVHYYA4BThHxD0vMnB3yw1Bs'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 69
ht-degree: 4%

---

# ThumbRes{#thumbres}

Risoluzione delle miniature. Specifica la risoluzione dell&#39;oggetto per l&#39;immagine miniatura.

Utilizzato solo se `catalog::ThumbType=3`.

## Proprietà {#section-ee5cae086a3d4875805fa8a08756a586}

Valore numerico reale maggiore di 0. Deve avere le stesse unità di `catalog::Resolution`.

## Predefinito {#section-f0e453fc8a7c451db21961c084eecabd}

`attribute::ThumbRes` viene utilizzato se il campo non è presente, se il valore è 0 o se il campo è vuoto.

## Consultate anche {#section-eb716bf647614db083020fe8ce453751}

[catalogo:ThumbType](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-thumbtype-cat.md#reference-41149ddffc8749cba2f8d9c8e2611e03) , [catalogo::Risoluzione](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-resolution-cat.md#reference-de489f5f36b64bd0831749546f8728e1), [attributo::ThumbRes](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-thumbres.md#reference-ac36cbbd0c8c433ebf7f515e54846501), [req=tmb](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76), [Ridimensionamento miniature](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-notes-on-server-behavior/r-thumbnail-scaling.md#reference-0f71817f721d4913b34816758d69b07f)
