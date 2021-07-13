---
description: Utilizza queste impostazioni del server per impostare i limiti di dimensione dell'immagine.
solution: Experience Manager
title: Limiti delle dimensioni dell'immagine
feature: Dynamic Media Classic, SDK/API
role: Developer,Administrator,User
exl-id: 75ec58ee-8c98-46cb-96b2-79d1c32e576f
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '234'
ht-degree: 0%

---

# Limiti delle dimensioni dell&#39;immagine{#image-size-limits}

Utilizza queste impostazioni del server per impostare i limiti di dimensione dell&#39;immagine.

## IS::MaxMessageSize - Limite dimensione risposta {#section-bd942385d4d144cd904003695d72c85e}

Limita le dimensioni dei dati che il server immagini può inviare al server Platform. In effetti, questo limita le dimensioni dell&#39;immagine di risposta codificata/compressa che Image Server può restituire al client tramite HTTP (Mbyte).

## IS::MaxRenderRngPixels - Limite dimensione immagine in uscita {#section-868ceb9764dd42dfb133ffeb72f9d3fb}

Limita le dimensioni delle immagini che il server di immagini può produrre (escluse le immagini salvate nel file). Valore intero maggiore di 0 in milioni di pixel. Se un’operazione di rendering supera il limite di dimensioni, viene restituito un errore. Il valore predefinito è 16.

## IS::MaxSavePixels - Limite di dimensioni per il salvataggio in file {#section-d1547c4afa88467080ab08356f775e06}

Limita le dimensioni delle immagini che il server di immagini scriverà nei file con il comando `req=saveToFile`. Valore intero maggiore di 0 in milioni di pixel. Se l’operazione di salvataggio del file supera tale limite, viene restituito un errore. Il valore predefinito è 100 milioni di pixel.

## IS::MaxNonDsfSize - Limite di dimensioni per le immagini in ingresso non PTIFF {#section-50de28a7158a436393cce5da0d1e4d46}

Dimensione massima (in Mpixel) delle immagini che non sono PTIFF che il server di immagini può aprire. Image Serving restituisce un errore quando si tenta di accedere a un&#39;immagine non PTIFF maggiore di questo limite.

>[!NOTE]
>
>Se si imposta questo valore su un valore troppo alto, la memoria del server di immagini potrebbe essere ridotta e si potrebbero verificare errori, compresi arresti anomali.
