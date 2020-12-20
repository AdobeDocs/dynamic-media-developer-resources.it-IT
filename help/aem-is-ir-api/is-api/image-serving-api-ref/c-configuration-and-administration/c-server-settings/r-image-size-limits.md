---
description: Usate queste impostazioni del server per impostare i limiti di dimensione immagine.
seo-description: Usate queste impostazioni del server per impostare i limiti di dimensione immagine.
seo-title: Limiti dimensione immagine
solution: Experience Manager
title: Limiti dimensione immagine
topic: Scene7 Image Serving - Image Rendering API
uuid: 6736e652-c495-45a2-bdd2-9975f99af0a2
translation-type: tm+mt
source-git-commit: e8e5b07329bde3e23ee095d5022da62d67e9478c
workflow-type: tm+mt
source-wordcount: '241'
ht-degree: 0%

---


# Limiti dimensione immagine{#image-size-limits}

Usate queste impostazioni del server per impostare i limiti di dimensione immagine.

## IS::MaxMessageSize - Limite dimensioni risposta {#section-bd942385d4d144cd904003695d72c85e}

Limita la dimensione dei dati che il server immagini può inviare al server della piattaforma. In effetti, questo limita le dimensioni dell’immagine di risposta codificata/compressa che Image Server può restituire al client tramite HTTP (Mbyte).

## IS::MaxRenderRongPixels - Limite dimensione immagine di output {#section-868ceb9764dd42dfb133ffeb72f9d3fb}

Limita le dimensioni delle immagini che il server immagini può produrre (escluse le immagini salvate in un file). Valore intero maggiore di 0 in milioni di pixel. Viene restituito un errore se un&#39;operazione di rendering supera il limite di dimensioni. Il valore predefinito è 16.

## IS::MaxSavePixels - Limite dimensione per il salvataggio in file {#section-d1547c4afa88467080ab08356f775e06}

Limita le dimensioni delle immagini che il server immagini scriverà nei file con il comando `req=saveToFile`. Valore intero maggiore di 0 in milioni di pixel. Se l&#39;operazione di salvataggio del file supera tale limite, viene restituito un errore. Il valore predefinito è 100 milioni di pixel.

## IS::MaxNonDsfSize - Limite dimensione per immagini di input non PTIFF {#section-50de28a7158a436393cce5da0d1e4d46}

La dimensione massima (in pixel) delle immagini che non sono PTIFF che il server immagini può aprire. Image Server restituisce un errore quando si tenta di accedere a un&#39;immagine non PTIFF maggiore di questo limite.

>[!NOTE]
>
>Se si imposta questo valore su un valore troppo alto, la memoria del server immagini potrebbe perdere di vista e si potrebbero verificare degli errori, compresi gli arresti anomali.

