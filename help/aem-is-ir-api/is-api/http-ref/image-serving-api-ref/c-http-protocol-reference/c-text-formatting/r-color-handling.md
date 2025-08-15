---
title: Trattamento del colore
description: La specifica RTF consente valori di colore RGB specificati con &bsol;colortbl. Ogni componente viene fornito separatamente con i comandi &bsol;red, &bsol;green e &bsol;blue.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 590ed0f1-8d78-4afc-ac9e-c28272cd24a6
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '279'
ht-degree: 0%

---

# Trattamento del colore{#color-handling}

La specifica RTF consente i valori di colore RGB specificati con `\colortbl`. Ogni componente viene fornito separatamente con i comandi `\red`, `\green` e `\blue`.

Il comando proprietario dell&#39;estensione RTF `\cmykcolortbl` consente di specificare colori CMYK, con ogni componente colore fornito con i comandi `\cyan`, `\magenta`, `\yellow` e `\black`.

I valori dei componenti colore per `\colortbl` sono compresi nell&#39;intervallo tra 0 e 255. I valori dei componenti per `\cmykcolortbl` sono compresi tra 0 e 100.

Il comando di estensione RTF `\*\iscolortbl`, supportato da `textPs=`, consente di specificare una tabella colori con valori di colore standard Image Server, con supporto completo per RGB, grigio, CMYK e alfa. Ha la seguente sintassi:

` {\&#42;\iscolortbl; *[!DNL colors]*;}`

*[!DNL colors]* uno o più valori di colore IS, separati da &#39;;&#39;

È possibile specificare più tipi di tabella colori nella stessa stringa RTF `text=` o `textPs=`. Ogni tabella colori può avere un numero diverso di voci. Image Server tenta di trovare i colori in questo ordine: `\iscolortbl` prima di `\cmykcolortbl` (solo se il tipo di pixel del livello di testo è CMYK) prima di `\colortbl`. Solo per `textPs=`, i colori vengono convertiti con precisione tra CMYK e RGB, se necessario (ad esempio, quando si specificano colori RGB ma è richiesto l&#39;output CMYK). Se non viene trovato alcun colore per un particolare valore di indice, viene utilizzato il colore predefinito (nero).

Fare riferimento a [color](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md) per una descrizione della sintassi dei valori dei colori IS.

## Restrizioni {#section-c5173e672d854e4aa9656844f7fc4d0e}

Il modificatore `text=` non supporta `\*\iscolortbl`. Il modificatore `textPs=` non supporta `\cmykcolortbl`.

Le selezioni dei colori vengono ignorate durante il rendering dei Photofont.

## Esempio {#section-0f166bb72bd44479be01131077851142}

Consente di controllare tre colori di testo con variabili, mentre viene visualizzato il valore predefinito del colore quando la stringa RTF viene aperta in un editor di testo RTF standard.

`…&$c1=ff0000&$c2=00ff00&$c3=0000ff&textPs={{\*\iscolortbl;$c1$;$c2$;$c3$;}{\colortbl;\red255;\green0;\blue0;\red0;\green255;\blue0;\red0;\green0;\blue255;}…}…`
