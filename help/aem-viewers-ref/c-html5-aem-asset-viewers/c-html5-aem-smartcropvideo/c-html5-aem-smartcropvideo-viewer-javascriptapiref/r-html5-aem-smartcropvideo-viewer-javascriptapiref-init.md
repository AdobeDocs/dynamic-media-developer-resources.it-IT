---
title: init
description: Riferimento API JavaScript per Smart Crop Video Viewer.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop Video
role: Developer,User
exl-id: d46a9c8b-064a-4928-b30e-885b12d287ab
source-git-commit: b6ebc938f55117c4144ff921bed7f8742cf3a8a7
workflow-type: tm+mt
source-wordcount: '130'
ht-degree: 2%

---

# init{#init}

Riferimento API JavaScript per Smart Crop Video Viewer.

`init()`

Avvia l&#39;inizializzazione di Smart Crop Video Viewer. A questo punto, l’elemento DOM contenitore deve essere creato in modo che il codice del visualizzatore possa trovarlo in base al suo ID.

Se l’elemento contenitore non fa ancora parte del layout della pagina web, ad esempio, potrebbe essere nascosto utilizzando `display:none` stile assegnato a esso - il visualizzatore sospende il processo di inizializzazione. Lo fa fino al momento in cui la pagina web riporta l’elemento contenitore al layout. Quando si verifica questa azione, il caricamento del visualizzatore riprende automaticamente.

Chiama questo metodo una sola volta durante il ciclo di vita del visualizzatore; le chiamate successive vengono ignorate.

## Parametri {#section-ad069aaaf4f145f2b50ae5ac89ca1ed2}

Nessuno.

## Restituisce {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

`{Object}` Un riferimento all’istanza del visualizzatore.

## Esempio {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.init()
```
