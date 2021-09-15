---
title: init
description: Riferimento API JavaScript per il visualizzatore Carosello.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Carousel Banners
role: Developer,User
exl-id: 00e09e26-1380-487c-9512-34d805f1330d
source-git-commit: 96ac67e5645c2c55920cc971806ba2f14ae57044
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# init{#init}

Riferimento API JavaScript per il visualizzatore Carosello.

`init()`

Avvia l&#39;inizializzazione del visualizzatore Carosello. A questo punto, l’elemento DOM contenitore deve essere creato in modo che il codice del visualizzatore possa trovarlo in base al suo ID.

Se l&#39;elemento contenitore non fa ancora parte del layout della pagina web, ad esempio potrebbe essere nascosto utilizzando lo stile `display:none`, il visualizzatore sospende il processo di inizializzazione. Viene sospeso fino al momento in cui la pagina web riporta l’elemento contenitore al layout, nel quale riprende automaticamente il caricamento del visualizzatore.

Chiama questo metodo una sola volta durante il ciclo di vita del visualizzatore; le chiamate successive vengono ignorate.

## Parametri {#section-ad069aaaf4f145f2b50ae5ac89ca1ed2}

Nessuno.

## Restituisce {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

`{Object}` Un riferimento all’istanza del visualizzatore.

## Esempio {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.init()
```
