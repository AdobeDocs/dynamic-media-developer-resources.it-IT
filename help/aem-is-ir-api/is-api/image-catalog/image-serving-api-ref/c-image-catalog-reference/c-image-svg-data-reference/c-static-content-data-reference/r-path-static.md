---
title: Percorso
description: Il server utilizza le regole di risoluzione del percorso per trovare il file di dati.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 9f273f32-1699-4bc3-8dd0-f1dfefaa6e27
source-git-commit: c1a4dad7888d31e0b78f0fc5091700ad8104e685
workflow-type: tm+mt
source-wordcount: '140'
ht-degree: 2%

---

# Percorso{#path}

Il server utilizza le regole di risoluzione dei percorsi descritte in [Gestione dei dati di origine](../../../../../../is-api/image-serving-api-ref/c-configuration-and-administration/c-configuration-and-administration.md#concept-1ec4d9f0e58a430cae045761f1ff9173) per trovare il file di dati.

## Proprietà {#section-72d9edc532ad43349afcb4df22e1c692}

Stringa di testo. Obbligatorio per i record immagine e SVG, potrebbe essere vuoto per i record modello. Se specificato, deve essere un percorso di file del server immagini relativo o assoluto valido. attribute::DefaultExt viene aggiunto se non è presente alcun suffisso di file.

## Formati di file immagine supportati {#section-8d6443c883aa48aaa00316fe9661aaa8}

Per un elenco completo dei formati di file di immagine supportati, consultare la descrizione dell&#39;utilità Image Converter (IC).

Le applicazioni che richiedono dati immagine in più risoluzioni diverse offrono prestazioni ottimali quando si utilizza il formato a più risoluzioni Dynamic Media pyramid TIFF (PTIFF). L&#39;utilità IC viene utilizzata per creare immagini PTIFF da qualsiasi formato di immagine supportato.

## Predefinito {#section-82dad83ec3f84ae8bf2f850b4139f63e}

Nessuno.

## Consultate anche {#section-b36074fae77d49f5bdfd63e9c36aa3ba}

[Utilità IC](../../../../../../is-api/is-utils/utilities/r-ic.md#reference-de9f43c63a8f48f1a755ff1760af8b7b), [attribute::RootPath](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md#reference-17d57e5967be403b8408fa7214017494), [attribute::DefaultExt](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultext.md#reference-1b96c71a253049ddaeae09892d3484a0), [src=](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-src.md#reference-f6506637778c4c69bf106a7924a91ab1)
