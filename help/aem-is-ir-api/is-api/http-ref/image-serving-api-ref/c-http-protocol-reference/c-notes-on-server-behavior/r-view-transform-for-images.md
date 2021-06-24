---
description: Visualizza trasformazione per immagini
solution: Experience Manager
title: Visualizza trasformazione per immagini
feature: Dynamic Media Classic, SDK/API
role: Developer,Business Practitioner
exl-id: fc20cbc2-9d66-4c52-80c2-9ba7c3b54744
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '276'
ht-degree: 0%

---

# Visualizza trasformazione per immagini{#view-transform-for-images}

L&#39;immagine restituita al client in risposta a una richiesta `req=img` viene derivata dall&#39;immagine composita considerando i seguenti valori: `wid=`, `hei=`, `fit=`, `scl=`, `rgn=`, `attribute::DefaultPix`, `attribute::MaxPix` e le dimensioni dell&#39;immagine composita.

Se sono specificati `wid=` e `hei=` e `scl=` non lo è, l&#39;immagine composita viene ridimensionata in modo che si adatti completamente al campo di visualizzazione definito da `wid=` e `hei=`. Se le proporzioni della direzione di visualizzazione sono diverse da quelle dell&#39;immagine composita, l&#39;immagine composita in scala viene allineata all&#39;interno della direzione di visualizzazione utilizzando il valore `align=`, se specificato, o viene centrata in altro modo. Qualsiasi spazio non coperto dai dati immagine viene riempito con `bgc=` o, se non specificato, con `attribute::BkgColor`.

Se si specifica `scl=`, l&#39;immagine composita viene ridimensionata in base a tale fattore di scala. Se è specificato anche `wid=` e/o `hei=`, l&#39;immagine in scala viene ritagliata su `wid=` e/o `hei=` oppure viene aggiunto spazio aggiuntivo, a seconda delle necessità. `align=` specifica la posizione in cui l’immagine viene ritagliata o viene aggiunto spazio aggiuntivo e viene riempito qualsiasi spazio aggiuntivo con  `bgc=` o  `attribute::BkgColor`.

Se non sono specificati né `wid=`, `hei=` né `scl=` e se la larghezza o l&#39;altezza dell&#39;immagine composita supera `attribute::DefaultPix`, l&#39;immagine composita viene ridimensionata in modo da non superare `attribute::DefaultPix`. In caso contrario, l&#39;immagine composita viene utilizzata senza ridimensionamento.

Per garantire che l&#39;immagine di visualizzazione venga restituita senza ulteriore ridimensionamento, specificare `scl=1`.

Se si specifica `rgn=`, l&#39;immagine di risposta viene ritagliata di conseguenza per arrivare alla dimensione finale dell&#39;immagine di risposta. Questa dimensione viene confrontata con `attribute::MaxPix` (se definita) e viene generato un errore se l&#39;immagine di risposta è più grande in una delle due dimensioni.

Se `fmt=` specifica i dati senza alfa, tutte le aree trasparenti nell&#39;immagine di risposta vengono riempite con `bgc=` o `attribute::BkgColor`.
