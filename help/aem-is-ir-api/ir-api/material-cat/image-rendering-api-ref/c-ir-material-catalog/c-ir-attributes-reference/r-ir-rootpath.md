---
title: RootPath
description: Percorso radice dati di origine. Valore stringa di testo. Percorso assoluto o segmento di percorso relativo per la cartella principale per tutti i file di dati vignetta, texture, immagine e ICC a cui fa riferimento questo catalogo di immagini.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 0eecb125-8147-4115-883a-cb6c38333270
source-git-commit: 8454991568374ecd1c4babdd3210250ea7988c4c
workflow-type: tm+mt
source-wordcount: '123'
ht-degree: 3%

---

# RootPath{#rootpath}

Percorso radice dati di origine. Valore stringa di testo. Percorso assoluto o segmento di percorso relativo per la cartella principale per tutti i file di dati vignetta, texture, immagine e ICC a cui fa riferimento questo catalogo di immagini.

## Proprietà {#section-5ff1cf592dd24dfc8cfa470c753ab828}

Stringa di testo. Deve essere vuoto, un segmento di percorso valido relativo all&#39;impostazione di configurazione del server Image Rendering `ir.resourceRootPaths`o un percorso di file assoluto valido. Non devono includere delimitatori di elementi di percorso iniziali e finali.

## Predefinito {#section-4a7f3ab22b0c4090b3896d29bd192b8a}

Ereditato da `default::RootPath` se non definito. Se definito ma vuoto, non contribuisce al percorso principale del file di origine.

## Consultate anche {#section-92012cc1ce32448ea977e7e0484857e2}

[catalogo::Percorso](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-path.md#reference-59ebb624250a4965ad1737578a2ab590) , [catalogo::AuxPath](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-auxpath.md#reference-943ad5ee3c3b4b06bbcbb005db0dc969), `ir.resourceRootPaths`
