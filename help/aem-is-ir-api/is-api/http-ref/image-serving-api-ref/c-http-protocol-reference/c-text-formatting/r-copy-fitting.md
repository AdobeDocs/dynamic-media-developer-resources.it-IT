---
description: textPs= implementa un algoritmo proprietario di adattamento alla copia che regola automaticamente le dimensioni del carattere per riempire in modo ottimale l'area di testo con del testo, riducendo al minimo lo spazio aggiuntivo nella parte inferiore evitando al contempo l'overflow.
solution: Experience Manager
title: Adattamento copia
feature: Dynamic Media Classic, SDK/API
role: Developer,Business Practitioner
exl-id: d1a560f3-f92c-4143-b80a-e1674c8a4207
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '528'
ht-degree: 0%

---

# Adattamento copia{#copy-fitting}

textPs= implementa un algoritmo proprietario di adattamento alla copia che regola automaticamente le dimensioni del carattere per riempire in modo ottimale l&#39;area di testo con del testo, riducendo al minimo lo spazio aggiuntivo nella parte inferiore evitando al contempo l&#39;overflow.

L’adattamento può essere attivato e controllato collettivamente per l’intero livello di testo, a livello di paragrafo, anche per un singolo intervallo di testo.

Specifica la dimensione minima del font con `\fs` e la dimensione massima del font con `\copyfit`. Qualsiasi numero di intervalli è consentito nella stessa stringa RTF. Le dimensioni di tutti gli intervalli sono diverse in modo proporzionale, garantendo il mantenimento dei rapporti desiderati sulle dimensioni del font.

`\copyfit` è considerato un comando di formattazione dei caratteri e ha regole di ambito come  `\fs` e  `\b`.

Il raccordo per la copia è disattivato specificando `\copyfit` con dimensioni uguali o inferiori alle dimensioni specificate con `\fs`.

## Limitazione del numero di righe {#section-e5aee0f039e04842afc3d6884ed681ac}

Oltre a specificare l’intervallo di dimensioni dei font, il comportamento dell’algoritmo di adattamento alla copia può essere ulteriormente controllato con i comandi `\copyfitlines` o `\copyfitmaxlines`, che limitano il numero di righe che l’algoritmo genererà. Entrambi i comandi accettano un parametro di conteggio delle righe o 0, per non limitare il numero di righe nell&#39;area copiata.

`\copyfitlines` consente l’overflow del testo su righe aggiuntive quando non rientra nel numero di righe specificato. Le interruzioni di riga esplicite nel segmento di testo da copiare vengono sempre rispettate.

`\copyfitmaxlines` tronca sempre le linee di output aggiuntive che superano il limite specificato. Il numero specificato di linee non verrà mai superato, anche se sono presenti interruzioni di riga esplicite. Per questo rilascio di Image Serving, non possono essere presenti più marcatori N-1 `\line` nell&#39;intervallo di testo adattato in copia. Il comportamento non è definito se questo limite viene superato.

## Esempi {#section-f4ddbbfade444560be30a813d90c2c1b}

Gli esempi seguenti presuppongono che i corpi di testo siano forniti con variabili denominate *[!DNL $A$]*, *[!DNL $B$]* e *[!DNL $C$]*.

**Mantenere lo stesso rapporto tra le dimensioni dei font in tutto l’intervallo:**

`{\fs10\copyfit100 $A${\fs20\copyfit200 $B$}$C$}`

*[!DNL $B$]* viene sempre eseguito il rendering di dimensioni due volte superiori al resto del testo. Quando viene specificato molto testo, viene eseguito il rendering di *[!DNL $A$]* e *[!DNL $C$]* con `\fs10` e *[!DNL $B$]* con `\fs20`. Con testo piccolo, *[!DNL $A$]* e *[!DNL $C$]* utilizzeranno `\fs100` e *[!DNL $B$]* `\fs200`.

**Converti in un font di grandi dimensioni comune se viene disegnata solo una piccola quantità di testo:**

`{\copyfit100\fs10 $A${\fs20 $B$}$C$}`

All&#39;estremità più piccola dell&#39;intervallo, viene eseguito il rendering di *[!DNL $B$]* con `\fs20`, il doppio rispetto a *[!DNL $A$]* e *[!DNL $C$]* in `\fs10`. Tutto il testo verrà disegnato all’ `\fs100` (50 punti) all’estremità opposta dell’intervallo.

**Converti in un font piccolo comune se si desidera eseguire il rendering di molto testo:**

`{\fs10\copyfit100 $A${\copyfit200 $B$}$C$}`

Tutto il testo viene disegnato con \fs10 all’estremità piccola dell’intervallo, mentre ai suoi valori più grandi, *[!DNL $A$]* e *[!DNL $C$]* vengono sottoposti a rendering con `\fs100` e *[!DNL $B$]* con `\fs200`.

**Disabilita adattamento copia per un intervallo di testo interno:**

`{\fs10\copyfit100 $A${\fs50\copyfit0 $B$}$C$}`

Le dimensioni del font per *[!DNL $A$]* e *[!DNL $C$]* possono variare tra 10 e 100, mentre per *[!DNL $B$]* viene sempre eseguito il rendering con `\fs50`.

**Limita l’output a una singola riga, anche se è disponibile più spazio verticale, ma consente l’overflow fino a righe aggiuntive se viene specificato troppo testo per l’inserimento in una singola riga in  `\fs10`:**

`{\fs10\copyfit100 \copyfitlines1 $A$}`

**Limita l&#39;output a una singola riga, anche se è disponibile più spazio verticale. Se viene specificato troppo testo per essere inserito in una singola riga in `\fs10`, verrà troncato:**

`{\fs10\copyfit100 \copyfitmaxlines1 $A$}`
