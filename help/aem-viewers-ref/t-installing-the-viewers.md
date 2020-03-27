---
description: Istruzioni per l’installazione dell’API dei visualizzatori Scene7.
seo-description: Istruzioni per l’installazione dell’API dei visualizzatori Scene7.
seo-title: Installazione di più visualizzatori sullo stesso server
solution: Experience Manager
title: Installazione di più visualizzatori sullo stesso server
topic: Dynamic media
uuid: 91ae8eb5-1d23-4fa3-a0d6-a4a0ed0eb104
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Installazione di più visualizzatori sullo stesso server{#installing-multiple-viewers-on-the-same-server}

Istruzioni per l’installazione dell’API dei visualizzatori Scene7.

Installate e verificate il server immagini prima di installare i visualizzatori Image Server.

Copiate i file IS Viewers sul disco rigido e quindi distribuite il `s7viewers.war` file nella `../ImageServing/webapps` directory. Per istruzioni su come implementare, avviare, arrestare e gestire il server immagini, consultate la documentazione di Image Server.

>[!NOTE]
>
>Non è disponibile un aggiornamento per i visualizzatori Image Server. Prima di continuare l’installazione, Adobe consiglia di eseguire il backup di qualsiasi directory di visualizzatori Scene7 esistente.

**Per installare i visualizzatori sullo stesso server**

1. Rinominare il visualizzatore .war nel contesto desiderato e distribuire il file nella posizione desiderata.
1. Impostate `this.isViewerRoot` il parametro in `config.js`.
1. Aprite `config.js` il percorso nella directory principale della cartella appena creata del visualizzatore.
1. Impostate il parametro `this.isViewerRoot = "/s7viewers"` sul contesto del `s7viewers.war` file. Ad esempio, `"/s7viewers-4.0"`. Salvate e chiudete il file.
1. Salvate il file e chiudete.
