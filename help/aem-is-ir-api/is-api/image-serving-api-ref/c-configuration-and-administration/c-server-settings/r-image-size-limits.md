---
description: Utilizzare queste impostazioni del server per impostare i limiti di dimensione delle immagini.
solution: Experience Manager
title: Limiti dimensioni immagine
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 75ec58ee-8c98-46cb-96b2-79d1c32e576f
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '229'
ht-degree: 1%

---

# Limiti dimensioni immagine{#image-size-limits}

Utilizzare queste impostazioni del server per impostare i limiti di dimensione delle immagini.

## IS::MaxMessageSize - Limite dimensioni risposta {#section-bd942385d4d144cd904003695d72c85e}

Limita le dimensioni dei dati che il server immagini può inviare a [!DNL Platform Server]. Questo limita la dimensione dell&#39;immagine di risposta codificata/compressa che Image Server può restituire al client tramite HTTP (Mbyte).

## IS::MaxRenderRgnPixels - Limite dimensioni immagine di output {#section-868ceb9764dd42dfb133ffeb72f9d3fb}

Limita le dimensioni delle immagini che possono essere prodotte dal server immagini (escluse le immagini salvate su file). Valore intero maggiore di 0 in milioni di pixel. Se un’operazione di rendering supera il limite di dimensioni, viene restituito un errore. Il valore predefinito è 16.

## IS::MaxSavePixels - Limite di dimensioni per il salvataggio sui file {#section-d1547c4afa88467080ab08356f775e06}

Limita le dimensioni delle immagini che il server immagini scrive nei file con il comando `req=saveToFile`. Valore intero maggiore di 0 in milioni di pixel. Se l&#39;operazione di salvataggio del file supera tale limite, viene restituito un errore. Il valore predefinito è 100 milioni di pixel.

## IS::MaxNonDsfSize - Limite dimensioni per immagini di input non PTIFF {#section-50de28a7158a436393cce5da0d1e4d46}

Dimensione massima (in Mpixel) delle immagini che non sono file PTIFF che il server immagini può aprire. Image Server restituisce un errore quando si tenta di accedere a un’immagine non PTIFF superiore a questo limite.

>[!NOTE]
>
>Se si imposta questo valore su un valore troppo alto, la memoria del server immagini potrebbe diventare insufficiente e si potrebbero verificare errori, inclusi arresti anomali.
