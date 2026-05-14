---
title: eliminare
description: Guida di riferimento dell'API JavaScript per il Visualizzatore immagini video.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Images
role: Developer,User
exl-id: 8af8506e-6b29-45ea-a70b-3eb3b2995047
TQID: 'https://experienceleague.adobe.com/UdBa-a0tF4sreueSd-MMna3lH1orbgVCb5w1N-LrL90'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 126
ht-degree: 0%

---

# eliminare{#dispose}

Guida di riferimento dell&#39;API JavaScript per il Visualizzatore immagini video.

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
