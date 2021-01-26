---
description: La specifica RTF consente i valori di colore RGB specificati con &bsol;colortbl. Ciascun componente è fornito separatamente con i comandi &bsol;red, &bsol;green, e &bsol;blue.
solution: Experience Manager
title: Gestione del colore
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 6c51d204-27ca-4fbd-a297-bf1d04b63a3f
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '273'
ht-degree: 0%

---


# Gestione del colore{#color-handling}

La specifica RTF consente i valori di colore RGB specificati con `\colortbl`. Ciascun componente viene fornito separatamente con i comandi `\red`, `\green` e `\blue`.

Il comando proprietario dell&#39;estensione RTF `\cmykcolortbl` consente di specificare i colori CMYK, con ogni componente colore fornito con i comandi `\cyan`, `\magenta`, `\yellow` e `\black`.

I valori dei componenti colore per `\colortbl` sono compresi tra 0 e 255. I valori dei componenti per `\cmykcolortbl` sono compresi tra 0 e 100.

Il comando di estensione RTF `\*\iscolortbl`, supportato da `textPs=`, consente di specificare una tabella colori con valori di colore standard Image Serving, con supporto completo di RGB, grigio, CMYK e alfa. Contiene la sintassi seguente:

` {\&#42;\iscolortbl; *[!DNL colors]*;}`

*[!DNL colors]* uno o più valori di colore IS, separati da &#39;;&#39;

È possibile specificare più di un tipo di tabella colori nella stessa stringa RTF `text=` o `textPs=`. Ogni tavola colore può avere un numero diverso di voci. Image Serving tenterà di trovare i colori in questo ordine: `\iscolortbl` prima di `\cmykcolortbl` (solo se il tipo di pixel del livello di testo è CMYK) prima di `\colortbl`. Solo per `textPs=`, i colori vengono convertiti accuratamente tra CMYK e RGB, se necessario (ad esempio, se vengono specificati colori RGB ma è richiesta l&#39;uscita CMYK). Se non viene trovato alcun colore per un particolare valore di indice, viene utilizzato il colore predefinito (nero).

Fare riferimento a [color](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md) per una descrizione della sintassi dei valori di colore IS.

## Restrizioni {#section-c5173e672d854e4aa9656844f7fc4d0e}

`text=` non supporta  `\*\iscolortbl`. `textPs=` non supporta  `\cmykcolortbl`.

Le selezioni colore vengono ignorate durante il rendering dei font Photoshop.

## Esempio {#section-0f166bb72bd44479be01131077851142}

Consentite il controllo di tre colori di testo con le variabili, pur mantenendo visibile il valore di colore predefinito quando la stringa RTF viene aperta in un editor di testo RTF standard.

`…&$c1=ff0000&$c2=00ff00&$c3=0000ff&textPs={{\*\iscolortbl;$c1$;$c2$;$c3$;}{\colortbl;\red255;\green0;\blue0;\red0;\green255;\blue0;\red0;\green0;\blue255;}…}…`
