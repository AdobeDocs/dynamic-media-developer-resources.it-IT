---
title: init
description: Riferimento API JavaScript per il visualizzatore eCatalog.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: e7775a65-67bf-4ad6-8e51-1fdf141946bc
source-git-commit: edc127dc6e2ae2d9bd5feed08c8bc896c8c39747
workflow-type: tm+mt
source-wordcount: '122'
ht-degree: 1%

---

# init{#init}

Riferimento API JavaScript per il visualizzatore eCatalog.

`init()`

Avvia l&#39;inizializzazione del visualizzatore eCatalog. A questo punto è necessario creare l’elemento DOM del contenitore in modo che il codice del visualizzatore possa trovarlo in base al suo ID.

Se l’elemento contenitore non fa ancora parte del layout della pagina web, ad esempio può essere nascosto utilizzando `display:none` stile assegnato: il visualizzatore sospende il processo di inizializzazione. Lo fa fino al momento in cui la pagina web riporta l’elemento contenitore al layout. Quando questa azione si verifica, il caricamento del visualizzatore riprende automaticamente.

Chiama questo metodo una sola volta durante il ciclo di vita del visualizzatore; le chiamate successive vengono ignorate.

## Parametri {#section-ad069aaaf4f145f2b50ae5ac89ca1ed2}

Nessuno.

## Restituisce {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

`{Object}` Riferimento all’istanza del visualizzatore.

## Esempio {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
\<instance>.init()
```
