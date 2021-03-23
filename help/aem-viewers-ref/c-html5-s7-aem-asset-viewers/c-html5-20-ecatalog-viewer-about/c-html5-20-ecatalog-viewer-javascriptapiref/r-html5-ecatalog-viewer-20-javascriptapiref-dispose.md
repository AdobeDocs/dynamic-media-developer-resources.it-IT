---
description: Riferimento API JavaScript per il visualizzatore di eCatalog.
seo-description: Riferimento API JavaScript per il visualizzatore di eCatalog.
seo-title: disporre
solution: Experience Manager
title: disporre
uuid: b2073d03-a0a0-4f55-a350-7336ddcf031d
feature: Dynamic Media Classic,Visualizzatori,SDK/API,eCatalog
role: Sviluppatore, Business Practices
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '141'
ht-degree: 2%

---


# dispose{#dispose}

Riferimento API JavaScript per il visualizzatore di eCatalog.

`dispose()`

Dispone questa istanza del visualizzatore rilasciando tutte le risorse utilizzate dalla logica del visualizzatore ed eliminando tutti gli oggetti interni e i componenti creati dal visualizzatore in fase di esecuzione.

Il codice della pagina web dovrebbe anche eliminare la variabile dell’istanza del visualizzatore e rimuovere completamente il visualizzatore dalla memoria del browser web.

Se il codice della pagina web ha registrato ascoltatori di eventi direttamente sui componenti SDK del visualizzatore utilizzati dal visualizzatore, o ha memorizzato riferimenti esterni a tali componenti, tali listener devono essere cancellati esplicitamente dal codice della pagina web e tali riferimenti a componenti esterni devono essere eliminati prima di chiamare `dispose()`.

Non accedere più all’API del visualizzatore dopo la chiamata di `dispose()` .

## Parametri {#section-ad069aaaf4f145f2b50ae5ac89ca1ed2}

Nessuno.

## Restituisce {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Nessuno.

## Esempio {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.dispose()
```

