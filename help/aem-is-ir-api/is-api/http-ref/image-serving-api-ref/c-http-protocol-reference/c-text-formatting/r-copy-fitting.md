---
description: textPs= implementa un algoritmo proprietario di adattamento alla copia che regola automaticamente le dimensioni del carattere per riempire in modo ottimale l'area di testo con del testo, riducendo al minimo lo spazio aggiuntivo nella parte inferiore evitando al contempo l'overflow.
solution: Experience Manager
title: Adattamento copia
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: d1a560f3-f92c-4143-b80a-e1674c8a4207
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '519'
ht-degree: 0%

---

# Adattamento copia{#copy-fitting}

textPs= implementa un algoritmo proprietario di adattamento alla copia che regola automaticamente le dimensioni del carattere per riempire in modo ottimale l&#39;area di testo con del testo, riducendo al minimo lo spazio aggiuntivo nella parte inferiore evitando al contempo l&#39;overflow.

L’adattamento può essere attivato e controllato collettivamente per l’intero livello di testo, a livello di paragrafo, anche per un singolo intervallo di testo.

Specifica la dimensione minima del font con `\fs` e la dimensione massima del font con `\copyfit`. Qualsiasi numero di intervalli è consentito nella stessa stringa RTF. Le dimensioni di tutti gli intervalli sono diverse in modo proporzionale, garantendo il mantenimento dei rapporti desiderati sulle dimensioni del font.

`\copyfit` è considerato un comando di formattazione dei caratteri e ha regole di ambito come `\fs` e `\b`.

L&#39;adattamento della copia è disattivato specificando `\copyfit` con una dimensione uguale o inferiore alla dimensione specificata con `\fs`.

## Limitazione del numero di righe {#section-e5aee0f039e04842afc3d6884ed681ac}

Oltre a specificare l’intervallo delle dimensioni dei font, il comportamento dell’algoritmo di adattamento alla copia può essere ulteriormente controllato con il `\copyfitlines` o `\copyfitmaxlines` , che limitano il numero di righe che l&#39;algoritmo genererà. Entrambi i comandi accettano un parametro di conteggio delle righe o 0, per non limitare il numero di righe nell&#39;area copiata.

`\copyfitlines` consente l’overflow del testo su righe aggiuntive quando non rientra nel numero di righe specificato. Le interruzioni di riga esplicite nel segmento di testo da copiare vengono sempre rispettate.

`\copyfitmaxlines` tronca sempre le linee di output aggiuntive che superano il limite specificato. Il numero specificato di linee non verrà mai superato, anche se sono presenti interruzioni di riga esplicite. Per questa versione di Image Serving, non più di N-1 `\line` possono essere presenti indicatori nell&#39;intervallo di testo adattato in copia. Il comportamento non è definito se questo limite viene superato.

## Esempi {#section-f4ddbbfade444560be30a813d90c2c1b}

Gli esempi seguenti presuppongono che i corpi di testo siano forniti con variabili denominate *[!DNL $A$]*, *[!DNL $B$]* e *[!DNL $C$]*.

**Mantenere lo stesso rapporto tra le dimensioni dei font in tutto l’intervallo:**

`{\fs10\copyfit100 $A${\fs20\copyfit200 $B$}$C$}`

*[!DNL $B$]* viene sempre eseguito il rendering di dimensioni due volte superiori al resto del testo. Quando viene specificato molto testo, *[!DNL $A$]* e *[!DNL $C$]* viene eseguito il rendering con `\fs10` e *[!DNL $B$]* con `\fs20`. Con poco testo, *[!DNL $A$]* e *[!DNL $C$]* utilizzerà `\fs100` e *[!DNL $B$]* `\fs200`.

**Converti in un font di grandi dimensioni comune se viene disegnata solo una piccola quantità di testo:**

`{\copyfit100\fs10 $A${\fs20 $B$}$C$}`

All&#39;estremità più piccola dell&#39;intervallo, *[!DNL $B$]* viene eseguito il rendering con `\fs20`, due volte più grande *[!DNL $A$]* e *[!DNL $C$]* a `\fs10`. Tutto il testo è disegnato in `\fs100` (50 punti) all&#39;estremità opposta dell&#39;intervallo.

**Converti in un font piccolo comune se si desidera eseguire il rendering di molto testo:**

`{\fs10\copyfit100 $A${\copyfit200 $B$}$C$}`

Tutto il testo viene disegnato con \fs10 sul lato piccolo dell&#39;intervallo, mentre al suo massimo, *[!DNL $A$]* e *[!DNL $C$]* viene eseguito il rendering con `\fs100` e *[!DNL $B$]* con `\fs200`.

**Disabilita adattamento copia per un intervallo di testo interno:**

`{\fs10\copyfit100 $A${\fs50\copyfit0 $B$}$C$}`

Dimensione del font *[!DNL $A$]* e *[!DNL $C$]* può variare tra 10 e 100, mentre *[!DNL $B$]* viene sempre eseguito il rendering con `\fs50`.

**Limita l’output a una singola riga, anche se è disponibile più spazio verticale, ma consente l’overflow fino a righe aggiuntive se viene specificato troppo testo per l’inserimento in una singola riga `\fs10`:**

`{\fs10\copyfit100 \copyfitlines1 $A$}`

**Limita l&#39;output a una singola riga, anche se è disponibile più spazio verticale. Se viene specificato troppo testo per essere inserito in una singola riga, `\fs10` viene troncato:**

`{\fs10\copyfit100 \copyfitmaxlines1 $A$}`
