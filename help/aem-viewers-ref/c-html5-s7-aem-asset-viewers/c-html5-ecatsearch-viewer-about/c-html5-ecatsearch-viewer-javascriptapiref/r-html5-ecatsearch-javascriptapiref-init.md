---
description: Riferimento API JavaScript per il visualizzatore eCatalog.
solution: Experience Manager
title: init
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: 4d71062c-fee7-4339-bd7f-1b7f778465c4
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '119'
ht-degree: 1%

---

# init{#init}

Riferimento API JavaScript per il visualizzatore eCatalog.

[!DNL `init()`]

Avvia l&#39;inizializzazione del visualizzatore eCatalog. A questo punto è necessario creare l’elemento DOM del contenitore in modo che il codice del visualizzatore possa trovarlo in base al suo ID.

Se l’elemento contenitore non fa ancora parte del layout della pagina web (ad esempio, potrebbe essere nascosto tramite [!DNL `display:none`] ), il visualizzatore sospende il processo di inizializzazione fino al momento in cui la pagina web riporta l’elemento contenitore nel layout. In questo caso, il caricamento del visualizzatore riprende automaticamente.

Chiama questo metodo una sola volta durante il ciclo di vita del visualizzatore; le chiamate successive vengono ignorate.

## Parametri {#section-ad069aaaf4f145f2b50ae5ac89ca1ed2}

Nessuno.

## Restituisce {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

[!DNL `{Object}`] Riferimento all’istanza del visualizzatore.

## Esempio {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.init()
```
