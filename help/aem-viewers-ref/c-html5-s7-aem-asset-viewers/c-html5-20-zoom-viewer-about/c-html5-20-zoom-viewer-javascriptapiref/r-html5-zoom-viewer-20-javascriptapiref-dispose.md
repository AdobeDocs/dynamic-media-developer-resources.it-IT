---
title: eliminare
description: Riferimento API JavaScript per Visualizzatore zoom.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: c796943e-8ea8-4a97-a1ff-09676204150a
source-git-commit: ec2a15e2e76bae5da4fbabc9b6912b12dc080f66
workflow-type: tm+mt
source-wordcount: '124'
ht-degree: 2%

---

# eliminare{#dispose}

Riferimento API JavaScript per Visualizzatore zoom.

`dispose()`

Dispone di questa istanza del visualizzatore rilasciando tutte le risorse utilizzate dalla logica del visualizzatore ed eliminando tutti gli oggetti e i componenti interni creati dal visualizzatore in fase di esecuzione.

Il codice della pagina web deve anche eliminare la variabile dell’istanza del visualizzatore e rimuovere completamente il visualizzatore dalla memoria del browser web.

Se il codice della pagina web contiene listener di eventi registrati direttamente sui componenti SDK del visualizzatore utilizzati dal visualizzatore, o riferimenti esterni memorizzati a tali componenti, tali listener devono essere esplicitamente annullati dal codice della pagina web. E, tali riferimenti a componenti esterni devono essere eliminati prima di richiamare `dispose()`.

Non accedere più all’API del visualizzatore dopo `dispose()` viene chiamato.

## Parametri {#section-ad069aaaf4f145f2b50ae5ac89ca1ed2}

Nessuno.

## Restituisce {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Nessuno.

## Esempio {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.dispose()
```
