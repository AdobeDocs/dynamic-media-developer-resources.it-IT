---
description: Sono supportati quattro tipi di livelli.
solution: Experience Manager
title: Tipi di livelli
feature: Dynamic Media Classic, SDK/API
role: Developer,Business Practitioner
exl-id: 9819a73d-1108-414a-831f-37ba94c3feb9
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '282'
ht-degree: 0%

---

# Tipi di livelli{#layer-types}

Sono supportati quattro tipi di livelli.

## Livelli immagine {#section-3e53df1437694272aca03f927fc0db07}

I livelli immagine devono avere un comando `src=` che specifica l’immagine da utilizzare come livello. È possibile specificare un&#39;immagine separata con `mask=` da utilizzare come maschera di livello oppure l&#39;immagine potrebbe avere già un canale alfa. Le dimensioni dei livelli immagine vengono sempre derivate dall&#39;immagine, ma l&#39;immagine viene spesso ridimensionata per adattarsi utilizzando il comando `size=` . Un percorso di clip può essere applicato con `clipPath=`.

## Livelli di testo {#section-dc2aec6416a340bcb20c1f884323c8d0}

Deve essere presente un comando `text=` o `textPs=` che fornisce il contenuto del testo sotto forma di un frammento di testo in formato RTF. I livelli di testo possono ridimensionarsi autonomamente in base al contenuto o possono avere dimensioni esplicite (ad esempio, se il testo deve essere racchiuso in una larghezza specifica o se il testo deve essere vincolato all’interno di un’area specifica). `textPs=` supporta lo scorrimento del testo in forme arbitrarie definite con  `textFlowPath=` e su percorsi arbitrari definiti con  `textPath=`. `textPs=` supporta anche il rendering del testo nella casella di testo o nella forma specificata ad angoli arbitrari (  `textAngle=`).

## Livelli in tinta unita {#section-56dfb672756643dda08dc93294809eb0}

I livelli a colori solidi vengono spesso utilizzati per il livello 0 nei modelli, in modo che le dimensioni dell&#39;immagine composita siano fisse e indipendenti da qualsiasi contenuto dell&#39;immagine. I livelli a colori solidi richiedono un attributo `color=` e `size=` o `mask=` e supportano la maggior parte degli altri comandi e attributi per modificare l&#39;aspetto. Gli strati a colori solidi possono essere oggetto di forme arbitrarie con `clipPath=`.

## Livelli di effetto {#section-dd3b628bc6734077af4c0ddcebcee05f}

Gli effetti di livello in stile Photoshop, come le ombre di goccia e gli effetti di bagliore, sono implementati da IS utilizzando sottolivelli speciali che possono essere collegati a livelli di immagine, testo e colore solido. Questi livelli di effetto ereditano la maschera e la posizione del livello padre dal livello padre e hanno funzionalità limitate.
