---
description: Percorso file immagine.
solution: Experience Manager
title: Percorso
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 9d5417df-3aa2-4620-a614-ca71a96e2069
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '146'
ht-degree: 2%

---

# Percorso{#path}

Percorso file immagine.

Percorso e nome relativi o assoluti del file immagine di origine associato a questo record catalogo. Per trovare il file di dati, il server utilizza le regole di risoluzione dei percorsi descritte in Gestione dei dati di Source.

## Proprietà {#path-properties}

Stringa di testo. Obbligatorio per i record immagine. Può essere vuoto per i record modello. Se specificato, deve essere un percorso di file del server immagini relativo o assoluto valido. attribute::DefaultExt viene aggiunto se non è presente alcun suffisso di file.

## Formati di file immagine supportati {#path-supported-image-file-formats}

Per un elenco completo dei formati di file supportati, consultare la descrizione dell&#39;utility Image Converter (IC).

Le applicazioni che richiedono dati immagine in più risoluzioni diverse offrono prestazioni ottimali quando si utilizza il formato a più risoluzioni Dynamic Medie pyramid TIFF (PTIFF). L&#39;utilità IC viene utilizzata per creare immagini PTIFF da qualsiasi formato di immagine supportato.

## Predefinito {#path-default}

Nessuno.

## Consultate anche {#path-seealso}

[Utilità IC](/help/aem-is-ir-api/is-api/is-utils/utilities/r-ic.md) , [attributo::RootPath](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md) , [attributo::DefaultExt](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultext.md) , [src=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-src.md)

<!-- [attribute::LowerCasePaths]() -->
