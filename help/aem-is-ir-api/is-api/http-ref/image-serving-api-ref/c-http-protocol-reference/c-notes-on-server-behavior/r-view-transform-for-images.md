---
description: Trasformazione di visualizzazione per immagini
solution: Experience Manager
title: Trasformazione di visualizzazione per immagini
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: fc20cbc2-9d66-4c52-80c2-9ba7c3b54744
TQID: 'https://experienceleague.adobe.com/PPSeNhcaJ4Nx8ojXOt9vqJFp7F9NGo4LO3UxdLKzmwo'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 271
ht-degree: 0%

---

# Trasformazione di visualizzazione per immagini{#view-transform-for-images}

L&#39;immagine restituita al client in risposta a una richiesta `req=img` è derivata dall&#39;immagine composita considerando i valori seguenti: `wid=`, `hei=`, `fit=`, `scl=`, `rgn=`, `attribute::DefaultPix`, `attribute::MaxPix` e le dimensioni dell&#39;immagine composita.

Se sono specificati `wid=` e `hei=` e `scl=` non lo è, l&#39;immagine composita viene ridimensionata in modo da rientrare completamente nel retto di visualizzazione definito da `wid=` e `hei=`. Se le proporzioni del rettangolo di visualizzazione sono diverse da quelle dell&#39;immagine composita, l&#39;immagine composita ridimensionata viene allineata all&#39;interno del rettangolo di visualizzazione utilizzando il valore `align=`, se specificato, oppure viene centrata in altro modo. Qualsiasi spazio non coperto dai dati immagine è riempito con `bgc=` o, se non specificato, con `attribute::BkgColor`.

Se si specifica `scl=`, l&#39;immagine composita verrà ridimensionata in base al fattore di scala specificato. Se si specificano anche `wid=` e/o `hei=`, l&#39;immagine ridimensionata viene ritagliata a `wid=` e/o viene aggiunto `hei=` o ulteriore spazio, in base alle esigenze. `align=` specifica dove viene ritagliata l&#39;immagine o aggiunto spazio aggiuntivo e qualsiasi spazio aggiuntivo viene riempito con `bgc=` o `attribute::BkgColor`.

Se non si specificano né `wid=`, `hei=` né `scl=` e se la larghezza o l&#39;altezza dell&#39;immagine composita supera `attribute::DefaultPix`, l&#39;immagine composita viene ridimensionata in modo da non superare `attribute::DefaultPix`. In caso contrario, l&#39;immagine composita viene utilizzata senza ridimensionamento.

Per garantire che l&#39;immagine della visualizzazione venga restituita senza ulteriori ridimensionamenti, specificare `scl=1`.

Se si specifica `rgn=`, l&#39;immagine di risposta viene ritagliata di conseguenza in modo da ottenere la dimensione dell&#39;immagine di risposta finale. Questa dimensione viene confrontata con `attribute::MaxPix` (se definito) e viene generato un errore se l&#39;immagine di risposta è più grande in una delle dimensioni.

Se `fmt=` specifica dati senza alfa, tutte le aree trasparenti nell&#39;immagine di risposta saranno riempite con `bgc=` o `attribute::BkgColor`.
