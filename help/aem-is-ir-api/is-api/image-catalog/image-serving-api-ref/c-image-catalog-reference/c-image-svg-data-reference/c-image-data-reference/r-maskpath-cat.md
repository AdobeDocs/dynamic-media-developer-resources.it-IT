---
description: Percorso del file della maschera. Percorso e nome relativi o assoluti per un file immagine maschera associato a questo record catalogo.
seo-description: Percorso del file della maschera. Percorso e nome relativi o assoluti per un file immagine maschera associato a questo record catalogo.
seo-title: MaskPath
solution: Experience Manager
title: MaskPath
topic: Scene7 Image Serving - Image Rendering API
uuid: a2d1f08a-0a26-41a6-9be2-f5cc2afb15c4
translation-type: tm+mt
source-git-commit: b4331c6f033903ec64f168da0b739927c6066710

---


# MaskPath{#maskpath}

Percorso del file della maschera. Percorso e nome relativi o assoluti per un file immagine maschera associato a questo record catalogo.

Consente di associare maschere separate alle immagini.

Il server utilizza le regole di risoluzione dei percorsi descritte in [Gestione dei dati](/help/aem-is-ir-api/is-api/image-serving-api-ref/c-configuration-and-administration/c-configuration-and-administration.md) di origine per trovare il file di dati.

## Proprietà {#section-cdc3b7e2811e41008479cd97887c01b7}

Valore stringa di testo. Facoltativo. Se specificato, deve essere un percorso di file del server immagini relativo o assoluto valido. `attribute::DefaultExt` viene aggiunto se non è presente alcun suffisso di file.

Se un’immagine principale ( `catalog::Path`) e un’immagine maschera ( `catalog::MaskPath`) sono definiti in un record di catalogo, entrambe devono avere esattamente la stessa dimensione in pixel. Le immagini delle maschere devono essere in scala di grigio a 8 bit.

`mask=` nelle sostituzioni delle richieste `catalog::MaskPath`.

`catalog::MaskPath` sostituisce il canale alfa nell’immagine principale ( `catalog::Path`), se presente, e se il canale alfa non è associato (ovvero non è premoltiplicato). Se l&#39;immagine alfa è premoltiplicata, `catalog::MaskPath` viene ignorata e il canale alfa viene sempre utilizzato.

## Predefinito {#section-78533e35bfec469ba087cb68a35bb81b}

Nessuno.

## Consultate anche {#section-68d262f5949c4959b8723ba44611d1dc}

[attribute::RootPath](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md) , [attribute::DefaultExt](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultext.md), [catalogo::Path](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-path-cat.md#reference-306afcaff172440ca81b85da8d78213c), [mask=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-mask.md), [req=mask](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md)
