---
description: Sono supportati quattro tipi generali di vignettature di produzione.
solution: Experience Manager
title: Ridimensionamento vignettatura
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: f9f92254-41d8-4d22-a168-78b49dd55478
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '335'
ht-degree: 0%

---

# Ridimensionamento vignettatura{#vignette-scaling}

Sono supportati quattro tipi generali di vignettature di produzione.

* Risoluzione singola

  Consigliato solo se si è certi che sia necessaria una sola dimensione per l&#39;immagine di rendering.
* Risoluzione multipla

  Consigliato quando si conoscono tutte le dimensioni di immagine di rendering desiderate. Offre una migliore qualità e un rendering più rapido rispetto alle vignettature a risoluzione singola e piramidali, perché non è necessario ridimensionare l’immagine dopo il rendering.
* Piramide

  La cosa migliore è che si consiglia quando sono necessarie più dimensioni di immagine e le dimensioni esatte non sono predeterminate e quando si utilizza il visualizzatore Dynamic Medie Zoom.
* Piramide con una o più risoluzioni aggiuntive

  Offre un&#39;alta qualità per dimensioni specifiche, garantendo al tempo stesso flessibilità e supporto zoom.

Ogni risoluzione viene effettivamente salvata nella vignettatura di produzione come vista indipendente con la propria larghezza e altezza dell&#39;immagine.

La dimensione di visualizzazione di una vignettatura a risoluzione singola è specificata con `-width` o `-height` o entrambi. Se vengono specificati entrambi i valori, la vignettatura viene ridimensionata in modo che nessuna delle due dimensioni superi la dimensione specificata. Se non viene specificato alcun valore, la vignettatura di output ha le stesse dimensioni della vignettatura di input. Non viene applicato alcun upscaling; se la dimensione specificata è maggiore della dimensione della vignettatura di input, la vignettatura di output ha le stesse dimensioni della vignettatura di input.

In effetti, le stesse regole si applicano alle vignettature a più risoluzioni, con il primo livello di risoluzione ridimensionato come una vignettatura a risoluzione singola. Le risoluzioni aggiuntive vengono specificate con valori separati da virgola aggiuntivi per `-width` o `-height`. Non è necessario ordinare i valori. Se `-width` specifica più valori, `-height` deve fornire un solo valore e viceversa, altrimenti viene restituito un errore.

Viene creata una vignettatura piramidale specificando `-pyramid`. Il livello di risoluzione maggiore di una vignettatura di questo tipo viene determinato esattamente come per una vignettatura a risoluzione singola. I livelli di risoluzione aggiuntivi vengono determinati automaticamente ridimensionando ogni livello a 0,5 volte rispetto al livello precedente, con il livello più piccolo che non supera 128x128 pixel.

È possibile specificare ulteriori livelli di risoluzione per una vignettatura piramidale, come per una vignettatura a più risoluzioni.
