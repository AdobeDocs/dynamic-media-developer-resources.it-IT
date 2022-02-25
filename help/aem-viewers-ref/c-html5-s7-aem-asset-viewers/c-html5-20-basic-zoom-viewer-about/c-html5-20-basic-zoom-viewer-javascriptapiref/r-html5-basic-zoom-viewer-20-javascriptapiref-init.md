---
title: init
description: Riferimento API JavaScript per visualizzatore zoom di base.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: cef585ae-44d7-406c-96f9-e03959a8e518
source-git-commit: 61e3a1fd0e21d336eaf5232096f5b1b54f2a6353
workflow-type: tm+mt
source-wordcount: '126'
ht-degree: 2%

---

# init{#init}

Riferimento API JavaScript per visualizzatore zoom di base.

`init()`

Avvia l&#39;inizializzazione del visualizzatore zoom di base. A questo punto, l’elemento DOM contenitore deve essere creato in modo che il codice del visualizzatore possa trovarlo in base al suo ID.

Se l’elemento contenitore non fa ancora parte del layout della pagina web (ad esempio, potrebbe essere nascosto utilizzando `display:none` stile assegnato), il visualizzatore sospende il processo di inizializzazione. Lo fa fino al momento in cui la pagina web riporta l’elemento contenitore al layout. Quando si verifica questa azione, il caricamento del visualizzatore riprende automaticamente.

Chiamare questo metodo una sola volta durante il ciclo di vita del visualizzatore; le chiamate successive vengono ignorate.

## Parametri {#section-ad069aaaf4f145f2b50ae5ac89ca1ed2}

Nessuno.

## Restituisce {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

`{Object}` Un riferimento all’istanza del visualizzatore.

## Esempio {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.init()
```
