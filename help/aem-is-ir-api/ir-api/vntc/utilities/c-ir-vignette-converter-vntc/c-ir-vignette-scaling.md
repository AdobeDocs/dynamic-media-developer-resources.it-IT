---
description: Sono supportati quattro tipi generali di vignette di produzione.
seo-description: Sono supportati quattro tipi generali di vignette di produzione.
seo-title: Ridimensionamento della vignetta
solution: Experience Manager
title: Ridimensionamento della vignetta
uuid: 08c8f826-7dce-4bcb-9323-4892262eb578
feature: Dynamic Media Classic, SDK/API
role: Sviluppatore, Business Practices
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '357'
ht-degree: 0%

---


# Scala vignetta{#vignette-scaling}

Sono supportati quattro tipi generali di vignette di produzione.

* Risoluzione singola

   Consigliato solo quando è certo che è necessaria una sola dimensione dell’immagine di rendering.
* Multirisoluzione

   Si consiglia quando sono note tutte le dimensioni di rendering desiderate dell&#39;immagine. Offre una qualità migliore e un rendering più rapido rispetto alle vignette a risoluzione singola e a piramide, perché l&#39;immagine non deve essere ridimensionata dopo il rendering.
* Piramide

   Ottimizzazione dello scopo, consigliata quando sono necessarie più dimensioni di immagine e le dimensioni esatte non sono predeterminate e quando si utilizza il visualizzatore zoom Dynamic Media.
* Piramide con una o più risoluzioni aggiuntive

   Offre un&#39;alta qualità per dimensioni specifiche, garantendo al contempo flessibilità e supporto ai visualizzatori zoom.

In effetti, ogni risoluzione viene salvata nella vignetta di produzione come vista indipendente con la propria larghezza e altezza dell&#39;immagine.

Le dimensioni di visualizzazione di una vignetta a risoluzione singola sono specificate con `-width` o `-height` o con entrambe. Se vengono specificati entrambi i valori, la vignetta verrà ridimensionata in modo che nessuna delle due dimensioni sia maggiore della dimensione specificata. Se non viene specificato nessuno dei due valori, la vignetta di output avrà la stessa dimensione della vignetta di input. Non sarà applicato alcun aumento; se la dimensione specificata è maggiore della dimensione della vignetta di input, la vignetta di output avrà la stessa dimensione della vignetta di input.

Le stesse regole si applicano alle vignette a risoluzione multipla, con il primo livello di risoluzione dimensionato come una vignetta a risoluzione singola. Le risoluzioni aggiuntive vengono specificate con valori separati da virgole aggiuntivi per `-width` o `-height`. Non è necessario ordinare i valori. Se `-width` specifica più valori, `-height` deve fornire un solo valore e viceversa, in caso contrario viene restituito un errore.

Viene creata una vignetta a piramide specificando `-pyramid`. Il livello di risoluzione più elevato di una vignetta di questo tipo è determinato esattamente come per una vignetta a risoluzione singola. I livelli di risoluzione aggiuntivi vengono determinati automaticamente ridimensionando ogni livello a 0,5x il livello precedente, con il livello più piccolo non superiore a 128x128 pixel.

È possibile specificare livelli di risoluzione aggiuntivi per una vignetta a piramide, come per una vignetta a più risoluzioni.
