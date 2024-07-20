---
title: Gestione delle etichette delle pagine
description: Gestione delle etichette delle pagine
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: b62b5cb8-6100-4d0f-afd8-e6daa6ce6539
source-git-commit: a919130f0940d81a221b79563b6b3e41533ba788
workflow-type: tm+mt
source-wordcount: '263'
ht-degree: 0%

---

# Gestione delle etichette delle pagine{#managing-page-labels}

Nell’interfaccia utente del visualizzatore sono disponibili due posizioni in cui vengono visualizzate le etichette di pagina: modalità miniature e menu a discesa sommario.

È possibile definire tre tipi di etichette:

* Etichette definite dall’autore mediante il meccanismo di localizzazione dei SIMBOLI.
* Etichette definite dall’autore sul backend, all’interno di Dynamic Media Classic.
* Etichette generate automaticamente dal visualizzatore.

Le etichette basate su SIMBOLI sono definite utilizzando `MediaSet.LABEL_XX[_YY]` e `MediaSet.LABEL_DELIM` SIMBOLI come descritto in [Localizzazione degli elementi dell&#39;interfaccia utente](../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74). È possibile definire tali etichette per l&#39;intera distribuzione ecatalog, nel qual caso è necessario utilizzare la sintassi SYMBOL breve ( `MediaSet.LABEL_XX`). In alternativa, specificarlo per ogni singola pagina utilizzando la sintassi SYMBOL completa ( `MediaSet.LABEL_XX_YY`).

Quando si definiscono le etichette per entrambe le pagine nel set di pagine affiancate dell&#39;ecatalog, il visualizzatore concatena queste etichette in una stringa utilizzando il SIMBOLO `MediaSet.LABEL_DELIM`. Le etichette basate su SIMBOLI hanno la precedenza su quelle definite nel backend o generate automaticamente dal visualizzatore.

Le etichette definite in Dynamic Media Classic vengono memorizzate nel record UserData delle singole immagini di pagina. Come per le etichette basate su SIMBOLI. In altre parole, se entrambe le pagine del catalogo hanno etichette definite, vengono concatenate utilizzando il SIMBOLO `MediaSet.LABEL_DELIM` in modalità orizzontale. Le etichette Dynamic Media Classic hanno la precedenza su quelle generate automaticamente, ma sono sostituite da etichette basate su SIMBOLI.

Le etichette generate automaticamente sono numeri sequenziali assegnati a tutte le pagine dell&#39;ecatalog. Le etichette generate automaticamente vengono ignorate per la distribuzione specificata se sono definite etichette basate su SIMBOLI o etichette Dynamic Media Classic.

Nel sommario è possibile disattivare la visualizzazione delle etichette generate automaticamente utilizzando il parametro `showdefault`.
