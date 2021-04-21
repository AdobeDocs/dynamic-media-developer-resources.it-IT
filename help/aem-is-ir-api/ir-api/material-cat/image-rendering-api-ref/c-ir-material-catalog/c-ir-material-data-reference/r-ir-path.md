---
description: Percorso file immagine. Percorso relativo e nome di un file immagine di texture o decal.
solution: Experience Manager
title: Percorso *
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '216'
ht-degree: 3%

---


# Percorso *{#path}

Percorso file immagine. Percorso relativo e nome di un file immagine di texture o decal.

Il server combina questo valore con `attribute::RootPath` per creare il percorso effettivo del file immagine. Può anche essere un percorso assoluto.

Utilizzato per specificare il file immagine texture per materiali di texture, cabinet e rivestimento di finestre, e il file immagine RGB o RGBA per i materiali di decorazione e bordo muro. Non tutti i materiali di rivestimento per armadietti e finestre richiedono un&#39;immagine di texture ripetibile separata.

## Proprietà {#section-8c12ea24f21d4472be677581893e6681}

Stringa di testo. Richiesto per materiali di texture e decal, opzionale per materiali di rivestimento per armadietti e finestre. Se specificato, deve essere un percorso di file relativo o assoluto valido. Deve essere vuoto per i materiali a colori solidi.

## Formati di file supportati {#section-7ef6c9f7c72c4f03ae926d030b6c46d8}

Image Rendering supporta gli stessi formati immagine sorgente di Dynamic Media Image Serving.

Le applicazioni che richiedono dati immagine in più risoluzioni diverse si comportano al meglio quando si utilizza il formato multi-risoluzione TIFF (PTIFF) piramidale di Dynamic Media. Image Server include l&#39;utilità Image Converter (IC) che crea immagini PTIFF da qualsiasi formato supportato.

Per un elenco completo dei formati di file supportati, fare riferimento alla descrizione dell&#39;utilità IC nella documentazione di Image Serving .

## Predefinito {#section-d2e91fcd7d3c45edb34e7d5ae1daadda}

Nessuno.

## Consultate anche {#section-1bf37fab8e5f4c42a03b785abafc53bd}

[Utilità](/help/aem-is-ir-api/is-api/is-utils/utilities/r-ic.md)  IC,  [attributo::RootPath](/help/aem-is-ir-api/ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rootpath.md),  [src=](/help/aem-is-ir-api/ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-src.md)
