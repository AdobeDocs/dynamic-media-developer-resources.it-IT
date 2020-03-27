---
description: Sono supportati quattro tipi di livelli.
seo-description: Sono supportati quattro tipi di livelli.
seo-title: Tipi di livelli
solution: Experience Manager
title: Tipi di livelli
topic: Scene7 Image Serving - Image Rendering API
uuid: d88b2163-7c9f-4885-9722-be3339e7127a
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Tipi di livelli{#layer-types}

Sono supportati quattro tipi di livelli.

## Livelli immagine {#section-3e53df1437694272aca03f927fc0db07}

I livelli immagine devono avere un `src=` comando che specifica l’immagine da usare come livello. È possibile specificare un’immagine separata con cui `mask=` utilizzarla come maschera di livello oppure l’immagine potrebbe avere già un canale alfa. Le dimensioni dei livelli immagine vengono sempre derivate dall’immagine, ma l’immagine viene spesso ridimensionata in base al `size=` comando. È possibile applicare un percorso di clip con `clipPath=`.

## Livelli di testo {#section-dc2aec6416a340bcb20c1f884323c8d0}

Deve disporre di un `text=` comando o `textPs=` che fornisca il contenuto di testo sotto forma di frammento di testo in formato RTF. I livelli di testo possono ridimensionarsi autonomamente in base al contenuto, oppure possono avere dimensioni esplicite (ad esempio, se il testo deve essere racchiuso in una larghezza specifica o se il testo deve essere vincolato all’interno di un’area specifica). `textPs=` supporta lo scorrimento del testo in forme arbitrarie definite con `textFlowPath=` e su tracciati arbitrari definiti con `textPath=`. `textPs=` supporta anche il rendering del testo nella casella di testo o nella forma specificata ad angoli arbitrari ( `textAngle=`).

## Livelli in tinta unita {#section-56dfb672756643dda08dc93294809eb0}

I livelli in tinta unita vengono spesso utilizzati per il livello 0 nei modelli, in modo che le dimensioni dell’immagine composita siano fisse e indipendenti da qualsiasi contenuto dell’immagine. I livelli a colori pieni richiedono un `color=` attributo `size=` o `mask=`, e supportano la maggior parte degli altri comandi e attributi per modificare l’aspetto. Ai livelli a colori pieni possono essere date forme arbitrarie con `clipPath=`.

## Livelli effetto {#section-dd3b628bc6734077af4c0ddcebcee05f}

Gli effetti di livello in stile Photoshop, come le ombre esterne e gli effetti di bagliore, vengono implementati da IS utilizzando appositi livelli secondari che possono essere collegati a livelli di immagine, testo e tinta unita. Questi livelli di effetto ereditano la maschera e la posizione del livello principale dal livello principale e hanno funzionalità limitate.
