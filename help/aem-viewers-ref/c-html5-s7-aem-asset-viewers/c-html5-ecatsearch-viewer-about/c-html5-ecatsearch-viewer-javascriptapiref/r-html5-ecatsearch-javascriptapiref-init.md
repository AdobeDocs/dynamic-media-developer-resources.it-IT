---
description: Riferimento API JavaScript per il visualizzatore di eCatalog.
solution: Experience Manager
title: init
feature: Dynamic Media Classic,Visualizzatori,SDK/API,Ricerca eCatalog
role: Developer,Business Practitioner
exl-id: 4d71062c-fee7-4339-bd7f-1b7f778465c4
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '127'
ht-degree: 2%

---

# init{#init}

Riferimento API JavaScript per il visualizzatore di eCatalog.

[!DNL `init()`]

Avvia l&#39;inizializzazione del visualizzatore di eCatalog. A questo punto, l’elemento DOM del contenitore deve essere creato in modo che il codice del visualizzatore possa trovarlo in base al suo ID.

Se l&#39;elemento contenitore non fa ancora parte del layout della pagina web (ad esempio, potrebbe essere nascosto utilizzando lo stile [!DNL `display:none`] assegnatogli), il visualizzatore sospende il processo di inizializzazione fino al momento in cui la pagina web riporta l&#39;elemento contenitore al layout. In questo caso, il caricamento del visualizzatore riprende automaticamente.

Chiamare questo metodo una sola volta durante il ciclo di vita del visualizzatore; le chiamate successive vengono ignorate.

## Parametri {#section-ad069aaaf4f145f2b50ae5ac89ca1ed2}

Nessuno.

## Restituisce {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

[!DNL `{Object}`] Un riferimento all’istanza del visualizzatore.

## Esempio {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.init()
```
