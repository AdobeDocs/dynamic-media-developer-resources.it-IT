---
description: Percorso file maschera. Percorso e nome relativi o assoluti per un file di immagine maschera associato a questo record catalogo.
solution: Experience Manager
title: MascheraPercorso
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: b67e0b62-d2cc-4b05-bd09-65b206466df5
TQID: 'https://experienceleague.adobe.com/tUXD-vnkr3qkaH3B-dE-e9wfSPXAcnwRbqG9KuJej9E'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 175
ht-degree: 2%

---

# MascheraPercorso{#maskpath}

Percorso file maschera. Percorso e nome relativi o assoluti per un file di immagine maschera associato a questo record catalogo.

Consente di applicare maschere separate alle immagini.

Il server utilizza le regole di risoluzione dei percorsi descritte in [Gestione dei dati di Source](/help/aem-is-ir-api/is-api/image-serving-api-ref/c-configuration-and-administration/c-configuration-and-administration.md) per trovare il file di dati.

## Proprietà {#section-cdc3b7e2811e41008479cd97887c01b7}

Valore stringa di testo. Facoltativo. Se specificato, deve essere un percorso di file del server immagini relativo o assoluto valido. `attribute::DefaultExt` viene aggiunto se non è presente alcun suffisso di file.

Se in un record di catalogo sono definite sia un&#39;immagine principale ( `catalog::Path`) che un&#39;immagine maschera ( `catalog::MaskPath`), entrambe devono avere esattamente la stessa dimensione in pixel. Le immagini della maschera devono essere in scala di grigi a 8 bit.

`mask=` nella richiesta sostituisce `catalog::MaskPath`.

`catalog::MaskPath` esegue l&#39;override del canale alfa nell&#39;immagine principale ( `catalog::Path`), se presente, e se il canale alfa non è associato (ovvero non è premoltiplicato). Se l&#39;immagine alfa è premoltiplicata, `catalog::MaskPath` viene ignorato e il canale alfa viene sempre utilizzato.

## Predefinito {#section-78533e35bfec469ba087cb68a35bb81b}

Nessuno.

## Consultate anche {#section-68d262f5949c4959b8723ba44611d1dc}

[attribute::RootPath](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md) , [attribute::DefaultExt](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultext.md), [catalog::Path](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-path-cat.md#reference-306afcaff172440ca81b85da8d78213c), [mask=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-mask.md), [req=mask](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md)
