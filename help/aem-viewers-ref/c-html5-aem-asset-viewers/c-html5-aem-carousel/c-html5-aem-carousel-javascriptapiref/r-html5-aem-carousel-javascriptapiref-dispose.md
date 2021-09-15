---
title: disporre
description: Riferimento API JavaScript per il visualizzatore Carosello.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Carousel Banners
role: Developer,User
exl-id: 64e9f83f-e17e-4544-825a-fd458e15fdb5
source-git-commit: 96ac67e5645c2c55920cc971806ba2f14ae57044
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# disporre{#dispose}

Riferimento API JavaScript per il visualizzatore Carosello.

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
