---
description: Riferimento API JavaScript per il visualizzatore Carosello.
solution: Experience Manager
title: init
feature: Dynamic Media Classic,Visualizzatori,SDK/API,Banner carosello
role: Sviluppatore, Business Practices
exl-id: 00e09e26-1380-487c-9512-34d805f1330d
translation-type: tm+mt
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '131'
ht-degree: 2%

---

# init{#init}

Riferimento API JavaScript per il visualizzatore Carosello.

`init()`

Avvia l&#39;inizializzazione del visualizzatore Carosello. A questo punto, l’elemento DOM contenitore deve essere creato in modo che il codice del visualizzatore possa trovarlo in base al suo ID.

Se l&#39;elemento contenitore non fa ancora parte del layout della pagina web (ad esempio, potrebbe essere nascosto utilizzando lo stile `display:none` assegnatogli), il visualizzatore sospende il processo di inizializzazione fino al momento in cui la pagina web riporta l&#39;elemento contenitore al layout. In questo caso, il caricamento del visualizzatore riprende automaticamente.

Chiama questo metodo una sola volta durante il ciclo di vita del visualizzatore; le chiamate successive vengono ignorate.

## Parametri {#section-ad069aaaf4f145f2b50ae5ac89ca1ed2}

Nessuno.

## Restituisce {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

`{Object}` Un riferimento all’istanza del visualizzatore.

## Esempio {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.init()
```
