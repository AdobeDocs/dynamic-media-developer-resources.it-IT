---
description: textPs= implementa un algoritmo proprietario di adattamento della copia che regola automaticamente le dimensioni del font per riempire in modo ottimale l'area di testo con il testo, riducendo al minimo lo spazio aggiuntivo nella parte inferiore ed evitando l'overflow.
solution: Experience Manager
title: Raccordo
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: d1a560f3-f92c-4143-b80a-e1674c8a4207
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '516'
ht-degree: 0%

---

# Raccordo{#copy-fitting}

textPs= implementa un algoritmo proprietario di adattamento della copia che regola automaticamente le dimensioni del font per riempire in modo ottimale l&#39;area di testo con il testo, riducendo al minimo lo spazio aggiuntivo nella parte inferiore ed evitando l&#39;overflow.

L&#39;adattamento del testo può essere attivato e controllato collettivamente per l&#39;intero livello di testo, in base al paragrafo, anche per una singola estensione di testo.

Specificare la dimensione minima del carattere con `\fs` e la dimensione massima del carattere con `\copyfit`. Nella stessa stringa RTF è consentito qualsiasi numero di intervalli. Le dimensioni di tutti gli intervalli vengono variate in modo proporzionale, garantendo il mantenimento dei rapporti di dimensione dei caratteri desiderati.

`\copyfit` è considerato un comando di formattazione di carattere e dispone di regole di ambito come `\fs` e `\b`.

L&#39;adattamento della copia è disabilitato specificando `\copyfit` con una dimensione uguale o inferiore a quella specificata con `\fs`.

## Limitazione del numero di righe {#section-e5aee0f039e04842afc3d6884ed681ac}

Oltre a specificare l&#39;intervallo di dimensioni dei caratteri, il comportamento dell&#39;algoritmo di adattamento della copia può essere ulteriormente controllato con i comandi `\copyfitlines` o `\copyfitmaxlines`, che limitano il numero di righe generate dall&#39;algoritmo. Entrambi i comandi accettano un parametro di conteggio righe o 0, per non limitare il numero di righe nell&#39;area adattata alla copia.

`\copyfitlines` consente l&#39;overflow del testo su righe aggiuntive quando non rientra nel numero di righe specificato. Le interruzioni di riga esplicite nel segmento di testo da copiare vengono sempre rispettate.

`\copyfitmaxlines` tronca sempre le righe di output in eccesso che superano il limite specificato. Il numero di righe specificato non viene mai superato, anche se sono presenti interruzioni di riga esplicite. Per questa versione di Image Server, nell&#39;intervallo di testo adattato alla copia non possono essere presenti più di N-1 `\line` marcatori. Comportamento non definito se viene superato questo limite.

## Esempi {#section-f4ddbbfade444560be30a813d90c2c1b}

Gli esempi seguenti presuppongono che i corpi di testo siano forniti con variabili denominate *[!DNL $A$]*, *[!DNL $B$]* e *[!DNL $C$]*.

**Mantenere lo stesso rapporto tra le dimensioni dei caratteri nell&#39;intervallo:**

`{\fs10\copyfit100 $A${\fs20\copyfit200 $B$}$C$}`

Il rendering di *[!DNL $B$]* è sempre eseguito il doppio del resto del testo. Se si specifica molto testo, viene eseguito il rendering di *[!DNL $A$]* e *[!DNL $C$]* con `\fs10` e *[!DNL $B$]* con `\fs20`. Con poco testo, *[!DNL $A$]* e *[!DNL $C$]* utilizzano `\fs100` e *[!DNL $B$]* `\fs200`.

**Converti in caratteri di grandi dimensioni comuni se viene disegnata solo una piccola quantità di testo:**

`{\copyfit100\fs10 $A${\fs20 $B$}$C$}`

All&#39;estremità più piccola dell&#39;intervallo, viene eseguito il rendering di *[!DNL $B$]* con `\fs20`, due volte più grande di *[!DNL $A$]* e *[!DNL $C$]* con `\fs10`. Tutto il testo viene disegnato a `\fs100` (50 punti) all&#39;estremità opposta dell&#39;intervallo.

**Converti in una dimensione di carattere piccola comune se deve essere eseguito il rendering di molto testo:**

`{\fs10\copyfit100 $A${\copyfit200 $B$}$C$}`

Tutto il testo viene disegnato con \fs10 all&#39;estremità inferiore dell&#39;intervallo, mentre all&#39;estremità più grande, *[!DNL $A$]* e *[!DNL $C$]* vengono rappresentati con `\fs100` e *[!DNL $B$]* con `\fs200`.

**Disabilita adattamento per testo interno:**

`{\fs10\copyfit100 $A${\fs50\copyfit0 $B$}$C$}`

La dimensione font per *[!DNL $A$]* e *[!DNL $C$]* può variare tra 10 e 100, mentre il rendering di *[!DNL $B$]* viene sempre eseguito con `\fs50`.

**Limitare l&#39;output a una singola riga, anche se è disponibile più spazio verticale, ma consentire l&#39;overflow a righe aggiuntive se è stata specificata una quantità di testo eccessiva per l&#39;inserimento in una singola riga in `\fs10`:**

`{\fs10\copyfit100 \copyfitlines1 $A$}`

**Limitare l&#39;output a una sola riga, anche se è disponibile più spazio verticale. Se viene specificata una quantità eccessiva di testo da inserire in una riga singola in `\fs10`, il testo verrà troncato:**

`{\fs10\copyfit100 \copyfitmaxlines1 $A$}`
