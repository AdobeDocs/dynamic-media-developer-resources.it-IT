---
description: Gestione delle etichette di pagina
solution: Experience Manager
title: Gestione delle etichette di pagina
feature: Dynamic Media Classic,Visualizzatori,SDK/API,Ricerca eCatalog
role: Developer,User
exl-id: 73c3904f-678f-47c4-b895-86671402df79
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '271'
ht-degree: 0%

---

# Gestione delle etichette di pagina{#managing-page-labels}

Nell’interfaccia utente del visualizzatore sono disponibili due posizioni in cui vengono visualizzate le etichette di pagina: modalità miniature e elenco a discesa del sommario.

È possibile definire tre tipi di etichette:

* Etichette definite dall&#39;autore utilizzando il meccanismo di localizzazione SYMBOL .
* Etichette definite dall’autore sul backend, in Dynamic Media Classic.
* Etichette generate automaticamente dal visualizzatore.

Le etichette basate su SYMBOL sono definite utilizzando `MediaSet.LABEL_XX[_YY]` e `MediaSet.LABEL_DELIM` SYMBOL come descritto in [Localizzazione degli elementi dell&#39;interfaccia utente](../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74). È possibile definire tali etichette per l&#39;intera estensione ecatalog, nel qual caso si dovrebbe utilizzare la sintassi SYMBOL breve ( `MediaSet.LABEL_XX`). Oppure, specificalo singolarmente per ogni pagina utilizzando la sintassi SYMBOL completa ( `MediaSet.LABEL_XX_YY`).

Quando definisci le etichette per entrambe le pagine nel set di pagine affiancate ecatalog, il visualizzatore concatena queste etichette in una stringa utilizzando `MediaSet.LABEL_DELIM` SYMBOL. Le etichette basate su SYMBOL hanno la precedenza sulle etichette definite sul backend o generate automaticamente dal visualizzatore.

Le etichette definite in Dynamic Media Classic sono memorizzate nel record UserData delle singole immagini di pagina. Come per le etichette basate su SYMBOL. In altre parole, se entrambe le pagine nella estensione ecatalog hanno delle etichette definite, vengono concatenate utilizzando `MediaSet.LABEL_DELIM` SYMBOL in modalità orizzontale. Le etichette di Dynamic Media Classic hanno la precedenza sulle etichette generate automaticamente, ma sono sostituite dalle etichette basate su SYMBOL.

Le etichette generate automaticamente sono numeri sequenziali assegnati a tutte le pagine dell’ecatalog. Le etichette generate automaticamente vengono ignorate per la diffusione specificata se sono definite etichette basate su SYMBOL o etichette Dynamic Media Classic.

Nel sommario è possibile disabilitare la visualizzazione delle etichette generate automaticamente utilizzando il parametro `showdefault` .
