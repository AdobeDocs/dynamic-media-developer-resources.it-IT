---
description: Questa documentazione spiega come amministrare il server Dynamic Media Image Rendering .
solution: Experience Manager
title: Panoramica sull'amministrazione del server
feature: Dynamic Media Classic, SDK/API
role: Developer,Admin,User
exl-id: 294cd068-8676-4932-a3ad-1a3c5bfa691e
source-git-commit: 38afaf2ed0f01868f02e236e941b23eed5b790aa
workflow-type: tm+mt
source-wordcount: '168'
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
