---
description: Questa documentazione spiega come amministrare il server di rendering immagini Dynamic Media.
seo-description: Questa documentazione spiega come amministrare il server di rendering immagini Dynamic Media.
seo-title: Panoramica dell'amministrazione del server
solution: Experience Manager
title: Panoramica dell'amministrazione del server
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 83aa83b7-bb7a-4bbd-923c-dd69763fe9c9
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '178'
ht-degree: 0%

---


# Panoramica sull&#39;amministrazione del server{#server-administration-overview}

Questa documentazione spiega come amministrare il server di rendering immagini Dynamic Media.

Il rendering delle immagini è composto da due componenti principali:

* Un pacchetto Java viene distribuito con Image Server Platform Server e gestisce la connessione client, il caching e i cataloghi dei materiali.
* Un modulo di codice nativo viene distribuito come libreria di estensioni per il server immagini e implementa le funzionalità di rendering delle immagini di base.

Entrambi i componenti sono denominati collettivamente *Server di rendering*.

Image Rendering condivide molte funzionalità server con Image Server e tutte le opzioni sono configurate modificando un file di configurazione. Gli attributi di configurazione aggiuntivi sono forniti dal catalogo predefinito ( [!DNL default.ini]) o da specifici cataloghi di materiali. Consultate Cataloghi materiali per ulteriori dettagli.

La cartella di installazione di Image Rendering ( *[!DNL install_folder]*) è [!DNL *[!DNL install_root]*/ImageRendering]. In Windows, il valore predefinito *[!DNL install_root]* è `C:\Program Files\Scene7`. Durante l’installazione è possibile specificare una cartella diversa. In Linux, *[!DNL install_root]* deve sempre essere [!DNL /usr/local/scene7]. È possibile utilizzare collegamenti simbolici.

Tutti i percorsi dei file sono con distinzione tra maiuscole e minuscole in UNIX e in Windows.
