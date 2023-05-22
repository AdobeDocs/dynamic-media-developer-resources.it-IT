---
title: eliminare
description: Riferimento API JavaScript per Visualizzatore file multimediali diversi.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: e09f73a9-a961-4188-b092-f7bbcae4946d
source-git-commit: cdc85af782ebc492ae2303469a7f4f54b5bc09c8
workflow-type: tm+mt
source-wordcount: '126'
ht-degree: 2%

---

# eliminare{#dispose}

Riferimento API JavaScript per Visualizzatore file multimediali diversi.

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
