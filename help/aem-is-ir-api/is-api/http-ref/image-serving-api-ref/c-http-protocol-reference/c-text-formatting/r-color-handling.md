---
description: La specifica RTF consente valori di colore RGB specificati con &bsol;colortbl. Ogni componente viene fornito separatamente con i comandi &bsol;red, &bsol;green e &bsol;blue.
solution: Experience Manager
title: Trattamento del colore
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 590ed0f1-8d78-4afc-ac9e-c28272cd24a6
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '273'
ht-degree: 0%

---

# Trattamento del colore{#color-handling}

La specifica RTF consente i valori di colore RGB specificati con `\colortbl`. Ogni componente viene fornito separatamente con `\red`, `\green`, e `\blue` comandi.

Comando di estensione RTF proprietario `\cmykcolortbl` consente di specificare colori CMYK, con ogni componente di colore fornito con `\cyan`, `\magenta`, `\yellow`, e `\black` comandi.

Valori dei componenti colore per `\colortbl` sono compresi tra 0 e 255. Valori dei componenti per `\cmykcolortbl` sono compresi tra 0 e 100.

Comando estensione RTF `\*\iscolortbl`, supportato da `textPs=`, consente di specificare una tavola dei colori con i valori standard dei colori Image Server, con supporto completo per RGB, grigio, CMYK e alfa. Ha la seguente sintassi:

` {\&#42;\iscolortbl; *[!DNL colors]*;}`

*[!DNL colors]* uno o più valori di colore IS, separati da &#39;;&#39;

È possibile specificare più di un tipo di tabella colori nello stesso `text=` o `textPs=` Stringa RTF. Ogni tabella colori può avere un numero diverso di voci. Image Server tenterà di trovare i colori in questo ordine: `\iscolortbl` prima di `\cmykcolortbl` (solo se il tipo di pixel del livello testo è CMYK) prima `\colortbl`. Per `textPs=` solo, i colori vengono convertiti con precisione tra CMYK e RGB, se necessario (ad esempio, quando si specificano colori RGB ma è richiesto l’output CMYK). Se non viene trovato alcun colore per un particolare valore di indice, viene utilizzato il colore predefinito (nero).

Fai riferimento a [colore](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md) per una descrizione della sintassi dei valori dei colori IS.

## Restrizioni {#section-c5173e672d854e4aa9656844f7fc4d0e}

`text=` non supporta `\*\iscolortbl`. `textPs=` non supporta `\cmykcolortbl`.

Le selezioni dei colori vengono ignorate durante il rendering dei Photofont.

## Esempio {#section-0f166bb72bd44479be01131077851142}

Consente di controllare tre colori di testo con variabili, mentre viene visualizzato il valore predefinito del colore quando la stringa RTF viene aperta in un editor di testo RTF standard.

`…&$c1=ff0000&$c2=00ff00&$c3=0000ff&textPs={{\*\iscolortbl;$c1$;$c2$;$c3$;}{\colortbl;\red255;\green0;\blue0;\red0;\green255;\blue0;\red0;\green0;\blue255;}…}…`
