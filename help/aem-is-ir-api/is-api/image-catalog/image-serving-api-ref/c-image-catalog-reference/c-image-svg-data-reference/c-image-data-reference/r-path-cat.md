---
description: Percorso file immagine.
solution: Experience Manager
title: Percorso
feature: Dynamic Media Classic, SDK/API
role: Developer,Business Practitioner
exl-id: 9d5417df-3aa2-4620-a614-ca71a96e2069
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '152'
ht-degree: 4%

---

# Percorso{#path}

Percorso file immagine.

Percorso relativo o assoluto e nome del file immagine di origine associato al record del catalogo. Per trovare il file di dati, il server utilizza le regole di risoluzione del percorso descritte in Gestione dei dati di origine .

## Proprietà {#path-properties}

Stringa di testo. Obbligatorio per i record immagine, può essere vuoto per i record modello. Se specificato, deve essere un percorso di file server di immagini relativo o assoluto valido. attribute::DefaultExt viene aggiunto se non è presente alcun suffisso di file.

## Formati di file immagine supportati {#path-supported-image-file-formats}

Fare riferimento alla descrizione dell&#39;utilità Image Converter (IC) per un elenco completo dei formati di file supportati.

Le applicazioni che richiedono dati di immagine in più risoluzioni diverse avranno prestazioni migliori quando si utilizza il formato multi-risoluzione TIFF (PTIFF) piramidale di Dynamic Media. L&#39;utilità IC viene utilizzata per creare immagini PTIFF da qualsiasi formato immagine supportato.

## Predefinito {#path-default}

Nessuno.

## Consultate anche {#path-seealso}

[Utilità](/help/aem-is-ir-api/is-api/is-utils/utilities/r-ic.md)  IC,  [attributo::RootPath](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md) ,  [attributo::DefaultExt](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultext.md) ,  [src=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-src.md)

<!-- [attribute::LowerCasePaths]() -->
