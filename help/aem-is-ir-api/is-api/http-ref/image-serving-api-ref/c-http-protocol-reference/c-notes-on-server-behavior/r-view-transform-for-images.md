---
description: 'null'
seo-description: 'null'
seo-title: Visualizzare la trasformazione per le immagini
solution: Experience Manager
title: Visualizzare la trasformazione per le immagini
topic: Scene7 Image Serving - Image Rendering API
uuid: 8594f746-0e58-4a59-933c-a44dc0b06c25
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '273'
ht-degree: 0%

---


# Visualizza trasformazione per immagini{#view-transform-for-images}

L&#39;immagine restituita al client in risposta a una richiesta `req=img` viene derivata dall&#39;immagine composita, considerando i seguenti valori: `wid=`, `hei=`, `fit=`, `scl=`, `rgn=`, `attribute::DefaultPix`, `attribute::MaxPix` e le dimensioni dell&#39;immagine composita.

Se sono specificati `wid=` e `hei=` e `scl=` non lo è, l&#39;immagine composita viene ridimensionata in modo che si adatti completamente all&#39;interno del rect di visualizzazione definito da `wid=` e `hei=`. Se le proporzioni del recto della vista sono diverse da quelle dell&#39;immagine composita, l&#39;immagine composita ridimensionata viene allineata all&#39;interno del rect della vista utilizzando il valore `align=`, se specificato, oppure viene centrata in caso contrario. Qualsiasi spazio non coperto dai dati immagine viene riempito con `bgc=` o, se non specificato, con `attribute::BkgColor`.

Se si specifica `scl=`, l&#39;immagine composita viene ridimensionata in base a tale fattore di scala. Se si specifica anche `wid=` e/o `hei=`, l&#39;immagine ridimensionata viene ritagliata fino a `wid=` e/o `hei=` oppure viene aggiunto spazio, se necessario. `align=` specifica la posizione in cui l’immagine viene ritagliata o viene aggiunto ulteriore spazio e viene riempito qualsiasi spazio aggiuntivo con  `bgc=` o  `attribute::BkgColor`.

Se non vengono specificati né `wid=`, `hei=` né `scl=`, e se la larghezza o l&#39;altezza dell&#39;immagine composita supera `attribute::DefaultPix`, l&#39;immagine composita viene ridimensionata in modo da non superare `attribute::DefaultPix`. In caso contrario, l&#39;immagine composita viene utilizzata senza ridimensionamento.

Per garantire che l&#39;immagine di visualizzazione venga restituita senza ulteriore ridimensionamento, specificate `scl=1`.

Se si specifica `rgn=`, l&#39;immagine di risposta viene ritagliata di conseguenza per ottenere la dimensione finale dell&#39;immagine di risposta. Questa dimensione viene confrontata con `attribute::MaxPix` (se definita) e viene generato un errore se l&#39;immagine di risposta è più grande in una delle due dimensioni.

Se `fmt=` specifica i dati senza alfa, tutte le aree trasparenti nell&#39;immagine di risposta vengono riempite con `bgc=` o `attribute::BkgColor`.
