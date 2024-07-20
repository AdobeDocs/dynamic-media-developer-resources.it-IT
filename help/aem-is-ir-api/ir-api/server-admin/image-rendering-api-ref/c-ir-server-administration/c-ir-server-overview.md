---
description: In questa documentazione viene illustrato come amministrare il server Dynamic Medie Image Rendering.
solution: Experience Manager
title: Panoramica sull'amministrazione del server
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 294cd068-8676-4932-a3ad-1a3c5bfa691e
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '161'
ht-degree: 0%

---

# Panoramica sull&#39;amministrazione del server{#server-administration-overview}

In questa documentazione viene illustrato come amministrare il server Dynamic Medie Image Rendering.

Image Rendering è costituito da due componenti principali:

* Un pacchetto Java viene distribuito con Image Server [!DNL Platform Server] e gestisce la connessione client, il caching e i cataloghi di materiale.
* Un modulo di codice nativo viene distribuito come libreria di estensioni per il server immagini e implementa le funzionalità di rendering delle immagini di base.

Entrambi i componenti sono denominati collettivamente *Server di rendering*.

Image Rendering condivide molte funzionalità server con Image Server e tutte le opzioni sono configurate modificando un file di configurazione. Attributi di configurazione aggiuntivi vengono forniti dal catalogo predefinito ( [!DNL default.ini]) o da cataloghi di materiale specifici. Per ulteriori informazioni, consulta Cataloghi materiali.

La cartella di installazione del rendering immagini ( *[!DNL install_folder]*) è [!DNL *[!DNL install_root]*/ImageRendering]. In Windows, il valore predefinito *[!DNL install_root]* è `C:\Program Files\Scene7`. È possibile specificare una cartella diversa durante l&#39;installazione. In Linux, *[!DNL install_root]* deve essere sempre [!DNL /usr/local/scene7]. Possono essere utilizzati collegamenti simbolici.

Tutti i percorsi dei file fanno distinzione tra maiuscole e minuscole in UNIX e non in Windows.
