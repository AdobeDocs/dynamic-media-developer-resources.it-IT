---
title: Registrazione Debug_trace
description: Utilizzare queste impostazioni del server per eseguire il debug della registrazione della traccia.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: fe1fc984-3c6b-4bd1-b5ba-630860ac7319
source-git-commit: 163ac6a6f44193f1b66ae24059630521d7247eae
workflow-type: tm+mt
source-wordcount: '389'
ht-degree: 1%

---

# Registrazione Debug_trace{#debug-trace-logging}

Utilizzare queste impostazioni del server per eseguire il debug della registrazione della traccia.

>[!NOTE]
>
>L&#39;Adobe consiglia di configurare tutti i file di registro da scrivere nella stessa cartella di `TC::directory`. In questo modo, tutti i file di registro di Image Server partecipano alla rotazione automatica dei file di registro configurata con `TC::maxDays`, che impedisce la potenziale instabilità del server a causa di condizioni di spazio su disco insufficiente.

## SV::log - Percorso file di log di traccia di Server Supervisor {#section-3697bc480ff646e79cacc2812c55ef26}

Nome della cartella e del file di base per i file di registro di Server Supervisor. Il percorso può essere assoluto o relativo a *[!DNL install_folder]*. Il Server Supervisor aggiunge un trattino e la data corrente ( *[!DNL -yyyy-mm-dd]*) al nome del file (prima del suffisso del file, se presente). Adobe consiglia di inviare tutti i file di registro alla stessa cartella di [!DNL Platform Server] file di registro ( `PS::LogFolder`) per utilizzare la gestione dei file di registro implementata da [!DNL Platform Server] (`PS::LogDays`). Il valore predefinito è [!DNL logs/Supervisor.log].

>[!NOTE]
>
>È necessario creare la nuova cartella prima di modificare questa impostazione. Verificare che le autorizzazioni di accesso siano impostate in modo che Server Supervisor disponga dei privilegi di creazione, lettura e scrittura necessari.

## SV::tracelevel - Livello registro traccia supervisore server {#section-36f8634741da4c618d67aa628b5fe474}

Il livello di registro può essere 1, 2, 3 o 4. Il valore predefinito è 2.

## IS::Log - Percorso file di registro debug server immagini {#section-73a3f09b77f2446c9f82207b7d8aec39}

Nome della cartella e del file di base per i file di log di traccia di Image Server. Il percorso può essere assoluto o relativo a *[!DNL install_folder]*. ImageServer aggiunge un trattino e la data corrente ( *[!DNL -yyyy-mm-dd]*) al nome del file (prima del suffisso del file, se presente). L&#39;Adobe consiglia di inviare i file di registro di Image Server alla stessa cartella di [!DNL Platform Server] file di registro ( `PS::LogFolder`) per utilizzare la gestione dei file di registro implementata da [!DNL Platform Server] (vedere `PS::LogDays`).

>[!NOTE]
>
>È necessario creare la nuova cartella prima di modificare questa impostazione. Assicurati che le autorizzazioni di accesso siano impostate in modo che Image Server disponga dei privilegi di creazione, lettura e scrittura necessari.

## IS:TraceClient - Livello registro debug server immagini {#section-3851f1f68e404430985c629ac80534db}

Il livello di registro può essere 1, 2, 3 o 4 (il valore predefinito è 2)

Il livello 1 registra gli eventi relativi all&#39;avvio, all&#39;arresto e [!DNL Platform Server] connessioni.

Il livello 2 registra anche la connessione e la disconnessione dalle immagini sorgente.

Il Livello 3 aggiunge la registrazione delle richieste di dati pixel e la consegna dello stesso al [!DNL Platform Server].

Il livello 4 registra tutti i messaggi ricevuti dal [!DNL Platform Server].

I livelli 3 e 4 devono essere utilizzati solo a scopo di debug, in quanto i file di registro possono diventare di grandi dimensioni.

## IS::TraceStatsInterval - Intervallo registro statistiche server immagini {#section-1d8df96d61044e33a5b2b2b0309c2d59}

Il server immagini scrive le statistiche della memoria nel file di log di traccia in base all&#39;intervallo specificato da questa impostazione. L’intervallo valido è 5-86.400 secondi.
