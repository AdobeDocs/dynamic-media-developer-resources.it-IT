---
description: Trasformazione di visualizzazione per immagini
solution: Experience Manager
title: Trasformazione di visualizzazione per immagini
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: fc20cbc2-9d66-4c52-80c2-9ba7c3b54744
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '271'
ht-degree: 0%

---

# Trasformazione di visualizzazione per immagini{#view-transform-for-images}

L&#39;immagine restituita al client in risposta a un `req=img` La richiesta viene derivata dall’immagine composita considerando i seguenti valori: `wid=`, `hei=`, `fit=`, `scl=`, `rgn=`, `attribute::DefaultPix`, `attribute::MaxPix`e le dimensioni dell&#39;immagine composita.

Se `wid=` e `hei=` sono specificati, e `scl=` non è, l&#39;immagine composita viene ridimensionata in modo da rientrare completamente nel retto di visualizzazione definito da `wid=` e `hei=`. Se le proporzioni del rettangolo di visualizzazione sono diverse da quelle dell&#39;immagine composita, l&#39;immagine composita ridimensionata viene allineata all&#39;interno del rettangolo di visualizzazione utilizzando `align=` valore, se specificato, oppure centrato altrimenti. Qualsiasi spazio non coperto dai dati immagine viene riempito con `bgc=` o, se non specificato, con `attribute::BkgColor`.

Se `scl=` L&#39;immagine composita viene ridimensionata in base al fattore di scala specificato. Se `wid=` e/o `hei=` viene specificata anche, l&#39;immagine ridimensionata viene quindi ritagliata in `wid=` e/o `hei=` oppure viene aggiunto ulteriore spazio, in base alle esigenze. `align=` specifica dove viene ritagliata l&#39;immagine o viene aggiunto spazio aggiuntivo e viene riempito con `bgc=` o `attribute::BkgColor`.

Se nessuno dei due `wid=`, `hei=` né `scl=` e se la larghezza o l&#39;altezza dell&#39;immagine composita supera `attribute::DefaultPix`, l&#39;immagine composita viene ridimensionata in modo da non superare `attribute::DefaultPix`. In caso contrario, l&#39;immagine composita viene utilizzata senza ridimensionamento.

Per garantire che l&#39;immagine della vista venga restituita senza ulteriori ridimensionamenti, specificate `scl=1`.

Se `rgn=` viene specificata, l’immagine di risposta viene quindi ritagliata di conseguenza per arrivare alle dimensioni finali dell’immagine di risposta. Questa dimensione viene confrontata con `attribute::MaxPix` (se definita), e viene generato un errore se l’immagine di risposta è più grande in una delle dimensioni.

Se `fmt=` specifica i dati senza alfa, tutte le aree trasparenti nell&#39;immagine di risposta vengono riempite con `bgc=` o `attribute::BkgColor`.
