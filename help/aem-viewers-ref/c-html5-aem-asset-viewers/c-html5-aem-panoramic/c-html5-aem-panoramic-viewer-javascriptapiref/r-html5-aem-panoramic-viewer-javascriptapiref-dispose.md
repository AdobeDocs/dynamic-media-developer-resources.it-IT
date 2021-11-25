---
title: disporre
description: Riferimento API JavaScript per il visualizzatore panoramico.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Panoramic
role: Developer,User
exl-id: 4e6ad465-36df-49e2-8c9e-722e8aa9063e
source-git-commit: 8aebcacd5abdc23565aab1bc3506c36f055b6439
workflow-type: tm+mt
source-wordcount: '124'
ht-degree: 3%

---

# disporre{#dispose}

Riferimento API JavaScript per il visualizzatore panoramico.

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
