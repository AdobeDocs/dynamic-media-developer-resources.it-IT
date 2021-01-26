---
description: Scansione JPEG progressiva. Il formato JPEG progressivo visualizza un’immagine in modo da mostrare inizialmente una foto sfocata o di bassa qualità nella sua interezza. Continuando, la scansione diventa più chiara man mano che i dati dell'immagine vengono scaricati completamente. Questo parametro consente di impostare il numero di scansioni necessarie (3, 4 o 5) per visualizzare l’intera immagine.
seo-description: Scansione JPEG progressiva. Il formato JPEG progressivo visualizza un’immagine in modo da mostrare inizialmente una foto sfocata o di bassa qualità nella sua interezza. Continuando, la scansione diventa più chiara man mano che i dati dell'immagine vengono scaricati completamente. Questo parametro consente di impostare il numero di scansioni necessarie (3, 4 o 5) per visualizzare l’intera immagine.
seo-title: pscan
solution: Experience Manager
title: pscan
topic: Dynamic Media Image Serving - Image Rendering API
uuid: c8e1d7a9-679c-437f-aa53-67aca3f40b30
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '270'
ht-degree: 1%

---


# pscan{#pscan}

Scansione JPEG progressiva. Il formato JPEG progressivo visualizza un’immagine in modo da mostrare inizialmente una foto sfocata o di bassa qualità nella sua interezza. Continuando, la scansione diventa più chiara man mano che i dati dell&#39;immagine vengono scaricati completamente. Questo parametro consente di impostare il numero di scansioni necessarie (3, 4 o 5) per visualizzare l’intera immagine.

`pscan=auto|3|4|5`

La velocità effettiva di ogni scansione dipende dalla velocità di trasmissione del sistema dell&#39;utente e del computer che riceve e decomprime i dati.

`Auto` utilizza le impostazioni di scansione calcolate dalla libreria JPEG indipendente e che dipendono dal modello di colore. I valori di `3`, `4`, `5` corrispondono all&#39;impostazione di scansione rilevata in  Adobe Photoshop quando si salva un file JPEG come pjpeg (JPEG progressivo).

Se `pscan` non è impostato, il valore predefinito è `auto`.

## Proprietà {#section-e36aa3c63a974b969d9e4f43fe5a37ab}

Attributo di richiesta. Si applica indipendentemente dall’impostazione del livello corrente. Ignorato se il formato di output non è JPEG progressivo.

## Predefinito {#section-01948f6cd7a2415091004cd7526436c7}

`pscan=auto`

## Esempio {#section-d51bc4d0e8a9473786f149cba9540506}

`http://localhost:8080/is/image/demo/bedroom.tif?wid=300&fmt=pjpeg&pscan=4`

## Consultate anche {#section-2105c6441d2b42edb15c7abc4e20d7fc}

[fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a)
