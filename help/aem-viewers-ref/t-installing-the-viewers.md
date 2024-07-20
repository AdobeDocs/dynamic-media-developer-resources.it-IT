---
title: Installazione di più visualizzatori Dynamic Medie sullo stesso server
description: Istruzioni per l’installazione dell’API dei visualizzatori Dynamic Medie.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API
role: Developer,User
exl-id: 7a8d7205-d3bf-4ca8-b80a-9072436a3df5
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '160'
ht-degree: 0%

---

# Installazione di più visualizzatori sullo stesso server{#installing-multiple-viewers-on-the-same-server}

<!-- Updated April 06, 2021 from https://wiki.corp.adobe.com/pages/viewpage.action?spaceKey=scene7qa&title=s7Viewers%2C+S7SDK%2C+S7OnDemand+Release+Notes - Contact is Sasha -->

Istruzioni per l’installazione dell’API dei visualizzatori Dynamic Medie.

Installa e verifica Image Server prima di installare i visualizzatori Image Server.

Copiare i file dei visualizzatori IS sul disco rigido e quindi distribuire il file `s7viewers.war` nella directory `../ImageServing/webapps`. Consulta la documentazione di Image Server per istruzioni su come distribuire, avviare, arrestare e gestire il server immagini.

>[!NOTE]
>
>Non è disponibile alcuna installazione di aggiornamento per i visualizzatori Image Server. L’Adobe consiglia di eseguire il backup di qualsiasi directory dei visualizzatori Dynamic Medie (s7viewers) esistente prima di continuare con l’installazione.

**Per installare più visualizzatori sullo stesso server:**

1. Rinomina il visualizzatore .war nel contesto desiderato e distribuisci il file nel percorso desiderato.
1. Imposta il parametro `this.isViewerRoot` in `config.js`.
1. Apri `config.js` nella directory principale della cartella del visualizzatore appena creata.
1. Impostare il parametro `this.isViewerRoot = "/s7viewers"` nel contesto del file `s7viewers.war`. Ad esempio, `"/s7viewers-4.0"`.
1. Salva il file e chiudi.
