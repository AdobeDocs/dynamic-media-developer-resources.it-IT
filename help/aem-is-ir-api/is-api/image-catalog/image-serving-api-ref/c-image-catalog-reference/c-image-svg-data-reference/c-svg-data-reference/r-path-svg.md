---
description: Percorso
solution: Experience Manager
title: Percorso
topic: Dynamic Media Image Serving - Image Rendering API
uuid: d1ed8a98-60eb-4bdb-884e-ea08c018d834
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '129'
ht-degree: 6%

---


# Percorso{#path}

Il server utilizza le regole di risoluzione dei percorsi descritte in [Gestione dei dati di origine](../../../../../../is-api/image-serving-api-ref/c-configuration-and-administration/c-configuration-and-administration.md#concept-1ec4d9f0e58a430cae045761f1ff9173) per trovare il file di dati.

## Proprietà {#section-72d9edc532ad43349afcb4df22e1c692}

Stringa di testo. Richiesto per i record immagine e SVG, potrebbe essere vuoto per i record modello. Se specificato, deve essere un percorso di file del server immagini relativo o assoluto valido. attribute::DefaultExt viene aggiunto se non è presente alcun suffisso di file.

## Formati di file immagine supportati {#section-8d6443c883aa48aaa00316fe9661aaa8}

Per un elenco completo dei formati di file immagine supportati, consultate la descrizione dell&#39;utilità Image Converter (IC).

Le applicazioni che richiedono dati immagine in più risoluzioni diverse si riveleranno ottimali quando si utilizza il formato Dynamic Media a piramide TIFF (PTIFF) a risoluzione multipla. L’utility IC viene utilizzata per creare immagini PTIFF da qualsiasi formato di immagine supportato.

## Predefinito {#section-82dad83ec3f84ae8bf2f850b4139f63e}

Nessuno.

## Consultate anche {#section-b36074fae77d49f5bdfd63e9c36aa3ba}

[Utility](../../../../../../is-api/is-utils/utilities/r-ic.md#reference-de9f43c63a8f48f1a755ff1760af8b7b) IC,  [attributo::RootPath](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md#reference-17d57e5967be403b8408fa7214017494),  [attributo::DefaultExt](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultext.md#reference-1b96c71a253049ddaeae09892d3484a0),  [src=](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-src.md#reference-f6506637778c4c69bf106a7924a91ab1)
