---
description: 'null'
seo-description: 'null'
seo-title: Gestione delle etichette di pagina
solution: Experience Manager
title: Gestione delle etichette di pagina
topic: Dynamic media
uuid: 49444fe6-ef34-4e5b-a293-e23830a67b4d
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '265'
ht-degree: 0%

---


# Gestione delle etichette di pagina{#managing-page-labels}

Nell’interfaccia utente del visualizzatore sono disponibili due posizioni per le etichette di pagina: modalità miniature e menu a discesa del sommario.

È possibile definire tre tipi di etichette:

* Etichette definite dall&#39;autore mediante il meccanismo di localizzazione SYMBOL.
* Etichette definite dall&#39;autore sul back-end, all&#39;interno di Scene7 Publishing System.
* Etichette generate automaticamente dal visualizzatore.

Le etichette basate su SYMBOL sono definite utilizzando `MediaSet.LABEL_XX[_YY]` e `MediaSet.LABEL_DELIM` SIMBOLI come descritto in [Localizzazione di elementi dell&#39;interfaccia utente](../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74). Potete definire tali etichette per l&#39;intero set di pagine affiancate del catalogo, nel qual caso dovrete usare una sintassi SIMBOLO breve ( `MediaSet.LABEL_XX`). Oppure, specificatelo per ciascuna pagina singolarmente utilizzando la sintassi SYMBOL completa ( `MediaSet.LABEL_XX_YY`).

Quando definite le etichette per entrambe le pagine nelle pagine affiancate del catalogo, il visualizzatore concatena queste etichette in una stringa utilizzando `MediaSet.LABEL_DELIM` SYMBOL. Le etichette basate su SYMBOL hanno precedenza rispetto alle etichette definite sul backend o generate automaticamente dal visualizzatore.

Le etichette definite in Scene7 Publishing System sono memorizzate nel record UserData delle singole immagini di pagina. Come per le etichette basate su SYMBOL. Se entrambe le pagine del set di pagine affiancate del catalogo hanno delle etichette definite, vengono concatenate utilizzando `MediaSet.LABEL_DELIM` SYMBOL in modalità orizzontale. Le etichette di Scene7 Publishing System hanno precedenza rispetto alle etichette generate automaticamente, ma vengono sostituite dalle etichette basate su SYMBOL.

Le etichette generate automaticamente sono numeri sequenziali assegnati a tutte le pagine del catalogo. Le etichette generate automaticamente vengono ignorate per il set di pagine affiancate specificato se sono state definite etichette basate su SYMBOL o se sono state definite etichette di Scene7 Publishing System.

Nel sommario è possibile disattivare la visualizzazione delle etichette generate automaticamente utilizzando il parametro `showdefault`.
