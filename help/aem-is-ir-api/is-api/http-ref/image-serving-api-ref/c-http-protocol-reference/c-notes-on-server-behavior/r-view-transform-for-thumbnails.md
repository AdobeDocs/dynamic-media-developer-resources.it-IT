---
description: L’immagine restituita al client in risposta a una richiesta req=tmb è derivata dall’immagine composita considerando i seguenti valori wid=, hei=, attribute DefaultThumbPix e attribute MaxPix.
solution: Experience Manager
title: Visualizza trasformazione per miniature
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 7db6736f-0b49-4c4f-89c5-e89d4752f339
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '245'
ht-degree: 0%

---

# Visualizza trasformazione per miniature{#view-transform-for-thumbnails}

L&#39;immagine restituita al client in risposta a una richiesta req=tmb viene derivata dall&#39;immagine composita considerando i seguenti valori: wid=, hei=, attribute::DefaultThumbPix e attribute::MaxPix.

1. **Calcolare il retto di visualizzazione**. Utilizzare `wid=` o il valore di larghezza `attribute::DefaultThumbPix` per la larghezza del retto di visualizzazione. Utilizzare `hei=` o il valore di altezza `attribute::DefaultThumbPix` per l&#39;altezza. In questo passaggio è necessario specificare completamente il rettangolo di visualizzazione. Si noti che il retto di visualizzazione è uguale al retto di livello 0, se non è specificato alcun `size=` per il livello 0.
1. **Ridimensiona il composito** - Se `catalog::ThumbType=Crop`, il composito viene ridimensionato alla più piccola immagine possibile durante il riempimento dell&#39;intero rettangolo di visualizzazione; i dati immagine in eccesso vengono ritagliati. Se `catalog::ThumbType= Fit`, il composito viene ridimensionato per ottenere la più grande immagine possibile mentre l&#39;intero composito viene ancora adattato al rettangolo di visualizzazione. Se `catalog::ThumbType=Texture`, il composito non viene ridimensionato per mantenere la risoluzione specificata in `catalog::ThumbRes`.
1. **Riempimento e ritaglio** - Il rettangolo di visualizzazione è riempito con il colore `bgc=` (o, se non specificato, con `attribute::ThumbBkgColor`). Il composito ridimensionato è allineato con il rettangolo di visualizzazione utilizzando l&#39;attributo: `ThumbHorizAlign` e l&#39;attributo: `ThumbVertAlign`. Il composito ridimensionato viene quindi unito al rettangolo di visualizzazione riempito senza ulteriori ridimensionamenti. Tutte le aree del composito che si estendono oltre il retto della vista vengono ritagliate.
