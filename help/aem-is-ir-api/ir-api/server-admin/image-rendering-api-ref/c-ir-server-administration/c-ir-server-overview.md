---
description: Questa documentazione spiega come amministrare il server di rendering delle immagini Dynamic Media.
solution: Experience Manager
title: Panoramica sull'amministrazione del server
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 294cd068-8676-4932-a3ad-1a3c5bfa691e
TQID: 'https://experienceleague.adobe.com/t9zGehwMxhHq1HrP3mmNGvkthmqYxX2ijeyihn5OEWI'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 163
ht-degree: 0%

---

# Panoramica sull&#39;amministrazione del server{#server-administration-overview}

Questa documentazione spiega come amministrare il server di rendering delle immagini Dynamic Media.

Image Rendering è costituito da due componenti principali:

* Un pacchetto Java viene distribuito con Image Server [!DNL Platform Server] e gestisce la connessione client, il caching e i cataloghi di materiale.
* Un modulo di codice nativo viene distribuito come libreria di estensioni per il server immagini e implementa le funzionalità di rendering delle immagini di base.

Entrambi i componenti sono denominati collettivamente *Server di rendering*.

Image Rendering condivide molte funzionalità server con Image Server e tutte le opzioni sono configurate modificando un file di configurazione. Attributi di configurazione aggiuntivi vengono forniti dal catalogo predefinito ( [!DNL default.ini]) o da cataloghi di materiale specifici. Per ulteriori informazioni, consulta Cataloghi materiali.

La cartella di installazione del rendering immagini ( *[!DNL install_folder]*) è [!DNL *[!DNL install_root]*/ImageRendering]. In Windows, il valore predefinito *[!DNL install_root]* è `C:\Program Files\Scene7`. È possibile specificare una cartella diversa durante l&#39;installazione. In Linux, *[!DNL install_root]* deve essere sempre [!DNL /usr/local/scene7]. Possono essere utilizzati collegamenti simbolici.

Tutti i percorsi dei file fanno distinzione tra maiuscole e minuscole in UNIX e non in Windows.
