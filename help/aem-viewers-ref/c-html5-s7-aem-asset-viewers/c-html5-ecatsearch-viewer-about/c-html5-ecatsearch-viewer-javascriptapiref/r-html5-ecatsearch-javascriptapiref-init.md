---
title: init
description: Riferimento API di JavaScript per il visualizzatore eCatalog.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: 4d71062c-fee7-4339-bd7f-1b7f778465c4
TQID: 'https://experienceleague.adobe.com/Hb-C6aORHF8--oX3IqgRZIi1rfbLg39F0Ewzb4sg45U'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 123
ht-degree: 0%

---

# init{#init}

Riferimento API di JavaScript per il visualizzatore eCatalog.

[!DNL `init()`]

Avvia l&#39;inizializzazione del visualizzatore eCatalog. A questo punto, è necessario creare l’elemento DOM del contenitore in modo che il codice del visualizzatore possa trovarlo in base al suo ID.

Se l&#39;elemento contenitore non fa ancora parte del layout della pagina Web, ad esempio potrebbe essere nascosto utilizzando lo stile [!DNL `display:none`] assegnato, il visualizzatore sospende il processo di inizializzazione. Lo fa fino al momento in cui la pagina web riporta l’elemento contenitore al layout. Quando si verifica questo evento, il caricamento del visualizzatore riprende automaticamente.

Chiama questo metodo una sola volta durante il ciclo di vita del visualizzatore; le chiamate successive vengono ignorate.

## Parametri {#section-ad069aaaf4f145f2b50ae5ac89ca1ed2}

Nessuno.

## Restituisce {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

[!DNL `{Object}`] Riferimento all&#39;istanza del visualizzatore.

## Esempio {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.init()
```
