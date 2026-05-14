---
title: eliminare
description: Riferimento API di JavaScript per il visualizzatore panoramico.
solution: Experience Manager, Experience Manager Assets
feature-set: Experience Manager, Experience Manager Assets
feature: Dynamic Media Classic,Viewers,SDK/API
role: Developer,User
exl-id: 4e6ad465-36df-49e2-8c9e-722e8aa9063e
autotag-review: '2026-05-13T22:08:54.657Z'
TQID: 'https://experienceleague.adobe.com/LIJyXNIBKd304RTksUCnN-g5vQjWBTvC-VWQNIgeKjo'
product_v2: id: beaff0dd-a904-4c6b-8290-b527cd877d75id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
source-git-commit: e76d4c499daf8c8a7a0be31e56d84f917c643095
workflow-type: tm+mt
source-wordcount: 124
ht-degree: 0%

---

# eliminare{#dispose}

Riferimento API di JavaScript per il visualizzatore panoramico.

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
