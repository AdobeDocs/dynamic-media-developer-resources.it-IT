---
description: Utilizzare queste impostazioni del server per eseguire il debug della registrazione di traccia.
seo-description: Utilizzare queste impostazioni del server per eseguire il debug della registrazione di traccia.
seo-title: Debug_trace logging
solution: Experience Manager
title: Debug_trace logging
topic: Scene7 Image Serving - Image Rendering API
uuid: 33f1d093-007d-453b-965a-9d701a845954
translation-type: tm+mt
source-git-commit: e8e5b07329bde3e23ee095d5022da62d67e9478c
workflow-type: tm+mt
source-wordcount: '410'
ht-degree: 0%

---


# Debug_trace logging{#debug-trace-logging}

Utilizzare queste impostazioni del server per eseguire il debug della registrazione di traccia.

>[!NOTE]
>
>Si consiglia di configurare tutti i file di registro in modo che vengano scritti nella stessa cartella di `TC::directory`. In questo modo tutti i file di registro di Image Server partecipano alla rotazione automatica dei file di registro configurata con `TC::maxDays`, che impedirà la potenziale instabilità del server a causa di condizioni di spazio su disco insufficiente.

## SV::log - Percorso del file di registro di traccia del supervisore del server {#section-3697bc480ff646e79cacc2812c55ef26}

Nome della cartella e del file di base per i file di registro di Server Supervisore. Il percorso può essere assoluto o relativo a *[!DNL install_folder]*. Il Server Supervisore aggiungerà un trattino e la data corrente ( *[!DNL -yyyy-mm-dd]*) al nome del file (prima dell&#39;eventuale suffisso del file). Si consiglia di inviare tutti i file di registro alla stessa cartella dei file di registro del server piattaforma ( `PS::LogFolder`) per sfruttare la gestione dei file di registro implementata dal server piattaforma ( `PS::LogDays`). Il valore predefinito è [!DNL logs/Supervisor.log].

>[!NOTE]
>
>Prima di modificare questa impostazione è necessario creare la nuova cartella. Accertatevi che le autorizzazioni di accesso siano impostate in modo che il Supervisore server disponga dei privilegi di creazione, lettura e scrittura necessari.

## SV::tracelevel - Livello di registro traccia supervisore server {#section-36f8634741da4c618d67aa628b5fe474}

Il livello di registro può essere 1, 2, 3 o 4. Il valore predefinito è 2.

## IS::Log - Percorso file registro debug Image Server {#section-73a3f09b77f2446c9f82207b7d8aec39}

Nome della cartella e del file di base per i file di registro di traccia del server immagini. Il percorso può essere assoluto o relativo a *[!DNL install_folder]*. ImageServer aggiungerà un trattino e la data corrente ( *[!DNL -yyyy-mm-dd]*) al nome del file (prima del suffisso del file, se presente). Si consiglia di inviare i file di registro del server immagini alla stessa cartella dei file di registro del server piattaforme ( `PS::LogFolder`) per sfruttare la gestione dei file di registro implementata dal server piattaforme (vedere `PS::LogDays`).

>[!NOTE]
>
>Prima di modificare questa impostazione è necessario creare la nuova cartella. Accertatevi che le autorizzazioni di accesso siano impostate in modo che Image Server disponga dei privilegi di creazione, lettura e scrittura necessari.

## IS:TraceClient - Livello registro debug server immagini {#section-3851f1f68e404430985c629ac80534db}

Il livello di registro può essere 1, 2, 3 o 4 (il valore predefinito è 2)

Il livello 1 registra gli eventi relativi alle connessioni di avvio, arresto e server piattaforma.

Il livello 2 registra anche la connessione e la disconnessione dalle immagini sorgente.

Il livello 3 aggiunge la registrazione delle richieste di dati in pixel e la distribuzione di tali dati al server della piattaforma.

Il livello 4 registra tutti i messaggi ricevuti dal server piattaforma.

I livelli 3 e 4 devono essere utilizzati solo a scopo di debug, in quanto i file di registro possono diventare molto grandi.

## IS::TraceStatsInterval - Intervallo di registro delle statistiche del server di immagini {#section-1d8df96d61044e33a5b2b2b0309c2d59}

Il server immagini scrive le statistiche della memoria nel relativo file di registro di traccia all’intervallo specificato da questa impostazione. L&#39;intervallo valido è compreso tra 5 e 86.400 secondi.
