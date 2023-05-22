---
title: init
description: Riferimento API JavaScript per il visualizzatore zoom in linea.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Inline Zoom
role: Developer,User
exl-id: c4419728-1e1a-4e11-88fe-24eb0c968c5c
source-git-commit: 50dddf148345d2ca5243d5d7108fefa56d23dad6
workflow-type: tm+mt
source-wordcount: '125'
ht-degree: 1%

---

# init{#init}

Riferimento API JavaScript per il visualizzatore zoom in linea.

`init()`

Avvia l&#39;inizializzazione del visualizzatore in modo che il codice del visualizzatore possa trovarlo in base al relativo ID. A questo punto è necessario creare l’elemento DOM del contenitore.

Se l’elemento contenitore non fa ancora parte del layout della pagina web, ad esempio può essere nascosto utilizzando `display:none` stile assegnato: il visualizzatore sospende il processo di inizializzazione. Lo fa fino al momento in cui la pagina web riporta l’elemento contenitore al layout. Quando si verifica questa azione, il caricamento del visualizzatore riprende automaticamente.

Chiama questo metodo una sola volta durante il ciclo di vita del visualizzatore; le chiamate successive vengono ignorate.

## Parametri {#section-ad069aaaf4f145f2b50ae5ac89ca1ed2}

Nessuno.

## Restituisce {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

`{Object}` Riferimento all’istanza del visualizzatore.

## Esempio {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.init()
```
