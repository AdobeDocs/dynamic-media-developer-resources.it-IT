---
description: Percorso file maschera. Percorso e nome relativi o assoluti per un file immagine maschera associato a questo record del catalogo.
solution: Experience Manager
title: MaskPath
feature: Dynamic Media Classic, SDK/API
role: Sviluppatore, Business Practices
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '179'
ht-degree: 3%

---


# MaskPath{#maskpath}

Percorso file maschera. Percorso e nome relativi o assoluti per un file immagine maschera associato a questo record del catalogo.

Consente di allegare maschere separate alle immagini.

Il server utilizza le regole di risoluzione del percorso descritte in [Gestione dei dati di origine](/help/aem-is-ir-api/is-api/image-serving-api-ref/c-configuration-and-administration/c-configuration-and-administration.md) per trovare il file di dati.

## Proprietà {#section-cdc3b7e2811e41008479cd97887c01b7}

Valore stringa di testo. Facoltativo. Se specificato, deve essere un percorso di file server di immagini relativo o assoluto valido. `attribute::DefaultExt` viene aggiunto se non è presente alcun suffisso di file.

Se sia un’immagine principale ( `catalog::Path`) che un’immagine maschera ( `catalog::MaskPath`) sono definite in un record di catalogo, entrambe devono avere esattamente la stessa dimensione di pixel. Le immagini della maschera devono essere in scala di grigi a 8 bit.

`mask=` nelle sostituzioni della richiesta  `catalog::MaskPath`.

`catalog::MaskPath` sostituisce il canale alfa nell’immagine principale (  `catalog::Path`), se presente, e se il canale alfa non è associato (cioè non è pre-moltiplicato). Se l&#39;immagine alfa è pre-moltiplicata, `catalog::MaskPath` viene ignorata e il canale alfa viene sempre utilizzato.

## Predefinito {#section-78533e35bfec469ba087cb68a35bb81b}

Nessuno.

## Consultate anche {#section-68d262f5949c4959b8723ba44611d1dc}

[attributo::RootPath](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md) ,  [attributo::DefaultExt](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultext.md),  [catalogo::Path](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-path-cat.md#reference-306afcaff172440ca81b85da8d78213c),  [mask=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-mask.md),  [req=mask](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md)
