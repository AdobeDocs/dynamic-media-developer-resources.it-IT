---
description: Immagine di risposta di errore. Image Server in genere restituisce uno stato di errore con un messaggio di testo quando si verifica un errore.
solution: Experience Manager
title: ErrorImage
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: f412a379-525e-42fc-97bf-b10e00da6a20
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '274'
ht-degree: 1%

---

# ErrorImage{#errorimage}

Immagine di risposta di errore. Image Server in genere restituisce uno stato di errore con un messaggio di testo quando si verifica un errore.

`attribute::ErrorImage` consente di configurare un’immagine, una voce di catalogo o un modello da restituire in caso di errore.

>[!NOTE]
>
>Le immagini mancanti possono essere gestite anche con `attribute::DefaultImage`.

È possibile configurare un modello Image Server che potrebbe riprodurre il testo del messaggio di errore nell’immagine di risposta. Le seguenti variabili predefinite possono essere incluse nel `$error.title` modello, sostituito da una breve descrizione dell&#39;errore, e `$error.message`, sostituito da una descrizione più dettagliata dell’errore (il livello di dettaglio è configurato con `attribute::ErrorDetail`).

Se l&#39;immagine/modello di errore può essere elaborato correttamente, viene restituito lo stato HTTP 200. Se si verifica un errore durante questa elaborazione, vengono restituiti lo stato dell’errore HTTP e un messaggio di testo.

## Proprietà {#section-f460c6c2dd1f46b29f9a79b093575f45}

Stringa di testo. Se specificato, deve essere un valore catalog::Id valido in un catalogo immagini o un valore relativo (to `attribute::RootPath`) o il percorso assoluto di un file immagine accessibile dal server immagini.

## Predefinito {#section-2885f289e5714ddca665a6aee401967f}

Ereditato da `default::ErrorImage` se non è definita. Se è definito ma vuoto, il comportamento dell&#39;immagine di errore è disabilitato, anche se `default::ErrorImage` viene definito e vengono restituiti uno stato di errore HTTP e un messaggio di testo.

## Esempio {#section-c92090abe1d247529542a8dd4960c2e6}

Per ottenere immagini di risposta con il messaggio di errore rappresentato nell’immagine, è necessario innanzitutto definire il modello nel catalogo delle immagini. In questo caso, creiamo una voce nel nostro catalogo di immagini denominata `onError`, contenente quanto segue in `catalog::Modifier`:

`size=300,300&bgc=ffffff&text=$error.message$`

Il modello è registrato con `attribute::ErrorImage`:

`ErrorImage=myCatalog/onError`

In questo esempio, il rendering del testo viene eseguito utilizzando il carattere predefinito, il colore e la dimensione del carattere.

## Consultate anche {#section-bbf1f85fc0a34033bdda1dd3e4e0bbb6}

[attribute::RootPath](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md#reference-17d57e5967be403b8408fa7214017494) , [catalogo::Id](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-id-cat.md), [attribute::DefaultImage](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-is-cat-defaultimage.md#reference-8e9900e129f54ed68462a3c2fc3bc433), [attribute::ErrorDetail](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-errordetail.md#reference-4987c8cddcba4c88960170e49cafc561)
