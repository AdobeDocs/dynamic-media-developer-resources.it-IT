---
description: textPs= implementa un algoritmo proprietario di adattamento alla copia che regola automaticamente le dimensioni dei font per riempire in modo ottimale l'area di testo con del testo, riducendo al minimo lo spazio disponibile nella parte inferiore ed evitando al contempo l'overflow.
seo-description: textPs= implementa un algoritmo proprietario di adattamento alla copia che regola automaticamente le dimensioni dei font per riempire in modo ottimale l'area di testo con del testo, riducendo al minimo lo spazio disponibile nella parte inferiore ed evitando al contempo l'overflow.
seo-title: Adattamento copia
solution: Experience Manager
title: Adattamento copia
topic: Scene7 Image Serving - Image Rendering API
uuid: c3ddbf1f-c724-4436-96ff-2c616dfd355d
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '555'
ht-degree: 0%

---


# Adattamento copia{#copy-fitting}

textPs= implementa un algoritmo proprietario di adattamento alla copia che regola automaticamente le dimensioni dei font per riempire in modo ottimale l&#39;area di testo con del testo, riducendo al minimo lo spazio disponibile nella parte inferiore ed evitando al contempo l&#39;overflow.

L’adattamento alla copia può essere attivato e controllato collettivamente per l’intero livello di testo, a livello di paragrafo, anche per una singola estensione di testo.

Specificate la dimensione minima del font con `\fs` e la dimensione massima del font con `\copyfit`. Un numero qualsiasi di intervalli è consentito nella stessa stringa RTF. Le dimensioni per tutti gli intervalli sono variabili in modo proporzionale, garantendo il mantenimento delle proporzioni desiderate per i font.

`\copyfit` è considerato un comando di formattazione dei caratteri e ha regole di ambito come  `\fs` e  `\b`.

L&#39;adattamento alla copia è disattivato specificando `\copyfit` con una dimensione uguale o inferiore alla dimensione specificata con `\fs`.

## Limitazione del numero di righe {#section-e5aee0f039e04842afc3d6884ed681ac}

Oltre a specificare l&#39;intervallo di dimensioni dei font, il comportamento dell&#39;algoritmo di adattamento alla copia può essere controllato ulteriormente con i comandi `\copyfitlines` o `\copyfitmaxlines`, che limitano il numero di righe che l&#39;algoritmo genererà. Entrambi i comandi accettano un parametro di conteggio delle righe o 0, per non limitare il numero di righe nell&#39;area copiata.

`\copyfitlines` consente l&#39;overflow del testo su righe aggiuntive quando non rientra nel numero specificato di righe. Le interruzioni di riga esplicite nel segmento di testo da copiare vengono sempre rispettate.

`\copyfitmaxlines` tronca sempre le linee di output aggiuntive che superano il limite specificato. Il numero specificato di righe non verrà mai superato, anche se sono presenti interruzioni di riga esplicite. Per questa versione di Image Server, non possono essere presenti più marcatori N-1 `\line` nell’intervallo di testo copiato. Se questo limite viene superato, il comportamento non è definito.

## Esempi {#section-f4ddbbfade444560be30a813d90c2c1b}

Gli esempi seguenti presuppongono che i corpi di testo siano forniti con variabili denominate *[!DNL $A$]*, *[!DNL $B$]* e *[!DNL $C$]*.

**Mantenete lo stesso rapporto tra le dimensioni dei font nell&#39;intervallo:**

`{\fs10\copyfit100 $A${\fs20\copyfit200 $B$}$C$}`

*[!DNL $B$]* il rendering sarà sempre doppio rispetto al resto del testo. Quando viene specificato molto testo, *[!DNL $A$]* e *[!DNL $C$]* verranno sottoposti a rendering con `\fs10` e *[!DNL $B$]* con `\fs20`. Con testo piccolo, *[!DNL $A$]* e *[!DNL $C$]* saranno utilizzati `\fs100` e *[!DNL $B$]* `\fs200`.

**Convertite in una dimensione font grande comune se viene disegnata solo una piccola quantità di testo:**

`{\copyfit100\fs10 $A${\fs20 $B$}$C$}`

All&#39;estremità più piccola dell&#39;intervallo, *[!DNL $B$]* verrà eseguito il rendering con `\fs20`, il doppio di *[!DNL $A$]* e *[!DNL $C$]* in `\fs10`. Tutto il testo verrà disegnato all&#39;estremità opposta dell&#39;intervallo `\fs100` (50 punti).

**Converti in una dimensione font piccola comune se si desidera eseguire il rendering di molto testo:**

`{\fs10\copyfit100 $A${\copyfit200 $B$}$C$}`

Tutto il testo viene disegnato con \fs10 all&#39;estremità piccola dell&#39;intervallo, mentre al lato più grande, *[!DNL $A$]* e *[!DNL $C$]* vengono sottoposti a rendering con `\fs100` e *[!DNL $B$]* con `\fs200`.

**Disattiva l’adattamento alla copia per un intervallo di testo interno:**

`{\fs10\copyfit100 $A${\fs50\copyfit0 $B$}$C$}`

La dimensione del font per *[!DNL $A$]* e *[!DNL $C$]* può variare da 10 a 100, mentre per *[!DNL $B$]* viene sempre eseguito il rendering con `\fs50`.

**Limitare l&#39;output a una singola riga, anche se è disponibile più spazio verticale, ma consentirne l&#39;overflow fino a righe aggiuntive se viene specificato troppo testo per adattarsi a una singola riga in  `\fs10`:**

`{\fs10\copyfit100 \copyfitlines1 $A$}`

**Limitare l&#39;output a una singola riga, anche se è disponibile più spazio verticale. Se viene specificato troppo testo per essere inserito in una singola riga in `\fs10`, verrà troncato:**

`{\fs10\copyfit100 \copyfitmaxlines1 $A$}`
