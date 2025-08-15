---
title: disporre
description: JavaScript riferimento API per Visualizzatore panoramico.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Panoramic
role: Developer,User
exl-id: 4e6ad465-36df-49e2-8c9e-722e8aa9063e
source-git-commit: 8aebcacd5abdc23565aab1bc3506c36f055b6439
workflow-type: tm+mt
source-wordcount: '124'
ht-degree: 0%

---

# disporre{#dispose}

JavaScript riferimento API per Visualizzatore panoramico.

`dispose()`

Elimina questa istanza visualizzatore rilasciando tutte le risorse utilizzate dalla logica di visualizzatore ed eliminando tutti gli oggetti e i componenti interni creati dal visualizzatore in fase di esecuzione.

Il codice della pagina Web dovrebbe anche eliminare la variabile istanza visualizzatore per rimuovere completamente il visualizzatore dalla memoria del browser Web.

Se il codice della pagina Web dispone di listener di eventi registrati direttamente nei componenti SDK del visualizzatore utilizzati dall&#39;visualizzatore o ha memorizzato riferimenti esterni a tali componenti, tali listener devono essere esplicitamente annullati dal codice della pagina Web. Inoltre, tali riferimenti a componenti esterni devono essere eliminati prima di chiamare `dispose()`.

Non accesso più l&#39;API del visualizzatore dopo `dispose()` che è stata chiamata.

## Parametri {#section-ad069aaaf4f145f2b50ae5ac89ca1ed2}

Nessuno.

## Rendiconto {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Nessuno.

## Esempio {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.dispose()
```
