---
title: disporre
description: Riferimento API JavaScript per il visualizzatore di immagini video.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Images
role: Developer,User
exl-id: 8af8506e-6b29-45ea-a70b-3eb3b2995047
source-git-commit: 24667a5ebab54ba22c4a3f6b52d19d7a31a93576
workflow-type: tm+mt
source-wordcount: '126'
ht-degree: 3%

---

# disporre{#dispose}

Riferimento API JavaScript per il visualizzatore di immagini video.

`dispose()`

Dispone questa istanza del visualizzatore rilasciando tutte le risorse utilizzate dalla logica del visualizzatore ed eliminando tutti gli oggetti interni e i componenti creati dal visualizzatore in fase di esecuzione.

Il codice della pagina web dovrebbe anche eliminare la variabile dell’istanza del visualizzatore e rimuovere completamente il visualizzatore dalla memoria del browser web.

Se il codice della pagina web ha registrato listener di eventi direttamente sui componenti SDK per visualizzatori utilizzati dal visualizzatore, o memorizzato riferimenti esterni a tali componenti, tali listener devono essere esplicitamente deregistrati dal codice della pagina web. Inoltre, tali riferimenti ai componenti esterni devono essere eliminati prima di chiamare `dispose()`.

Non accedere più all’API del visualizzatore dopo la chiamata di `dispose()`.

## Parametri {#section-ad069aaaf4f145f2b50ae5ac89ca1ed2}

Nessuno.

## Restituisce {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Nessuno.

## Esempio {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.dispose()
```
