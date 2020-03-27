---
description: Percorso del file immagine.
solution: Experience Manager
title: Percorso
topic: Scene7 Image Serving - Image Rendering API
uuid: 0fca88bb-de00-4eff-83ad-c0f5e3b8ece0
translation-type: tm+mt
source-git-commit: 7b837020deef888a038a074d0aa826d43e60aeb6

---


# Percorso{#path}

Percorso del file immagine.

Percorso relativo o assoluto e nome del file immagine di origine associato a questo record catalogo. Il server utilizza le regole di risoluzione dei percorsi descritte in Gestione dei dati di origine per trovare il file di dati.

## Proprietà {#path-properties}

Stringa di testo. Obbligatorio per i record immagine, può essere vuoto per i record modello. Se specificato, deve essere un percorso di file del server immagini relativo o assoluto valido. attribute::DefaultExt viene aggiunto se non è presente alcun suffisso di file.

## Formati di file immagine supportati {#path-supported-image-file-formats}

Per un elenco completo dei formati di file supportati, fare riferimento alla descrizione dell’utility Image Converter (IC).

Le applicazioni che richiedono dati immagine in più risoluzioni diverse otterranno le prestazioni migliori quando si utilizza il formato multirisoluzione TIFF (PTIFF) della piramide multimediale dinamica. L’utility IC viene utilizzata per creare immagini PTIFF da qualsiasi formato di immagine supportato.

## Predefinito {#path-default}

Nessuno.

## Consultate anche {#path-seealso}

[IC Utility](/help/aem-is-ir-api/is-api/is-utils/utilities/r-ic.md) , [attribute::RootPath](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md) , [attribute::DefaultExt](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultext.md) , [src=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-src.md)

<!-- [attribute::LowerCasePaths]() -->