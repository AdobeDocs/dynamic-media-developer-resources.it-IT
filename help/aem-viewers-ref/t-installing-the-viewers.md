---
title: Installazione di più visualizzatori Dynamic Media sullo stesso server
description: Istruzioni per l'installazione dell'API dei visualizzatori Dynamic Media.
solution: Experience Manager
topic: Dynamic Media
translation-type: tm+mt
source-git-commit: 07eb6cf84a46753b41307187d5c5b2a077fa9009
workflow-type: tm+mt
source-wordcount: '162'
ht-degree: 1%

---


# Installazione di più visualizzatori sullo stesso server{#installing-multiple-viewers-on-the-same-server}

<!-- Updated January 13, 2021 from https://wiki.corp.adobe.com/pages/viewpage.action?spaceKey=scene7qa&title=s7Viewers%2C+S7SDK%2C+S7OnDemand+Release+Notes - Contact is Sasha -->

Istruzioni per l&#39;installazione dell&#39;API visualizzatori Dynamic Media.

Installate e verificate il server immagini prima di installare i visualizzatori Image Server.

Copiate i file dei visualizzatori IS sul disco rigido, quindi distribuite il file `s7viewers.war` nella directory `../ImageServing/webapps`. Per istruzioni su come implementare, avviare, arrestare e gestire il server immagini, consultate la documentazione di Image Server.

>[!NOTE]
>
>Non è disponibile un aggiornamento per i visualizzatori Image Server.  Adobe consiglia di eseguire il backup di qualsiasi directory di visualizzatori Dynamic Media (s7viewers) esistente prima di continuare l&#39;installazione.

**Per installare più visualizzatori sullo stesso server**

1. Rinominare il visualizzatore .war nel contesto desiderato e distribuire il file nella posizione desiderata.
1. Impostate il parametro `this.isViewerRoot` in `config.js`.
1. Aprite `config.js` nella directory principale della cartella del visualizzatore appena creata.
1. Impostate il parametro `this.isViewerRoot = "/s7viewers"` nel contesto del file `s7viewers.war`. Ad esempio, `"/s7viewers-4.0"`.
1. Salvate il file e chiudete.
