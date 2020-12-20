---
description: Riferimento API JavaScript per il visualizzatore di eCatalog.
seo-description: Riferimento API JavaScript per il visualizzatore di eCatalog.
seo-title: init
solution: Experience Manager
title: init
topic: Dynamic media
uuid: b01f1497-8bee-4e01-8f92-272b324cb2dd
translation-type: tm+mt
source-git-commit: 2bd5b17e473ec53844b4bbcb4f13580b2d6bfaf4
workflow-type: tm+mt
source-wordcount: '126'
ht-degree: 2%

---


# init{#init}

Riferimento API JavaScript per il visualizzatore di eCatalog.

[!DNL `init()`]

Avvia l’inizializzazione del visualizzatore di eCatalog. Per questa volta è necessario creare l’elemento DOM contenitore in modo che il codice del visualizzatore possa trovarlo in base al suo ID.

Se l&#39;elemento contenitore non fa ancora parte del layout della pagina Web (ad esempio, potrebbe essere nascosto utilizzando lo stile [!DNL `display:none`] assegnatogli), il visualizzatore sospende il processo di inizializzazione fino al momento in cui la pagina Web riporta l&#39;elemento contenitore al layout. In questo caso, il caricamento del visualizzatore riprende automaticamente.

Chiamare questo metodo una sola volta durante il ciclo di vita del visualizzatore; le chiamate successive vengono ignorate.

## Parametri {#section-ad069aaaf4f145f2b50ae5ac89ca1ed2}

Nessuno.

## Restituisce {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

[!DNL `{Object}`] Un riferimento all’istanza del visualizzatore.

## Esempio {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.init()
```

