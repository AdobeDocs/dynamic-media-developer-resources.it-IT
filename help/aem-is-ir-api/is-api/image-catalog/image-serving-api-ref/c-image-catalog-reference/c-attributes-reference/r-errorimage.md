---
description: Immagine di risposta di errore. Image Server restituisce normalmente uno stato di errore con un messaggio di testo quando si verifica un errore.
solution: Experience Manager
title: ErrorImage
feature: Dynamic Media Classic, SDK/API
role: Developer,Business Practitioner
exl-id: f412a379-525e-42fc-97bf-b10e00da6a20
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '280'
ht-degree: 1%

---

# ErrorImage{#errorimage}

Immagine di risposta di errore. Image Server restituisce normalmente uno stato di errore con un messaggio di testo quando si verifica un errore.

`attribute::ErrorImage` consente di configurare un&#39;immagine, una voce di catalogo o un modello da restituire in caso di errore.

>[!NOTE]
>
>Le immagini mancanti possono essere gestite anche con `attribute::DefaultImage`.

È possibile configurare un modello Image Server che potrebbe eseguire il rendering del testo del messaggio di errore nell’immagine di risposta. Le seguenti variabili predefinite possono essere incluse nel modello `$error.title`, che viene sostituito da una breve descrizione dell’errore, e `$error.message`, che viene sostituito da una descrizione dell’errore più dettagliata (il livello di dettaglio è configurato con `attribute::ErrorDetail`).

Se l’immagine/modello di errore può essere elaborato correttamente, viene restituito lo stato HTTP 200. Se si verifica un errore durante l’elaborazione, vengono restituiti lo stato di errore HTTP e un messaggio di testo.

## Proprietà {#section-f460c6c2dd1f46b29f9a79b093575f45}

Stringa di testo. Se specificato, deve essere un valore catalog::Id valido in un catalogo immagini o un percorso relativo (a `attribute::RootPath`) o assoluto a un file immagine accessibile dal server immagini.

## Predefinito {#section-2885f289e5714ddca665a6aee401967f}

Ereditato da `default::ErrorImage` se non definito. Se definito ma vuoto, il comportamento dell’immagine di errore viene disabilitato, anche se è definito `default::ErrorImage`, e viene restituito uno stato di errore HTTP e un messaggio di testo.

## Esempio {#section-c92090abe1d247529542a8dd4960c2e6}

Per ottenere immagini di risposta con il messaggio di errore di cui è stato eseguito il rendering nell’immagine, è necessario innanzitutto definire il modello nel catalogo immagini. In questo caso, creiamo una voce nel nostro catalogo immagini denominata `onError`, contenente quanto segue in `catalog::Modifier`:

`size=300,300&bgc=ffffff&text=$error.message$`

Il modello è registrato con `attribute::ErrorImage`:

`ErrorImage=myCatalog/onError`

In questo esempio, il testo verrà riprodotto utilizzando il font, il colore del font e le dimensioni del font predefiniti.

## Consultate anche {#section-bbf1f85fc0a34033bdda1dd3e4e0bbb6}

[attributo::RootPath](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md#reference-17d57e5967be403b8408fa7214017494) ,  [catalogo::Id](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-id-cat.md),  [attributo::DefaultImage](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-is-cat-defaultimage.md#reference-8e9900e129f54ed68462a3c2fc3bc433),  [attributo::ErrorDetail](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-errordetail.md#reference-4987c8cddcba4c88960170e49cafc561)
