---
description: Percorso del file immagine. Percorso relativo e nome di un file immagine di struttura o decal.
seo-description: Percorso del file immagine. Percorso relativo e nome di un file immagine di struttura o decal.
seo-title: Percorso *
solution: Experience Manager
title: Percorso *
topic: Scene7 Image Serving - Image Rendering API
uuid: 9e85a358-3f2f-4b8b-a98f-03de2a1a8a4c
translation-type: tm+mt
source-git-commit: 7d3902803d42f5d479dd04ac9470a4088809f3d6

---


# Percorso *{#path}

Percorso del file immagine. Percorso relativo e nome di un file immagine di struttura o decal.

Il server combina questo valore con `attribute::RootPath` la creazione del percorso effettivo del file immagine. Può anche essere un percorso assoluto.

Utilizzato per specificare il file immagine della texture per i materiali di rivestimento di texture, cabinet e finestre, nonché il file immagine RGB o RGBA per i materiali di decorazione e bordo della parete. Non tutti i materiali di rivestimento per armadietti e finestre richiedono un&#39;immagine di struttura ripetibile separata.

## Proprietà {#section-8c12ea24f21d4472be677581893e6681}

Stringa di testo. Obbligatorio per materiali di texture e decantazione, opzionale per materiali di rivestimento per armadio e finestre. Se specificato, deve essere un percorso di file relativo o assoluto valido. Deve essere vuoto per i materiali in tinta unita.

## Formati di file supportati {#section-7ef6c9f7c72c4f03ae926d030b6c46d8}

Il rendering delle immagini supporta gli stessi formati delle immagini sorgente di Scene7 Image Server.

Le applicazioni che richiedono dati immagine a diverse risoluzioni si comportano nel modo migliore quando si utilizza il formato multirisoluzione TIFF (PTIFF) piramidale di Scene7. Image Server include l’utilità Image Converter (IC) che crea immagini PTIFF da qualsiasi formato supportato.

Per un elenco completo dei formati di file supportati, consultare la descrizione dell’utility IC nella documentazione di Image Server.

## Predefinito {#section-d2e91fcd7d3c45edb34e7d5ae1daadda}

Nessuno.

## Consultate anche {#section-1bf37fab8e5f4c42a03b785abafc53bd}

[Utility](/help/aem-is-ir-api/is-api/is-utils/utilities/r-ic.md) IC, [attributo::RootPath](/help/aem-is-ir-api/ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rootpath.md), [src=](/help/aem-is-ir-api/ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-src.md)
