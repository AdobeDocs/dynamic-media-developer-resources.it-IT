---
description: Immagine della risposta di errore. Image Server restituisce normalmente uno stato di errore con un messaggio di testo quando si verifica un errore.
seo-description: Immagine della risposta di errore. Image Server restituisce normalmente uno stato di errore con un messaggio di testo quando si verifica un errore.
seo-title: ErrorImage
solution: Experience Manager
title: ErrorImage
topic: Scene7 Image Serving - Image Rendering API
uuid: b071c0cd-e7b8-422b-9b23-d93f504d9ce5
translation-type: tm+mt
source-git-commit: fe557a2429ceb7b48f22b9cbef5820ad39bad69f

---


# ErrorImage{#errorimage}

Immagine della risposta di errore. Image Server restituisce normalmente uno stato di errore con un messaggio di testo quando si verifica un errore.

`attribute::ErrorImage` consente di configurare un’immagine, una voce di catalogo o un modello da restituire in caso di errore.

>[!NOTE]
>
>È inoltre possibile gestire le immagini mancanti con `attribute::DefaultImage`.

È possibile configurare un modello Image Server che potrebbe rappresentare il testo del messaggio di errore nell’immagine della risposta. Le seguenti variabili predefinite possono essere incluse nel `$error.title` modello, che viene sostituito con una breve descrizione dell’errore, e `$error.message`, che viene sostituita da una descrizione dell’errore più dettagliata (il livello di dettaglio è configurato con `attribute::ErrorDetail`).

Se è possibile elaborare correttamente l&#39;immagine o il modello di errore, viene restituito lo stato HTTP 200. Se durante l&#39;elaborazione si verifica un errore, vengono restituiti lo stato di errore HTTP e un messaggio di testo.

## Proprietà {#section-f460c6c2dd1f46b29f9a79b093575f45}

Stringa di testo. Se specificato, deve essere un valore catalog::Id valido in un catalogo immagini o un percorso relativo (da `attribute::RootPath`) o assoluto a un file immagine accessibile dal server immagini.

## Predefinito {#section-2885f289e5714ddca665a6aee401967f}

Ereditato da `default::ErrorImage` se non definito. Se definito ma vuoto, il comportamento dell&#39;immagine di errore è disabilitato, anche se `default::ErrorImage` è definito, e viene restituito uno stato di errore HTTP e un messaggio di testo.

## Esempio {#section-c92090abe1d247529542a8dd4960c2e6}

Per ottenere immagini di risposta con il messaggio di errore rappresentato nell’immagine, è necessario innanzitutto definire il modello nel catalogo immagini. In questo caso, nel nostro catalogo immagini viene creata una voce denominata `onError`, contenente quanto segue in `catalog::Modifier`:

`size=300,300&bgc=ffffff&text=$error.message$`

Il modello è registrato con `attribute::ErrorImage`:

`ErrorImage=myCatalog/onError`

Per questo esempio, il testo verrà riprodotto utilizzando il font predefinito, il colore del font e la dimensione del font.

## Consultate anche {#section-bbf1f85fc0a34033bdda1dd3e4e0bbb6}

[attributo::RootPath](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md#reference-17d57e5967be403b8408fa7214017494) , [catalogo::Id](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-id-cat.md), [attributo::DefaultImage](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-is-cat-defaultimage.md#reference-8e9900e129f54ed68462a3c2fc3bc433), [attributo::ErrorDetail](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-errordetail.md#reference-4987c8cddcba4c88960170e49cafc561)
