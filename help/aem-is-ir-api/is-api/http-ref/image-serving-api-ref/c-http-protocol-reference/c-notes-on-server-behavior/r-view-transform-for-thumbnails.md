---
description: L'immagine restituita al client in risposta a una richiesta req=tmb viene derivata dall'immagine composita considerando i seguenti valori wid=, hei=, attribute DefaultThumbPix e attribute MaxPix.
seo-description: L'immagine restituita al client in risposta a una richiesta req=tmb viene derivata dall'immagine composita considerando i seguenti valori wid=, hei=, attribute DefaultThumbPix e attribute MaxPix.
seo-title: Visualizza trasformazione per miniature
solution: Experience Manager
title: Visualizza trasformazione per miniature
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 29924bc1-ada1-420f-aef7-bf9a7db7065b
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '279'
ht-degree: 0%

---


# Visualizza trasformazione per miniature{#view-transform-for-thumbnails}

L&#39;immagine restituita al client in risposta a una richiesta req=tmb viene derivata dall&#39;immagine composita, considerando i seguenti valori: wid=, hei=, attribute::DefaultThumbPix e attribute::MaxPix.

1. **Calcola il rect**  della vista - Utilizza  `wid=` o il valore della larghezza  `attribute::DefaultThumbPix` per la larghezza del rect della vista. Utilizzare `hei=` o il valore di altezza di `attribute::DefaultThumbPix` per l&#39;altezza. In questo passaggio è necessario specificare completamente il rect della vista. Tenete presente che il rect della vista sarà lo stesso del rect del livello 0, se per il livello 0 non è specificato alcun valore `size=`.
1. **Scala il composto**  - Se  `catalog::ThumbType=Crop`, il composto viene ridimensionato al più piccolo possibile mentre riempie l&#39;intero recto della vista; i dati immagine aggiuntivi vengono ritagliati. Se `catalog::ThumbType= Fit`, il composito viene ridimensionato in scala fino all&#39;immagine più grande possibile mentre l&#39;intero composito viene adattato al recto della vista. Se `catalog::ThumbType=Texture`, il composito non viene ridimensionato per mantenere la risoluzione specificata in `catalog::ThumbRes`.
1. **Riempimento e ritaglio**  - Il rettangolo di visualizzazione viene riempito con il  `bgc=` colore (o, se non specificato, con  `attribute::ThumbBkgColor`). Il composito ridimensionato è allineato con il rect della vista utilizzando l&#39;attributo: `ThumbHorizAlign` e attribute: `ThumbVertAlign`. Il composito ridimensionato viene quindi unito al rect della vista riempita senza ulteriore ridimensionamento. Vengono ritagliate tutte le aree del composito che si estendono oltre il recto della vista.

