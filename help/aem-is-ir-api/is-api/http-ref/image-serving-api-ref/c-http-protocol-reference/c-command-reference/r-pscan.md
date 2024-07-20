---
title: pscan
description: Scansione JPEG progressiva. Progressive JPEG mostra un'immagine in modo tale che inizialmente sia completamente sfocata/di bassa qualità.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 1afd3a60-e0b6-47d1-b7e4-98a3145782a2
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '181'
ht-degree: 2%

---

# pscan{#pscan}

Scansione JPEG progressiva. Progressive JPEG mostra un&#39;immagine in modo tale che inizialmente sia completamente sfocata/di bassa qualità. Man mano che la scansione continua, diventa più chiara man mano che i dati dell&#39;immagine diventano più completamente scaricati. Questo parametro consente di impostare il numero di scansioni necessarie (3, 4 o 5) per visualizzare l’intera immagine.

`pscan=auto|3|4|5`

La velocità effettiva di ciascuna scansione dipende dalla velocità di trasmissione del sistema dell&#39;utente e del computer che riceve e decomprime i dati.

`Auto` utilizza le impostazioni di scansione calcolate dalla libreria JPEG indipendente e dipendono dal modello di colore. I valori di `3`, `4`, `5` corrispondono all&#39;impostazione di scansione trovata in Adobe Photoshop quando si salva un file JPEG come pjpeg (progressive JPEG).

Se `pscan` non è impostato, il valore predefinito è `auto`.

## Proprietà {#section-e36aa3c63a974b969d9e4f43fe5a37ab}

Attributo della richiesta. Si applica indipendentemente dall&#39;impostazione del livello corrente. Ignorato se il formato di output non è JPEG progressivo.

## Predefinito {#section-01948f6cd7a2415091004cd7526436c7}

`pscan=auto`

## Esempio {#section-d51bc4d0e8a9473786f149cba9540506}

`http://localhost:8080/is/image/demo/bedroom.tif?wid=300&fmt=pjpeg&pscan=4`

## Consultate anche {#section-2105c6441d2b42edb15c7abc4e20d7fc}

[fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a)
