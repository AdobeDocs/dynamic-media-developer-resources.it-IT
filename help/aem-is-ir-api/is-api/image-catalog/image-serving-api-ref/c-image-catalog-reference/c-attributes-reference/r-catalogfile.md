---
description: Percorsi dei file di dati delle immagini. Specifica i file che contengono i dati immagine per questo catalogo.
solution: Experience Manager
title: FileCatalogo
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 240a3884-68dd-474c-83a6-d79fc5b6c300
TQID: 'https://experienceleague.adobe.com/MhxEBtyw3JIvMg5miQotPPCeoLeWATtXy0fbRtE7ePs'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 108
ht-degree: 3%

---

# FileCatalogo{#catalogfile}

Percorsi dei file di dati delle immagini. Specifica i file che contengono i dati immagine per questo catalogo.

I file di dati immagine vengono caricati nell&#39;ordine specificato. Se lo stesso valore `catalog::Id` si trova in più record (nello stesso file di catalogo o in file di catalogo diversi), prevale l&#39;ultima istanza.

## Proprietà {#section-6da55f145ecd4e31a5de52637a436983}

Uno o più valori stringa di testo separati da virgole. Facoltativo. Ogni valore deve essere un percorso assoluto o relativo alla cartella del catalogo.

## Predefinito {#section-80f91cd7a6b2479ebb310319e9c74da7}

Vuoto: indica che questo catalogo immagini non include dati immagine.

## Consultate anche {#section-910b67c5041d44d99a105ad43ff63a37}

[Campi dati catalogo](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-catalog-data-fields/c-catalog-data-fields.md#concept-b19581028ec44f98b9f5943624403d29)
