---
title: eliminare
description: Riferimento API di JavaScript per il visualizzatore eCatalog.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: 827decd9-1f6c-4ac1-8fcc-acc93cfb859d
source-git-commit: edc127dc6e2ae2d9bd5feed08c8bc896c8c39747
workflow-type: tm+mt
source-wordcount: '124'
ht-degree: 0%

---

# eliminare{#dispose}

Riferimento API di JavaScript per il visualizzatore eCatalog.

`dispose()`

Dispone di questa istanza del visualizzatore rilasciando tutte le risorse utilizzate dalla logica del visualizzatore ed eliminando tutti gli oggetti e i componenti interni creati dal visualizzatore in fase di esecuzione.

Il codice della pagina web deve anche eliminare la variabile dell’istanza del visualizzatore e rimuovere completamente il visualizzatore dalla memoria del browser web.

Se il codice della pagina web contiene listener di eventi registrati direttamente sui componenti del Visualizzatore SDK utilizzati dal visualizzatore, o riferimenti esterni memorizzati a tali componenti, tali listener devono essere esplicitamente annullati dal codice della pagina web. Inoltre, tali riferimenti a componenti esterni devono essere eliminati prima di chiamare `dispose()`.

Non accedere più all&#39;API del visualizzatore dopo la chiamata di `dispose()`.

## Parametri {#section-ad069aaaf4f145f2b50ae5ac89ca1ed2}

Nessuno.

## Restituisce {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Nessuno.

## Esempio {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.dispose()
```
