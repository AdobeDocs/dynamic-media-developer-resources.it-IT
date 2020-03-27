---
description: Riferimento API JavaScript per il visualizzatore zoom in linea.
seo-description: Riferimento API JavaScript per il visualizzatore zoom in linea.
seo-title: init
solution: Experience Manager
title: init
topic: Dynamic media
uuid: a3bd0cd1-e4cb-4b09-a78f-0958b55a79e4
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# init{#init}

Riferimento API JavaScript per il visualizzatore zoom in linea.

`init()`

Avvia l&#39;inizializzazione del visualizzatore in modo che il codice possa trovarlo in base al suo ID. Per questa volta è necessario creare l&#39;elemento DOM contenitore.

Se l’elemento contenitore non fa ancora parte del layout della pagina Web (ad esempio, potrebbe essere nascosto utilizzando `display:none` lo stile assegnato), il visualizzatore sospende il processo di inizializzazione fino al momento in cui la pagina Web riporta l’elemento contenitore al layout. In questo caso, il caricamento del visualizzatore riprende automaticamente.

Chiamare questo metodo una sola volta durante il ciclo di vita del visualizzatore; le chiamate successive vengono ignorate.

## Parametri {#section-ad069aaaf4f145f2b50ae5ac89ca1ed2}

Nessuno.

## Restituisce {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

`{Object}` Un riferimento all’istanza del visualizzatore.

## Esempio {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.init()
```

