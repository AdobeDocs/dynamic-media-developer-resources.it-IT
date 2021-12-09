---
title: disporre
description: Riferimento API JavaScript per il visualizzatore di eCatalog.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: 827decd9-1f6c-4ac1-8fcc-acc93cfb859d
source-git-commit: edc127dc6e2ae2d9bd5feed08c8bc896c8c39747
workflow-type: tm+mt
source-wordcount: '124'
ht-degree: 3%

---

# disporre{#dispose}

Riferimento API JavaScript per il visualizzatore di eCatalog.

`dispose()`

Dispone questa istanza del visualizzatore rilasciando tutte le risorse utilizzate dalla logica del visualizzatore ed eliminando tutti gli oggetti interni e i componenti creati dal visualizzatore in fase di esecuzione.

Il codice della pagina web dovrebbe anche eliminare la variabile dell’istanza del visualizzatore e rimuovere completamente il visualizzatore dalla memoria del browser web.

Se il codice della pagina web ha registrato listener di eventi direttamente sui componenti SDK per visualizzatori utilizzati dal visualizzatore, o memorizzato riferimenti esterni a tali componenti, tali listener devono essere esplicitamente deregistrati dal codice della pagina web. Inoltre, tali riferimenti esterni devono essere eliminati prima di richiamare `dispose()`.

Non accedere più all’API del visualizzatore dopo `dispose()` viene chiamato.

## Parametri {#section-ad069aaaf4f145f2b50ae5ac89ca1ed2}

Nessuno.

## Restituisce {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Nessuno.

## Esempio {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.dispose()
```
