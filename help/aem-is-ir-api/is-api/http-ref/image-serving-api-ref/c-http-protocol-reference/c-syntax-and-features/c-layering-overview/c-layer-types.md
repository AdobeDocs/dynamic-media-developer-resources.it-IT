---
description: Sono supportati quattro tipi di livelli.
solution: Experience Manager
title: Tipi di livelli
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 9819a73d-1108-414a-831f-37ba94c3feb9
TQID: 'https://experienceleague.adobe.com/F2ZE-uepvnDVG2OImJIzXm44Wm3KLYfLZrBnk11tE6I'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 283
ht-degree: 0%

---

# Tipi di livelli{#layer-types}

Sono supportati quattro tipi di livelli.

## Livelli immagine {#section-3e53df1437694272aca03f927fc0db07}

I livelli immagine devono avere un comando `src=` che specifichi l&#39;immagine da utilizzare come livello. È possibile specificare un&#39;immagine separata con `mask=` da utilizzare come maschera di livello oppure l&#39;immagine potrebbe avere già un canale alfa. La dimensione dei livelli immagine è sempre derivata dall&#39;immagine, ma l&#39;immagine viene spesso ridimensionata utilizzando il comando `size=`. È possibile applicare un percorso di clip con `clipPath=`.

## Livelli di testo {#section-dc2aec6416a340bcb20c1f884323c8d0}

Deve avere un comando `text=` o `textPs=` che fornisce il contenuto di testo sotto forma di frammento di testo RTF (Rich Text Formatted). I livelli di testo possono avere dimensioni autonome rispetto al contenuto o possono avere dimensioni esplicite. Ad esempio, se il testo deve essere racchiuso in una larghezza specifica o se deve essere vincolato all&#39;interno di un&#39;area specifica. `textPs=` supporta il flusso di testo in forme arbitrarie definite con `textFlowPath=` e in percorsi arbitrari definiti con `textPath=`. `textPs=` supporta anche il rendering del testo nella casella di testo o nella forma specificata con angoli arbitrari ( `textAngle=`).

## Livelli di colore pieno {#section-56dfb672756643dda08dc93294809eb0}

I livelli a colori solidi vengono spesso utilizzati per il livello 0 nei modelli, in modo che le dimensioni dell&#39;immagine composita siano fisse e indipendenti da qualsiasi contenuto di immagine. I livelli a colori a tinta unita richiedono un attributo `color=` e `size=` o `mask=` e supportano la maggior parte degli altri comandi e attributi per modificare l&#39;aspetto. Ai livelli di colore pieno possono essere assegnate forme arbitrarie con `clipPath=`.

## Livelli degli effetti {#section-dd3b628bc6734077af4c0ddcebcee05f}

Gli effetti di livello in stile Photoshop, come le ombre esterne e gli effetti bagliore, vengono implementati da IS utilizzando speciali sottolivelli che possono essere attaccati ai livelli immagine, testo e colore a tinta unita. Questi livelli di effetto ereditano la maschera e la posizione del livello padre dal livello padre e sono limitati in termini di funzionalità.
