---
description: Riferimento API JavaScript per il visualizzatore 360 gradi.
seo-description: Riferimento API JavaScript per il visualizzatore 360 gradi.
seo-title: init
solution: Experience Manager
title: init
topic: Dynamic media
uuid: 1803028f-dcba-49da-9fb7-78bfd64fc47d
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# init{#init}

Riferimento API JavaScript per il visualizzatore 360 gradi.

`init()`

Avvia l’inizializzazione del visualizzatore 360 gradi. Per questa volta, è necessario creare l&#39; `DOM` elemento contenitore in modo che il codice del visualizzatore possa trovarlo in base al suo ID.

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

