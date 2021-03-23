---
description: Questa documentazione spiega come amministrare il server Dynamic Media Image Rendering .
seo-description: Questa documentazione spiega come amministrare il server Dynamic Media Image Rendering .
seo-title: Panoramica sull'amministrazione del server
solution: Experience Manager
title: Panoramica sull'amministrazione del server
uuid: 83aa83b7-bb7a-4bbd-923c-dd69763fe9c9
feature: Dynamic Media Classic, SDK/API
role: Sviluppatore, amministratore, Business Practices
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '187'
ht-degree: 0%

---


# Panoramica sull&#39;amministrazione del server{#server-administration-overview}

Questa documentazione spiega come amministrare il server Dynamic Media Image Rendering .

Image Rendering è costituito da due componenti principali:

* Un pacchetto Java viene distribuito con il server della piattaforma Image Server e gestisce le connessioni client, la memorizzazione in cache e i cataloghi di materiale.
* Un modulo di codice nativo viene distribuito come libreria di estensioni per Image Server e implementa le funzionalità di rendering delle immagini di base.

Entrambi i componenti sono chiamati collettivamente *Server di rendering*.

Image Rendering condivide molte funzionalità del server con Image Server e tutte le opzioni sono configurate modificando un file di configurazione. Gli attributi di configurazione aggiuntivi vengono forniti dal catalogo predefinito ( [!DNL default.ini]) o da cataloghi di materiali specifici. Per ulteriori informazioni, consulta Cataloghi dei materiali .

La cartella di installazione di Image Rendering ( *[!DNL install_folder]*) è [!DNL *[!DNL install_root]*/ImageRendering]. In Windows, il valore predefinito *[!DNL install_root]* è `C:\Program Files\Scene7`. È possibile specificare una cartella diversa durante l&#39;installazione. Su Linux, *[!DNL install_root]* deve sempre essere [!DNL /usr/local/scene7]. È possibile utilizzare collegamenti simbolici.

Tutti i percorsi dei file sono sensibili all&#39;uso di maiuscole e minuscole in UNIX e non fanno distinzione tra maiuscole e minuscole in Windows.
