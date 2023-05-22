---
description: Percorso file maschera. Percorso e nome relativi o assoluti per un file di immagine maschera associato a questo record catalogo.
solution: Experience Manager
title: MascheraPercorso
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: b67e0b62-d2cc-4b05-bd09-65b206466df5
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '171'
ht-degree: 2%

---

# MascheraPercorso{#maskpath}

Percorso file maschera. Percorso e nome relativi o assoluti per un file di immagine maschera associato a questo record catalogo.

Consente di applicare maschere separate alle immagini.

Il server utilizza le regole di risoluzione dei percorsi descritte in [Gestione dei dati di origine](/help/aem-is-ir-api/is-api/image-serving-api-ref/c-configuration-and-administration/c-configuration-and-administration.md) per trovare il file di dati.

## Proprietà {#section-cdc3b7e2811e41008479cd97887c01b7}

Valore stringa di testo. Facoltativo. Se specificato, deve essere un percorso di file del server immagini relativo o assoluto valido. `attribute::DefaultExt` viene aggiunto se non è presente alcun suffisso di file.

Se entrambe le immagini sono principali ( `catalog::Path`) e un&#39;immagine maschera ( `catalog::MaskPath`) sono definiti in un record di catalogo, entrambi devono avere esattamente la stessa dimensione in pixel. Le immagini della maschera devono essere in scala di grigi a 8 bit.

`mask=` nelle sostituzioni di richiesta `catalog::MaskPath`.

`catalog::MaskPath` sostituisce il canale alfa nell&#39;immagine principale ( `catalog::Path`), se presente, e se il canale alfa non è associato (ovvero non premoltiplicato). Se l&#39;immagine alfa è premoltiplicata, `catalog::MaskPath` viene ignorato e viene sempre utilizzato il canale alfa.

## Predefinito {#section-78533e35bfec469ba087cb68a35bb81b}

Nessuno.

## Consultate anche {#section-68d262f5949c4959b8723ba44611d1dc}

[attribute::RootPath](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md) , [attribute::DefaultExt](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultext.md), [catalog::Path](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-path-cat.md#reference-306afcaff172440ca81b85da8d78213c), [mask= maschera](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-mask.md), [req=mask](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md)
