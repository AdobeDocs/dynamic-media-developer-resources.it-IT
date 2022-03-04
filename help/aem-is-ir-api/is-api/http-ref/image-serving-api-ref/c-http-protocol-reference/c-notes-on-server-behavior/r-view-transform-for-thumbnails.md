---
description: L'immagine restituita al client in risposta a una richiesta req=tmb viene derivata dall'immagine composita considerando i seguenti valori wid=, hei=, attribute DefaultThumbPix e attribute MaxPix.
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

1. **Calcola la direzione di visualizzazione** - Utilizzo `wid=` o il valore della larghezza di `attribute::DefaultThumbPix` per la larghezza del rettangolo di visualizzazione. Utilizzo `hei=` o il valore dell&#39;altezza di `attribute::DefaultThumbPix` per l&#39;altezza. La direzione di visualizzazione deve essere completamente specificata in questo passaggio. (La direzione di visualizzazione è la stessa della direzione di livello 0, se non `size=`è specificato per il livello 0).
1. **Scala il composito** - Se `catalog::ThumbType=Crop`, il composito viene quindi ridimensionato fino all&#39;immagine più piccola possibile mentre si riempie ancora l&#39;intera direzione di visualizzazione; i dati immagine aggiuntivi vengono ritagliati. Se `catalog::ThumbType= Fit`quindi il composito viene scalato fino all&#39;immagine più grande possibile, mentre l&#39;intero composito viene ancora inserito nella direzione di visualizzazione. Se `catalog::ThumbType=Texture`, il composito non viene scalato per mantenere la risoluzione specificata in `catalog::ThumbRes`.
1. **Riempimento e ritaglio** - La funzione di correzione della visualizzazione è riempita con il pulsante `bgc=` colore (o, se non specificato, con `attribute::ThumbBkgColor`). Il composito in scala viene allineato con il comando di visualizzazione utilizzando l&#39;attributo: `ThumbHorizAlign` e attributo: `ThumbVertAlign`. Il composito scalato viene quindi unito al comando di visualizzazione riempito senza ulteriori ridimensionamento. Tutte le aree del composito che si estendono oltre la direzione di visualizzazione vengono ritagliate.
