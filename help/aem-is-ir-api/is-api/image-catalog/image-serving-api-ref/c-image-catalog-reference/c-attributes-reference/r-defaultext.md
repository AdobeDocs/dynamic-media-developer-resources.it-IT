---
description: Suffisso file immagine predefinito. Aggiunto al valore del campo Percorso (o Percorso maschera del catalogo) del catalogo se il percorso non include un suffisso file
solution: Experience Manager
title: DefaultExt
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 43b3e5b8-6374-458d-8503-8e04c8c84233
TQID: 'https://experienceleague.adobe.com/3juJVbcGdP1Z-F5inwe-Do7vkk80T-SNJmAiotjU6iw'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 139
ht-degree: 2%

---

# DefaultExt{#defaultext}

Suffisso file immagine predefinito. Aggiunto al valore del campo catalog::Path (o catalog::MaskPath) se il percorso non include un suffisso file

Un suffisso di file è costituito da un punto e da uno o più caratteri compresi tra il punto e la fine della stringa. Il suffisso viene aggiunto al percorso http, se il percorso non viene risolto in una voce di catalogo e se l’ultimo elemento percorso non include un suffisso file.

## Proprietà {#section-b024e6450b414ccc8b83a48a3b4e00f9}

Stringa di testo. Deve includere un carattere &quot;.&quot; iniziale e uno o più caratteri.

## Predefinito {#section-1194c36ffe0748c5b9ff7d732a506588}

Ereditato da `default::DefaultExt` se non definito. Se definito ma vuoto, ai nomi delle immagini non viene applicato alcun suffisso predefinito quando si utilizza questo catalogo.

## Consultate anche {#section-d7c408b979844643adff8258f500eb7c}

[catalogo::Percorso](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-path-cat.md) , [catalogo::PercorsoMaschera](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-maskpath-cat.md)
