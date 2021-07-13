---
description: Utilizza queste impostazioni del server per configurare il server.
solution: Experience Manager
title: Server
feature: Dynamic Media Classic, SDK/API
role: Developer,Administrator,User
exl-id: 10970ca8-b209-4adf-b027-6eb8d7a15db6
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '353'
ht-degree: 0%

---

# Server{#server}

Utilizza queste impostazioni del server per configurare il server.

## SV::ImageServerMode - Image Server Mode {#section-991b287f2dde4f77a24fc69d5b32cabd}

Per Linux sono disponibili sia una versione a 32 bit che una versione a 64 bit di Image Server. Specifica ImageServer64 quando installato su server Linux a 64 bit o ImageServer32 (predefinito) quando installato su server a 32 bit.

>[!NOTE]
>
>La versione a 64 bit di Image Server non supporta i file sorgente FlashPix.

>[!NOTE]
>
>La modalità a 64 bit non è supportata in Windows. È possibile specificare solo `ImageServer32`. In caso contrario, Image Server non si avvia.

## SV::PsHeapSize - Dimensione heap del server della piattaforma {#section-fd83715948764aeda58d6b3a9f9f8be9}

Dimensione dell’heap Java per Platform Server. Il valore predefinito è &quot; `512m`&quot; (512 Mbyte).

## IS::TcpPort, PS::isConnection.port - Porta di ascolto del server di immagini {#section-5421bfd2ca2a4a979faf812b6fdb2887}

Specifica la porta utilizzata per la comunicazione tra Platform Server e Image Server. Assicurati di specificare un numero di porta che non viene utilizzato altrimenti sul sistema host.

>[!NOTE]
>
>Affinché Image Serving funzioni correttamente, è necessario impostare lo stesso valore per `IS::TcpPort` e `PS::isConnection.port`.

## IS::PhysicalMemory - Limite di memoria del server di immagini {#section-85e37aa2ac6e456eb698da716dd3247d}

Limite approssimativo per i dati immagine in memoria, espresso come percentuale di memoria fisica. L&#39;intervallo valido è compreso tra il 10% e il 90%. Il server immagini tenta di limitare l&#39;uso della memoria immagine alla quantità specificata, se possibile. Il limite può essere temporaneamente superato durante l&#39;attività di lavorazione pesante.

## IS::WorkerThreads - Numero di thread di lavoro di Image Server {#section-e2946063b13c4f728cdf5dba3d8b4de1}

Il numero massimo di thread utilizzati da Image Server per l&#39;elaborazione dei dati immagine. Il valore predefinito è 0, che consente al server di immagini di ottimizzare automaticamente il conteggio dei thread.

Alcuni sistemi operativi dispongono di modelli threading con un alto overhead di commutazione di contesto. In tale circostanza le prestazioni complessive del server possono migliorare quando viene selezionato un conteggio di thread specifico (ad esempio un thread per CPU). Per trovare l’impostazione ottimale potrebbe essere necessaria una certa sperimentazione. Per ulteriori informazioni, consulta le note sulla versione di Image Serving e la documentazione del sistema operativo .

## IS::NumberOfTextServers - Numero di istanze del server di testo {#section-971e20a90c1a473598fba738ed95671a}

Il numero massimo di render di testo da attivare contemporaneamente. 0 (impostazione predefinita) equivale a 1,5 volte il numero di core della CPU disponibili.

## IS::TextServerTcpPortRange - Porte di comunicazione del server di testo {#section-a13465de88ed4df09931e5ba840c1942}

Le porte da utilizzare per le comunicazioni server di testo. Specificare il primo e l&#39;ultimo numero di porta, separati da &#39;-&#39;.
