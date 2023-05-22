---
title: init
description: Riferimento API JavaScript per il visualizzatore 360 gradi.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Spin Sets
role: Developer,User
exl-id: 5217a02a-6092-4cb9-b4fb-f959cdc85a6e
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '118'
ht-degree: 1%

---

# init{#init}

Riferimento API JavaScript per il visualizzatore 360 gradi.

`init()`

Avvia l&#39;inizializzazione del visualizzatore 360 gradi. A questo punto il contenitore `DOM` deve essere creato in modo che il codice visualizzatore possa trovarlo in base al suo ID.

Se l’elemento contenitore non fa ancora parte del layout della pagina web, ad esempio può essere nascosto utilizzando `display:none` style: il visualizzatore sospende il processo di inizializzazione. Viene sospeso fino al momento in cui la pagina web riporta l’elemento contenitore nel layout, momento in cui il caricamento del visualizzatore riprende automaticamente.

Chiama questo metodo una sola volta durante il ciclo di vita del visualizzatore; le chiamate successive vengono ignorate.

## Parametri {#section-ad069aaaf4f145f2b50ae5ac89ca1ed2}

Nessuno.

## Restituisce {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

`{Object}` Riferimento all’istanza del visualizzatore.

## Esempio {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.init()
```
