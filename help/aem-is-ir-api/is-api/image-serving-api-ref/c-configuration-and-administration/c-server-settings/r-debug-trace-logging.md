---
description: Utilizzare queste impostazioni del server per eseguire il debug della registrazione delle tracce.
solution: Experience Manager
title: Debug_trace logging
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '408'
ht-degree: 0%

---


# Debug_trace logging{#debug-trace-logging}

Utilizzare queste impostazioni del server per eseguire il debug della registrazione delle tracce.

>[!NOTE]
>
>Si consiglia di configurare tutti i file di registro in modo che vengano scritti nella stessa cartella di `TC::directory`. Questo assicura che tutti i file di registro di Image Server partecipino alla rotazione automatica dei file di registro configurata con `TC::maxDays`, che impedirà la potenziale instabilità del server a causa di condizioni di spazio su disco insufficiente.

## SV::log - Percorso file di log di traccia del supervisore del server {#section-3697bc480ff646e79cacc2812c55ef26}

Nome della cartella e del file di base per i file di registro di Server Supervisore. Il percorso può essere assoluto o relativo a *[!DNL install_folder]*. Al nome del file (prima del suffisso del file, se presente) verrà aggiunto un trattino e la data corrente ( *[!DNL -yyyy-mm-dd]*). Si consiglia di inviare tutti i file di registro alla stessa cartella dei file di registro di Platform Server ( `PS::LogFolder`) per sfruttare la gestione dei file di registro implementata da Platform Server ( `PS::LogDays`). Il valore predefinito è [!DNL logs/Supervisor.log].

>[!NOTE]
>
>È necessario creare la nuova cartella prima di modificare questa impostazione. Assicurati che le autorizzazioni di accesso siano impostate in modo che il Server Supervisore disponga dei privilegi di creazione, lettura e scrittura necessari.

## SV::tracelevel - Livello di log di traccia del supervisore del server {#section-36f8634741da4c618d67aa628b5fe474}

Il livello di log può essere 1, 2, 3 o 4. Il valore predefinito è 2.

## IS::Log - Percorso file di registro di debug Image Server {#section-73a3f09b77f2446c9f82207b7d8aec39}

Nome della cartella e del file di base per i file di registro di traccia di Image Server. Il percorso può essere assoluto o relativo a *[!DNL install_folder]*. ImageServer aggiunge un trattino e la data corrente ( *[!DNL -yyyy-mm-dd]*) al nome del file (prima dell&#39;eventuale suffisso di file). Si consiglia di inviare i file di registro di Image Server alla stessa cartella dei file di registro di Platform Server ( `PS::LogFolder`) per sfruttare la gestione dei file di registro implementata da Platform Server (vedere `PS::LogDays`).

>[!NOTE]
>
>È necessario creare la nuova cartella prima di modificare questa impostazione. Assicurati che le autorizzazioni di accesso siano impostate in modo che Image Server disponga dei privilegi di creazione, lettura e scrittura necessari.

## IS:TraceClient - Livello di log debug Image Server {#section-3851f1f68e404430985c629ac80534db}

Il livello di log può essere 1, 2, 3 o 4 (il valore predefinito è 2)

Il livello 1 registra gli eventi relativi alle connessioni di avvio, arresto e Platform Server.

Il livello 2 registra anche la connessione e la disconnessione dalle immagini sorgente.

Il livello 3 aggiunge la registrazione delle richieste per i dati pixel e la consegna dello stesso al server Platform.

Il livello 4 registra tutti i messaggi ricevuti dal server Platform.

I livelli 3 e 4 devono essere utilizzati solo a scopo di debug, in quanto i file di log possono diventare molto grandi.

## IS::TraceStatsInterval - Intervallo di log delle statistiche del server di immagini {#section-1d8df96d61044e33a5b2b2b0309c2d59}

Image Server scrive le statistiche della memoria nel file di log di traccia nell&#39;intervallo specificato da questa impostazione. L&#39;intervallo valido è compreso tra 5 e 86.400 secondi.
