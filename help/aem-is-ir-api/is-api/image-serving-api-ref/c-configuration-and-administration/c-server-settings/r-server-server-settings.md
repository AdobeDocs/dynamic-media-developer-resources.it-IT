---
description: Utilizzate queste impostazioni del server per configurare il server.
seo-description: Utilizzate queste impostazioni del server per configurare il server.
seo-title: Server
solution: Experience Manager
title: Server
topic: Scene7 Image Serving - Image Rendering API
uuid: 50db98cc-8354-4884-9416-00808828061b
translation-type: tm+mt
source-git-commit: e8e5b07329bde3e23ee095d5022da62d67e9478c
workflow-type: tm+mt
source-wordcount: '357'
ht-degree: 0%

---


# Server{#server}

Utilizzate queste impostazioni del server per configurare il server.

## SV::ImageServerMode - Image Server Mode {#section-991b287f2dde4f77a24fc69d5b32cabd}

Per Linux sono disponibili sia una versione a 32 che a 64 bit del server immagini. Specificate ImageServer64 se installato su server Linux a 64 bit oppure ImageServer32 (predefinito) se installato su server a 32 bit.

>[!NOTE]
>
>La versione a 64 bit del server immagini non supporta i file sorgente FlashPix.

>[!NOTE]
>
>La modalità a 64 bit non è supportata in Windows. È `ImageServer32` possibile specificare solo l&#39;oggetto. In caso contrario, Image Server non verrà avviato.

## SV::PsHeapSize - Platform Server Heap Size {#section-fd83715948764aeda58d6b3a9f9f8be9}

Dimensione heap Java per Platform Server. Il valore predefinito è &quot; `512m`&quot; (512 Mbyte).

## IS::TcpPort, PS::isConnection.port - Porta di ascolto del server immagini {#section-5421bfd2ca2a4a979faf812b6fdb2887}

Specifica la porta utilizzata per la comunicazione tra Platform Server e Image Server. Assicurarsi di specificare un numero di porta che non viene utilizzato altrimenti nel sistema host.

>[!NOTE]
>
>Affinché Image Server funzioni correttamente, è necessario impostare lo stesso valore per `IS::TcpPort` e `PS::isConnection.port`.

## IS::PhysicalMemory - Limite di memoria del server di immagini {#section-85e37aa2ac6e456eb698da716dd3247d}

Limite approssimativo per i dati immagine in memoria, espresso come percentuale di memoria fisica. L&#39;intervallo valido è compreso tra 10% e 90%. Se possibile, Image Server tenta di limitare l’utilizzo della memoria immagine alla quantità specificata. Il limite può essere superato temporaneamente durante l&#39;attività di trasformazione pesante.

## IS::WorkerThread - Numero di thread di lavoro Image Server {#section-e2946063b13c4f728cdf5dba3d8b4de1}

Il numero massimo di thread utilizzati dal server immagini per l&#39;elaborazione dei dati immagine. Il valore predefinito è 0, che consente al server immagini di ottimizzare automaticamente il numero di thread.

Alcuni sistemi operativi hanno modelli di threading con un sovraccarico elevato per la commutazione del contesto. In tali circostanze le prestazioni complessive del server possono migliorare quando viene selezionato un numero di thread specifico (ad esempio un thread per CPU). Potrebbe essere necessaria una certa sperimentazione per trovare l&#39;impostazione ottimale. Per ulteriori informazioni, consultate le note sulla versione di Image Server e la documentazione del sistema operativo.

## IS::NumberOfTextServers - Numero di istanze del server di testo {#section-971e20a90c1a473598fba738ed95671a}

Il numero massimo di renderer di testo da attivare contemporaneamente. 0 (impostazione predefinita) equivale a 1,5 volte il numero di core CPU disponibili.

## IS::TextServerTcpPortRange - Porte di comunicazione server di testo {#section-a13465de88ed4df09931e5ba840c1942}

Le porte da utilizzare per le comunicazioni con il server di testo. Specificare il primo e l&#39;ultimo numero di porta, separati da &#39;-&#39;.
