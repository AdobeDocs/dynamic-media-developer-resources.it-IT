---
description: Riferimento API JavaScript per visualizzatore zoom in linea.
solution: Experience Manager
title: init
feature: Dynamic Media Classic,Visualizzatori,SDK/API,Zoom in linea
role: Developer,User
exl-id: c4419728-1e1a-4e11-88fe-24eb0c968c5c
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '130'
ht-degree: 2%

---

# init{#init}

Riferimento API JavaScript per visualizzatore zoom in linea.

`init()`

Avvia l&#39;inizializzazione del visualizzatore in modo che il codice del visualizzatore possa trovarlo in base al suo ID. A questo punto è necessario creare l’elemento DOM del contenitore.

Se l&#39;elemento contenitore non fa ancora parte del layout della pagina web (ad esempio, potrebbe essere nascosto utilizzando lo stile `display:none` assegnatogli), il visualizzatore sospende il processo di inizializzazione fino al momento in cui la pagina web riporta l&#39;elemento contenitore al layout. In questo caso, il caricamento del visualizzatore riprende automaticamente.

Chiamare questo metodo una sola volta durante il ciclo di vita del visualizzatore; le chiamate successive vengono ignorate.

## Parametri {#section-ad069aaaf4f145f2b50ae5ac89ca1ed2}

Nessuno.

## Restituisce {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

`{Object}` Un riferimento all’istanza del visualizzatore.

## Esempio {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.init()
```
