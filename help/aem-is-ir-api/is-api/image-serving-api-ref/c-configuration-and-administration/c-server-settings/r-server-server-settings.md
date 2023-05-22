---
description: Utilizzare queste impostazioni server per configurare il server.
solution: Experience Manager
title: Server
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 10970ca8-b209-4adf-b027-6eb8d7a15db6
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '342'
ht-degree: 0%

---

# Server{#server}

Utilizzare queste impostazioni server per configurare il server.

## SV::ImageServerMode - Image Server Mode {#section-991b287f2dde4f77a24fc69d5b32cabd}

Sia la versione a 32 bit che la versione a 64 bit del server immagini sono disponibili per Linux. Specificare ImageServer64 se installato su server Linux a 64 bit o ImageServer32 (impostazione predefinita) se installato su server a 32 bit.

>[!NOTE]
>
>La versione a 64 bit del server immagini non supporta i file di origine FlashPix.

>[!NOTE]
>
>Modalità a 64 bit non supportata in Windows. Solo `ImageServer32` possono essere specificati. In caso contrario, Image Server non si avvierà.

## SV::PsHeapSize - [!DNL Platform Server] Dimensione heap {#section-fd83715948764aeda58d6b3a9f9f8be9}

Dimensione heap Java per [!DNL Platform Server]. Impostazione predefinita &quot; `512m`&quot; (512 Mbyte).

## IS::TcpPort, PS::isConnection.port - Porta di ascolto server immagini {#section-5421bfd2ca2a4a979faf812b6fdb2887}

Specifica la porta utilizzata per la comunicazione tra [!DNL Platform Server] e il server immagini. Assicurarsi di specificare un numero di porta che non venga utilizzato in altro modo nel sistema host.

>[!NOTE]
>
>Affinché Image Server funzioni correttamente, è necessario impostare lo stesso valore per `IS::TcpPort` e `PS::isConnection.port`.

## IS::PhysicalMemory - Limite memoria server immagini {#section-85e37aa2ac6e456eb698da716dd3247d}

Limite approssimativo per i dati immagine in memoria, espresso come percentuale della memoria fisica. L&#39;intervallo valido è compreso tra 10% e 90%. Il server immagini tenta di limitare l&#39;utilizzo della memoria immagine alla quantità specificata, se possibile. Il limite può essere temporaneamente superato durante un’intensa attività di elaborazione.

## IS::WorkerThreads - Numero di thread di lavoro del server immagini {#section-e2946063b13c4f728cdf5dba3d8b4de1}

Numero massimo di thread utilizzati dal server immagini per l&#39;elaborazione dei dati immagine. Il valore predefinito è 0, che consente al server immagini di ottimizzare automaticamente il conteggio dei thread.

Alcuni sistemi operativi dispongono di modelli di threading con un elevato sovraccarico di cambio di contesto. In tali circostanze, le prestazioni complessive del server possono migliorare quando viene selezionato un numero specifico di thread (ad esempio, un thread per CPU). Per trovare l’impostazione ottimale potrebbe essere necessaria una certa sperimentazione. Per ulteriori informazioni, consulta le note sulla versione di Image Server e la documentazione del sistema operativo.

## IS::NumberOfTextServers - Numero di istanze del server di testo {#section-971e20a90c1a473598fba738ed95671a}

Numero massimo di renderer di testo attivi contemporaneamente. 0 (valore predefinito) equivale a 1,5 volte il numero di core della CPU disponibili.

## IS::TextServerTcpPortRange - Porte di comunicazione server di testo {#section-a13465de88ed4df09931e5ba840c1942}

Porte da utilizzare per le comunicazioni server di testo. Specifica il primo e l’ultimo numero di porta, separati da &quot;-&quot;.
