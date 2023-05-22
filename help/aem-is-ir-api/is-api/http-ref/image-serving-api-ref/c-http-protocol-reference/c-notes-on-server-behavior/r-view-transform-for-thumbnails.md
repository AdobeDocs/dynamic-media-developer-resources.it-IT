---
description: L’immagine restituita al client in risposta a una richiesta req=tmb è derivata dall’immagine composita considerando i seguenti valori wid=, hei=, attribute DefaultThumbPix e attribute MaxPix.
solution: Experience Manager
title: Visualizza trasformazione per miniature
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 7db6736f-0b49-4c4f-89c5-e89d4752f339
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '243'
ht-degree: 0%

---

# Visualizza trasformazione per miniature{#view-transform-for-thumbnails}

L&#39;immagine restituita al client in risposta a una richiesta req=tmb viene derivata dall&#39;immagine composita considerando i seguenti valori: wid=, hei=, attribute::DefaultThumbPix e attribute::MaxPix.

1. **Calcola il rettangolo di visualizzazione** - Utilizzo `wid=` o il valore della larghezza di `attribute::DefaultThumbPix` per la larghezza del rettangolo di visualizzazione. Utilizzare `hei=` o il valore di altezza di `attribute::DefaultThumbPix` per l&#39;altezza. In questo passaggio è necessario specificare completamente il rettangolo di visualizzazione. (Si noti che il rettangolo di visualizzazione è uguale al rettangolo di livello 0, se no `size=`è specificato per il livello 0).
1. **Ridimensiona il composito** - Se `catalog::ThumbType=Crop`, quindi il composito viene ridimensionato per ottenere l’immagine più piccola possibile mentre si riempie ancora l’intero rettangolo di visualizzazione; i dati immagine aggiuntivi vengono ritagliati. Se `catalog::ThumbType= Fit`, quindi il composito viene ridimensionato per ottenere l&#39;immagine più grande possibile mentre l&#39;intero composito viene inserito nel retto di visualizzazione. Se `catalog::ThumbType=Texture`, il composito non viene ridimensionato per mantenere la risoluzione specificata in `catalog::ThumbRes`.
1. **Riempimento e ritaglio** - Il rettangolo di visualizzazione viene riempito con `bgc=` colore (o, se non specificato, con `attribute::ThumbBkgColor`). Il composito ridimensionato viene allineato con il rettangolo di visualizzazione utilizzando l&#39;attributo: `ThumbHorizAlign` Attributo e: `ThumbVertAlign`. Il composito ridimensionato viene quindi unito al rettangolo di visualizzazione riempito senza ulteriori ridimensionamenti. Tutte le aree del composito che si estendono oltre il retto della vista vengono ritagliate.
