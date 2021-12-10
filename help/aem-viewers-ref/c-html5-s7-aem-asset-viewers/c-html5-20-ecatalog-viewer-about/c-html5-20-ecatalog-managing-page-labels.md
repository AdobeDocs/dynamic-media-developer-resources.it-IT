---
title: Gestione delle etichette di pagina
description: Gestione delle etichette di pagina
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: b62b5cb8-6100-4d0f-afd8-e6daa6ce6539
source-git-commit: a919130f0940d81a221b79563b6b3e41533ba788
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# Gestione delle etichette di pagina{#managing-page-labels}

Nell’interfaccia utente del visualizzatore sono disponibili due posizioni in cui vengono visualizzate le etichette di pagina: modalità miniature e elenco a discesa del sommario.

È possibile definire tre tipi di etichette:

* Etichette definite dall&#39;autore utilizzando il meccanismo di localizzazione SYMBOL .
* Etichette definite dall’autore sul backend, in Dynamic Media Classic.
* Etichette generate automaticamente dal visualizzatore.

Le etichette basate su SYMBOL sono definite utilizzando `MediaSet.LABEL_XX[_YY]` e `MediaSet.LABEL_DELIM` SYMBOL come descritto in [Localizzazione degli elementi dell’interfaccia utente](../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74). Puoi definire tali etichette per l&#39;intero spread ecatalog, nel qual caso devi usare una sintassi SYMBOL breve ( `MediaSet.LABEL_XX`). Oppure, specificalo singolarmente per ogni pagina utilizzando la sintassi SYMBOL completa ( `MediaSet.LABEL_XX_YY`).

Quando definisci le etichette per entrambe le pagine nel set di pagine affiancate ecatalog, il visualizzatore concatena queste etichette in un’unica stringa utilizzando `MediaSet.LABEL_DELIM` SIMBOLO. Le etichette basate su SYMBOL hanno la precedenza sulle etichette definite sul backend o generate automaticamente dal visualizzatore.

Le etichette definite in Dynamic Media Classic sono memorizzate nel record UserData delle singole immagini di pagina. Come per le etichette basate su SYMBOL. In altre parole, se entrambe le pagine nella distribuzione ecatalog hanno delle etichette definite, vengono concatenate utilizzando `MediaSet.LABEL_DELIM` SYMBOL in modalità orizzontale. Le etichette Dynamic Media Classic hanno la precedenza sulle etichette generate automaticamente, ma sono sostituite dalle etichette basate su SYMBOL.

Le etichette generate automaticamente sono numeri sequenziali assegnati a tutte le pagine dell’ecatalog. Le etichette generate automaticamente vengono ignorate per la distribuzione specificata se sono definite etichette basate su SYMBOL o etichette Dynamic Media Classic definite.

Nel sommario è possibile disattivare la visualizzazione delle etichette generate automaticamente utilizzando `showdefault` parametro .
