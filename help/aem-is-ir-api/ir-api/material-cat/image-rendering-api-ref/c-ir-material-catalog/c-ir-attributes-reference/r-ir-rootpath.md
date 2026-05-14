---
title: PercorsoDirectoryPrincipale
description: Percorso directory principale dati di Source. Valore stringa di testo. Percorso assoluto o segmento di percorso relativo per la cartella principale per tutti i file di dati vignettatura, texture, immagine e ICC a cui fa riferimento questo catalogo immagini.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 0eecb125-8147-4115-883a-cb6c38333270
TQID: 'https://experienceleague.adobe.com/yCtXjcZDG0HCqydirr7TDe5-e0oWtHmlvAxHDl-gfac'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 123
ht-degree: 2%

---

# PercorsoDirectoryPrincipale{#rootpath}

Percorso directory principale dati di Source. Valore stringa di testo. Percorso assoluto o segmento di percorso relativo per la cartella principale per tutti i file di dati vignettatura, texture, immagine e ICC a cui fa riferimento questo catalogo immagini.

## Proprietà {#section-5ff1cf592dd24dfc8cfa470c753ab828}

Stringa di testo. Deve essere vuoto, un segmento di percorso valido relativo all&#39;impostazione di configurazione del server Image Rendering `ir.resourceRootPaths` oppure un percorso di file assoluto valido. Non deve includere delimitatori di elementi del percorso iniziale e finale.

## Predefinito {#section-4a7f3ab22b0c4090b3896d29bd192b8a}

Ereditato da `default::RootPath` se non definito. Se definito ma vuoto, non contribuisce al percorso radice del file di origine.

## Consultate anche {#section-92012cc1ce32448ea977e7e0484857e2}

[catalogo::Percorso](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-path.md#reference-59ebb624250a4965ad1737578a2ab590) , [catalogo::AuxPath](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-auxpath.md#reference-943ad5ee3c3b4b06bbcbb005db0dc969), `ir.resourceRootPaths`
