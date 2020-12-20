---
description: Riferimento API JavaScript per il visualizzatore zoom di base.
seo-description: Riferimento API JavaScript per il visualizzatore zoom di base.
seo-title: init
solution: Experience Manager
title: init
topic: Dynamic media
uuid: a2a4fb97-89ec-41d2-ada7-8ff1775eaefa
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '131'
ht-degree: 2%

---


# init{#init}

Riferimento API JavaScript per il visualizzatore zoom di base.

`init()`

Avvia l’inizializzazione del visualizzatore zoom di base. Per questa volta, è necessario creare l’elemento DOM contenitore in modo che il codice del visualizzatore possa trovarlo in base al suo ID.

Se l&#39;elemento contenitore non fa ancora parte del layout della pagina Web (ad esempio, potrebbe essere nascosto utilizzando lo stile `display:none` assegnatogli), il visualizzatore sospende il processo di inizializzazione fino al momento in cui la pagina Web riporta l&#39;elemento contenitore al layout. In questo caso, il caricamento del visualizzatore riprende automaticamente.

Chiamare questo metodo una sola volta durante il ciclo di vita del visualizzatore; le chiamate successive vengono ignorate.

## Parametri {#section-ad069aaaf4f145f2b50ae5ac89ca1ed2}

Nessuno.

## Restituisce {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

`{Object}` Un riferimento all’istanza del visualizzatore.

## Esempio {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.init()
```

