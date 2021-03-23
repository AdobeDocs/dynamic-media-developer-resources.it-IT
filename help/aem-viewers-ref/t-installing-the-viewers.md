---
title: Installazione di più visualizzatori Dynamic Media sullo stesso server
description: Istruzioni per l’installazione dell’API dei visualizzatori Dynamic Media.
solution: Experience Manager
feature: Dynamic Media Classic,Visualizzatori,SDK/API
role: Sviluppatore, Business Practices
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '171'
ht-degree: 1%

---


# Installazione di più visualizzatori sullo stesso server{#installing-multiple-viewers-on-the-same-server}

<!-- Updated January 13, 2021 from https://wiki.corp.adobe.com/pages/viewpage.action?spaceKey=scene7qa&title=s7Viewers%2C+S7SDK%2C+S7OnDemand+Release+Notes - Contact is Sasha -->

Istruzioni per l’installazione dell’API dei visualizzatori Dynamic Media.

Installa e verifica Image Serving prima di installare i visualizzatori Image Serving.

Copiare i file IS Viewers sul disco rigido e quindi distribuire il file `s7viewers.war` nella directory `../ImageServing/webapps`. Per istruzioni su come distribuire, avviare, interrompere e gestire il server immagini, consulta la documentazione di Image Server .

>[!NOTE]
>
>Non esiste un&#39;installazione di aggiornamento per i visualizzatori Image Server. Adobe consiglia di eseguire il backup di qualsiasi directory dei visualizzatori Dynamic Media (s7viewers) esistente prima di continuare l’installazione.

**Per installare più visualizzatori sullo stesso server**

1. Rinomina il visualizzatore .war nel contesto desiderato e distribuisci il file nella posizione desiderata.
1. Imposta il parametro `this.isViewerRoot` in `config.js`.
1. Apri `config.js` nella directory principale della cartella di visualizzatore appena creata.
1. Imposta il parametro `this.isViewerRoot = "/s7viewers"` nel contesto del file `s7viewers.war`. Ad esempio, `"/s7viewers-4.0"`.
1. Salva il file e chiudi.
