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

---


# Visualizzare la trasformazione per le immagini{#view-transform-for-images}

L&#39;immagine restituita al client in risposta a una `req=img` richiesta viene derivata dall&#39;immagine composita considerando i seguenti valori: `wid=`, `hei=`, `fit=`, `scl=`, `rgn=`, `attribute::DefaultPix`, `attribute::MaxPix`e le dimensioni dell&#39;immagine composita.

Se `wid=` e `hei=` sono specificati, e non lo `scl=` è, l&#39;immagine composita viene ridimensionata in modo che si adatti completamente all&#39;oggetto rect della vista definito da `wid=` e `hei=`. Se le proporzioni del rect della vista sono diverse da quelle dell’immagine composita, l’immagine composita ridimensionata viene allineata all’interno del rect della vista utilizzando il `align=` valore, se specificato, oppure viene centrata in caso contrario. Qualsiasi spazio non coperto dai dati immagine viene riempito con `bgc=` o, se non specificato, con `attribute::BkgColor`.

Se `scl=` viene specificata, l&#39;immagine composita viene ridimensionata in base a tale fattore di scala. Se `wid=` e/o `hei=` viene specificato anche, l’immagine ridimensionata viene ritagliata in `wid=` base alle esigenze e/o `hei=` viene aggiunto ulteriore spazio. `align=` specifica la posizione in cui l’immagine viene ritagliata o viene aggiunto ulteriore spazio e viene riempito qualsiasi spazio aggiuntivo con `bgc=` o `attribute::BkgColor`.

Se non `wid=`vengono specificati né `hei=` né `scl=` vengono specificati né la larghezza né l’altezza dell’immagine composita superano `attribute::DefaultPix`, l’immagine composita viene ridimensionata in modo da non superare `attribute::DefaultPix`. In caso contrario, l&#39;immagine composita viene utilizzata senza ridimensionamento.

Per garantire che l’immagine di visualizzazione venga restituita senza ulteriore ridimensionamento, specificate `scl=1`.

Se `rgn=` viene specificato, l&#39;immagine della risposta viene ritagliata di conseguenza per ottenere la dimensione finale dell&#39;immagine della risposta. Questa dimensione viene confrontata con `attribute::MaxPix` (se definita) e viene generato un errore se l&#39;immagine di risposta è più grande in una delle due dimensioni.

Se `fmt=` specifica i dati senza alfa, tutte le aree trasparenti nell&#39;immagine di risposta vengono riempite con `bgc=` o `attribute::BkgColor`.
