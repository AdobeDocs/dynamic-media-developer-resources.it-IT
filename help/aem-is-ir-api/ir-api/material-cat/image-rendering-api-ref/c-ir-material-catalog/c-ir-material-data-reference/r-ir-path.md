---
description: Percorso file immagine. Percorso relativo e nome di un file di immagine texture o decalcomania.
solution: Experience Manager
title: Percorso*
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 28758709-26ae-4261-b11e-34e37b9d1b8c
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '207'
ht-degree: 1%

---

# Percorso*{#path}

Percorso file immagine. Percorso relativo e nome di un file di immagine texture o decalcomania.

Il server combina questo valore con `attribute::RootPath` per generare il percorso effettivo del file di immagine. Può anche essere un percorso assoluto.

Consente di specificare il file di immagine della trama per i materiali di rivestimento per texture, cabinet e finestre e il file di immagine RGB o RGBA per i materiali di bordo per decalcomanie e pareti. Non tutti i materiali di rivestimento di armadi e finestre richiedono un&#39;immagine di texture separata e ripetibile.

## Proprietà {#section-8c12ea24f21d4472be677581893e6681}

Stringa di testo. Necessario per i materiali di texture e decalcomanie, facoltativo per i materiali di rivestimento di armadi e finestre. Se specificato, deve essere un percorso di file relativo o assoluto valido. Deve essere vuoto per i materiali a colori.

## Formati di file supportati {#section-7ef6c9f7c72c4f03ae926d030b6c46d8}

Image Rendering supporta gli stessi formati di immagine sorgente di Dynamic Media Image Server.

Le applicazioni che richiedono dati immagine in più risoluzioni diverse offrono prestazioni ottimali quando si utilizza il formato multi-risoluzione PTIFF (Dynamic Media pyramid TIFF). Image Server include l&#39;utility Image Converter (IC) che crea immagini PTIFF da qualsiasi formato supportato.

Per un elenco completo dei formati di file supportati, consultare la descrizione dell&#39;utility IC nella documentazione di Image Server.

## Predefinito {#section-d2e91fcd7d3c45edb34e7d5ae1daadda}

Nessuno.

## Consultate anche {#section-1bf37fab8e5f4c42a03b785abafc53bd}

[Utilità IC](/help/aem-is-ir-api/is-api/is-utils/utilities/r-ic.md) , [attributo::RootPath](/help/aem-is-ir-api/ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rootpath.md), [src=](/help/aem-is-ir-api/ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-src.md)
