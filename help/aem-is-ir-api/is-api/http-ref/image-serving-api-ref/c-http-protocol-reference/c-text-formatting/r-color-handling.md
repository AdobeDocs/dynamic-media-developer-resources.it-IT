---
description: La specifica RTF consente valori di colore RGB specificati con &bsol;colortbl. Ogni componente è fornito separatamente con i comandi &bsol;rosso, &bsol;verde e &bsol;blu.
solution: Experience Manager
title: Trattamento del colore
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '281'
ht-degree: 0%

---


# Trattamento del colore{#color-handling}

La specifica RTF consente valori di colore RGB specificati con `\colortbl`. Ciascun componente viene fornito separatamente con i comandi `\red`, `\green` e `\blue`.

Il comando proprietario dell&#39;estensione RTF `\cmykcolortbl` consente di specificare i colori CMYK, con ogni componente colore fornito con i comandi `\cyan`, `\magenta`, `\yellow` e `\black`.

I valori dei componenti colore per `\colortbl` sono compresi tra 0 e 255. I valori dei componenti per `\cmykcolortbl` sono compresi tra 0 e 100.

Il comando di estensione RTF `\*\iscolortbl`, supportato da `textPs=`, fornisce un modo per specificare una tabella dei colori con valori di colore standard Image Serving, con supporto RGB, grigio, CMYK e alfa completo. Ha la seguente sintassi:

` {\&#42;\iscolortbl; *[!DNL colors]*;}`

*[!DNL colors]* uno o più valori di colore IS, separati da &#39;;&#39;

È possibile specificare più di un tipo di tabella colori nella stessa stringa RTF `text=` o `textPs=`. Ogni tabella di colori può avere un numero di voci diverso. Image Serving tenterà di trovare i colori in questo ordine: `\iscolortbl` prima di `\cmykcolortbl` (solo se il tipo di pixel del livello di testo è CMYK) prima di `\colortbl`. Solo per `textPs=`, i colori vengono convertiti con precisione tra CMYK e RGB, se necessario (ad esempio, quando sono specificati colori RGB ma è richiesto l’output CMYK). Se non viene trovato alcun colore per un particolare valore di indice, viene utilizzato il colore predefinito (nero).

Per una descrizione della sintassi dei valori di colore IS, fare riferimento a [color](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md) .

## Restrizioni {#section-c5173e672d854e4aa9656844f7fc4d0e}

`text=` non supporta  `\*\iscolortbl`. `textPs=` non supporta  `\cmykcolortbl`.

Le selezioni colore vengono ignorate durante il rendering dei font Photofont.

## Esempio {#section-0f166bb72bd44479be01131077851142}

Consenti il controllo di tre colori di testo con le variabili, pur visualizzando il valore predefinito del colore quando la stringa RTF viene aperta in un editor di testo RTF standard.

`…&$c1=ff0000&$c2=00ff00&$c3=0000ff&textPs={{\*\iscolortbl;$c1$;$c2$;$c3$;}{\colortbl;\red255;\green0;\blue0;\red0;\green255;\blue0;\red0;\green0;\blue255;}…}…`
