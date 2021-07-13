---
description: L'immagine restituita al client in risposta a una richiesta req=tmb viene derivata dall'immagine composita considerando i seguenti valori wid=, hei=, attribute DefaultThumbPix e attribute MaxPix.
solution: Experience Manager
title: Visualizza trasformazione per miniature
feature: Dynamic Media Classic, SDK/API
role: Developer,User
exl-id: 7db6736f-0b49-4c4f-89c5-e89d4752f339
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '249'
ht-degree: 0%

---

# Visualizza trasformazione per miniature{#view-transform-for-thumbnails}

L&#39;immagine restituita al client in risposta a una richiesta req=tmb viene derivata dall&#39;immagine composita considerando i seguenti valori: wid=, hei=, attribute::DefaultThumbPix e attribute::MaxPix.

1. **Calcola la direzione di visualizzazione** : utilizza  `wid=` o il valore della larghezza di  `attribute::DefaultThumbPix` per la larghezza della direzione di visualizzazione. Utilizzare `hei=` o il valore dell&#39;altezza di `attribute::DefaultThumbPix` per l&#39;altezza. La direzione di visualizzazione deve essere completamente specificata in questo passaggio. (Se non è specificato alcun valore `size=`per il livello 0, la direzione di visualizzazione sarà la stessa del parametro di livello 0).
1. **Scala il composito**  - Se  `catalog::ThumbType=Crop`, il composito viene scalato fino all&#39;immagine più piccola possibile mentre si riempie ancora l&#39;intera direzione di visualizzazione; i dati immagine aggiuntivi vengono ritagliati. Se `catalog::ThumbType= Fit`, il composito viene ridimensionato in base all&#39;immagine più grande possibile, mantenendo l&#39;intero composito nella direzione di visualizzazione. Se `catalog::ThumbType=Texture`, il composito non viene scalato per mantenere la risoluzione specificata in `catalog::ThumbRes`.
1. **Riempimento e ritaglio**  - Il rettangolo di visualizzazione viene riempito con il  `bgc=` colore (o, se non specificato, con  `attribute::ThumbBkgColor`). Il composito in scala viene allineato con il comando di visualizzazione utilizzando l&#39;attributo: `ThumbHorizAlign` e attributo: `ThumbVertAlign`. Il composito scalato viene quindi unito al comando di visualizzazione riempito senza ulteriori ridimensionamento. Tutte le aree del composito che si estendono oltre la direzione di visualizzazione vengono ritagliate.
