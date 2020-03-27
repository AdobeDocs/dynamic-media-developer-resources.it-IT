---
description: Riferimento API JavaScript per il visualizzatore video interattivo.
seo-description: Riferimento API JavaScript per il visualizzatore video interattivo.
seo-title: disporre
solution: Experience Manager
title: disporre
topic: Dynamic media
uuid: 95046b8c-1277-4954-b13d-329994d0cb04
translation-type: tm+mt
source-git-commit: 16838d04b005224fad6df215ab5bf8c25ef86fc7

---


# disporre{#dispose}

Riferimento API JavaScript per il visualizzatore video interattivo.

`dispose()`

Dispone l’istanza del visualizzatore rilasciando tutte le risorse utilizzate dalla logica del visualizzatore ed eliminando tutti gli oggetti e i componenti interni creati dal visualizzatore in fase di esecuzione.

Il codice della pagina Web deve anche eliminare la variabile di istanza del visualizzatore per rimuovere completamente il visualizzatore dalla memoria del browser Web.

Se il codice della pagina Web ha registrato i listener di eventi direttamente sui componenti SDK per visualizzatori utilizzati dal visualizzatore o memorizzati i riferimenti esterni a tali componenti, tali listener devono essere esplicitamente cancellati dal codice della pagina Web e tali riferimenti esterni devono essere eliminati prima della chiamata `dispose()`.

Non accedete più all’API del visualizzatore dopo `dispose()` la chiamata.

## Parametri {#section-ad069aaaf4f145f2b50ae5ac89ca1ed2}

Nessuno.

## Restituisce {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Nessuno.

## Esempio {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.dispose()
```

