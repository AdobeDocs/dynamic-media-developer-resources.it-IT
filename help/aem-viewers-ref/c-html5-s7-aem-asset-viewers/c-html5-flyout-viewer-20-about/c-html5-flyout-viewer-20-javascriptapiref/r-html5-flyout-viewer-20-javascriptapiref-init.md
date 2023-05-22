---
description: Riferimento API JavaScript per il visualizzatore a comparsa.
solution: Experience Manager
title: init
feature: Dynamic Media Classic,Viewers,SDK/API,Flyout
role: Developer,User
exl-id: e86f8c0f-c130-43c5-8c3a-07c6bc49e2f7
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '122'
ht-degree: 1%

---

# init{#init}

Riferimento API JavaScript per il visualizzatore a comparsa.

`init()`

Avvia l&#39;inizializzazione del visualizzatore a comparsa. A questo punto, è necessario creare l’elemento DOM del contenitore in modo che il codice visualizzatore possa trovarlo in base al suo ID.

Se l’elemento contenitore non fa ancora parte del layout della pagina web (ad esempio, potrebbe essere nascosto tramite `display:none` ), il visualizzatore sospende il processo di inizializzazione fino al momento in cui la pagina web riporta l’elemento contenitore nel layout. In questo caso, il caricamento del visualizzatore riprende automaticamente.

Questo metodo deve essere chiamato una sola volta durante il ciclo di vita del visualizzatore e le chiamate conseguenti vengono ignorate.

## Parametri {#section-ad069aaaf4f145f2b50ae5ac89ca1ed2}

Nessuno.

## Restituisce {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

`{Object}` Riferimento all’istanza del visualizzatore.

## Esempio {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.init()
```
