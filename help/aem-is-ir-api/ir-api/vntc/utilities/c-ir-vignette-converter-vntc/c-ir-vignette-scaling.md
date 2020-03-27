---
description: Sono supportati quattro tipi generali di vignettatura di produzione.
seo-description: Sono supportati quattro tipi generali di vignettatura di produzione.
seo-title: Ridimensionamento vignettatura
solution: Experience Manager
title: Ridimensionamento vignettatura
topic: Scene7 Image Serving - Image Rendering API
uuid: 08c8f826-7dce-4bcb-9323-4892262eb578
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Ridimensionamento vignettatura{#vignette-scaling}

Sono supportati quattro tipi generali di vignettatura di produzione.

* Risoluzione singola

   Consigliato solo quando è certa che è necessaria una sola dimensione immagine di rendering.
* Multi-risoluzione

   Consigliato quando sono note tutte le dimensioni di immagine di rendering desiderate. Fornisce una qualità migliore e un rendering più rapido rispetto alle vignettature a risoluzione singola e a piramide, perché non è necessario ridimensionare l&#39;immagine dopo il rendering.
* Piramide

   Ideale per tutti gli usi, consigliato quando sono necessarie più dimensioni di immagine e le dimensioni esatte non sono predeterminate e quando si utilizza uno dei visualizzatori zoom Flash di Scene7.
* Piramide con una o più risoluzioni aggiuntive

   Fornisce alta qualità per dimensioni specifiche, garantendo al contempo flessibilità e supporto del visualizzatore zoom.

Ogni risoluzione viene salvata nella vignettatura di produzione come visualizzazione indipendente con larghezza e altezza dell’immagine.

Le dimensioni di visualizzazione di una vignettatura a risoluzione singola vengono specificate con `-width` o `-height` con entrambi. Se vengono specificati entrambi i valori, la vignettatura verrà ridimensionata in modo che nessuna dimensione sia maggiore della dimensione specificata. Se non viene specificato alcun valore, la vignettatura di output avrà le stesse dimensioni della vignettatura di input. Non verrà applicato alcun ingrandimento; se la dimensione specificata è maggiore della dimensione della vignettatura di input, la vignettatura di output avrà la stessa dimensione della vignettatura di input.

Le stesse regole si applicano alle vignettature a più risoluzioni, con il primo livello di risoluzione che viene ridimensionato come una vignettatura a risoluzione singola. Le risoluzioni aggiuntive vengono specificate con valori separati da virgola aggiuntivi per `-width` o `-height`. I valori non devono essere ordinati. Se `-width` specifica più valori, `-height` deve fornire solo un singolo valore, e viceversa, in caso contrario viene restituito un errore.

Per creare una vignettatura piramidale, specificate `-pyramid`. Il livello di risoluzione più elevato di una simile vignettatura è determinato esattamente come per una vignettatura a risoluzione singola. I livelli di risoluzione aggiuntivi vengono determinati automaticamente ridimensionando ogni livello a 0,5 volte il livello precedente, con il livello più piccolo non superiore a 128x128 pixel.

È possibile specificare livelli di risoluzione aggiuntivi per una vignettatura piramidale, come per una vignettatura a più risoluzioni.
