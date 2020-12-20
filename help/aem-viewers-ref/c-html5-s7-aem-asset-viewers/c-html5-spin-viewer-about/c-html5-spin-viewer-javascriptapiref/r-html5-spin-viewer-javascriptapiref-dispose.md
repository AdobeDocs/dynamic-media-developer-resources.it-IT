---
description: Riferimento API JavaScript per il visualizzatore 360 gradi.
seo-description: Riferimento API JavaScript per il visualizzatore 360 gradi.
seo-title: disporre
solution: Experience Manager
title: disporre
topic: Dynamic media
uuid: c92c82b4-3a1a-4cbe-ad16-aa00322889e1
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---


# dispose{#dispose}

Riferimento API JavaScript per il visualizzatore 360 gradi.

`dispose()`

Dispone l’istanza del visualizzatore rilasciando tutte le risorse utilizzate dalla logica del visualizzatore ed eliminando tutti gli oggetti e i componenti interni creati dal visualizzatore in fase di esecuzione.

Il codice della pagina Web deve anche eliminare la variabile di istanza del visualizzatore per rimuovere completamente il visualizzatore dalla memoria del browser Web.

Se il codice della pagina Web ha registrato i listener di eventi direttamente sui componenti SDK per visualizzatori utilizzati dal visualizzatore o memorizzati i riferimenti esterni a tali componenti, tali listener devono essere esplicitamente deregistrati dal codice della pagina Web e tali riferimenti esterni devono essere eliminati prima di chiamare `dispose()`.

Non accedete più all&#39;API del visualizzatore dopo la chiamata di `dispose()`.

## Parametri {#section-ad069aaaf4f145f2b50ae5ac89ca1ed2}

Nessuno.

## Restituisce {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Nessuno.

## Esempio {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.dispose()
```

