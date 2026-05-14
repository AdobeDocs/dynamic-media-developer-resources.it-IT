---
description: Percorsi dei file di dati del catalogo dei contenuti statici. Specifica i file che contengono i dati del contenuto statico per questo catalogo.
solution: Experience Manager
title: StaticContentCatalogFile
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: ff6f0ad8-189f-4172-89cb-f138d2df8fe4
TQID: 'https://experienceleague.adobe.com/98uNzMz83z3lfa2d3LNixYKZzUWWE9zqrK1fnPo-JNA'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 116
ht-degree: 3%

---

# StaticContentCatalogFile{#staticcontentcatalogfile}

Percorsi dei file di dati del catalogo dei contenuti statici. Specifica i file che contengono i dati del contenuto statico per questo catalogo.

I file di dati statici del catalogo dei contenuti vengono caricati nell&#39;ordine specificato. Se lo stesso valore `static::Id` si trova in più record (nello stesso file di catalogo o in file di catalogo diversi), prevale l&#39;ultima istanza.

## Proprietà {#section-3f8dc8d21fa84fbeb71db6ca1ecbdd8c}

Uno o più valori stringa di testo separati da virgole. Facoltativo. Ogni valore deve essere un percorso assoluto o relativo alla cartella del catalogo.

## Predefinito {#section-702edfbc00c54fc29e412a3ff99fef2b}

Vuoto: indica che questo catalogo immagini non include dati di contenuto statico.

## Consultate anche {#section-13d78d475fff40e7a4edf9a9c73f3c15}

[Dati catalogo](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-catalog-data-fields/c-catalog-data-fields.md#concept-b19581028ec44f98b9f5943624403d29)
