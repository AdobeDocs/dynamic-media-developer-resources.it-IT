---
description: Percorso file immagine. Percorso relativo e nome di un file di immagine texture o decalcomania.
solution: Experience Manager
title: Percorso*
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 28758709-26ae-4261-b11e-34e37b9d1b8c
TQID: 'https://experienceleague.adobe.com/ndDZ1MOPM1GHqOKFkwwMnJoZHVjaCeVVEHudb-5fPk0'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 208
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
