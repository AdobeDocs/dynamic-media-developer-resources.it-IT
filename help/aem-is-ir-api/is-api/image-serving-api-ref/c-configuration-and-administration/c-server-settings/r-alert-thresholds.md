---
description: Utilizza queste impostazioni del server per configurare le soglie di avviso.
solution: Experience Manager
title: Soglie di allarme
feature: Dynamic Media Classic, SDK/API
role: Sviluppatore, amministratore, Business Practices
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '405'
ht-degree: 0%

---


# Soglie di avviso{#alert-thresholds}

Utilizza queste impostazioni del server per configurare le soglie di avviso.

## AS: monitorAlertGenerator.maxAverageResponseTime - Soglia tempo di rispostaAS: monitorAlertGenerator.maxAverageResponseTime - Tempo di risposta {#section-35111039ac6c4a63ba23fc2c828ab726}

Viene emesso un avviso di tempo di risposta quando il tempo medio di elaborazione di una richiesta durante l’intervallo di campionamento supera la soglia qui impostata. Espresso in msec; numero intero 0 o superiore. I valori tipici sono compresi tra 100 e 1000 msec, a seconda della complessità delle operazioni.

>[!NOTE]
>
>Per questo avviso non vengono considerate le richieste con stato di risposta 4xx o 5xx.

## AS::monitorAlertGenerator.maxErrorRate - Soglia del tasso di risposta degli erroriAS::monitorAlertGenerator.maxErrorRate - Tasso di risposta degli errori {#section-76ba77fd3102419395e0f86719a1f3ec}

Viene generato un avviso di errore quando il rapporto tra le risposte di errore HTTP e le risposte di errore totali nell’intervallo di campionamento supera la soglia specificata.

Valore reale compreso tra 0,0 e 1,0. In genere impostato su tra 0,005 e 0,1. Impostare su 1 per disabilitare gli avvisi di errore.

## AS::monitorAlertGenerator.minRequestRate - Soglia traffico bassa {#section-8dfb89ed138640fd86f5ce1dae2a533e}

Viene inviato un avviso di traffico minimo quando il numero medio di richieste al secondo ricevute nell’intervallo di campionamento corrente scende al di sotto di tale soglia. Disattiva l’avviso impostando questo valore su 0. Espresso in richieste al secondo. Valore reale 0 o superiore.

## AS::monitorAlertGenerator.minFreeHeapSpace -Soglia spazio heap libero {#section-ce6705045f6842769030ccb1894594cc}

Specifica lo spazio di heap Java gratuito minimo. Un avviso di priorità viene inviato immediatamente dopo un ciclo di raccolta degli oggetti inattivi Java quando lo spazio di heap gratuito è inferiore a questa soglia. Si consiglia di 50 MB per il funzionamento sicuro del Platform Server. Mantenere lo spazio heap libero al di sopra di questo valore riduce la frequenza dei cicli di raccolta degli oggetti inattivi, che possono migliorare le prestazioni complessive del server. Valore intero in byte, 0 o superiore.

## AS::monitorAlertGenerator.maxOverlap - Numero massimo di richieste simultanee {#section-ddc6925bff944758ab19bcc9cf3f2589}

Viene attivato un avviso di sovrapposizione quando il numero medio di richieste elaborate contemporaneamente durante l’intervallo di media supera questa soglia. Un’elevata sovrapposizione può indicare una possibile condizione di sovraccarico del server.

Valore intero 1 o superiore. Un intervallo tipico è da 20 a 50, a seconda della frequenza di hit della cache e della complessità della richiesta.

## AS::monitorAlertGenerator.lockedThreshold - Soglia richieste bloccate {#section-012a1c9937d445708380339279c62d80}

Specifica il numero di secondi in cui una richiesta deve essere in sospeso prima che venga considerata bloccata o bloccata. Viene emesso un avviso di richiesta bloccata se alla fine di un intervallo di tempo medio almeno una richiesta è rimasta in sospeso per un periodo di tempo superiore a quello specificato. Valore intero positivo in msec.

Per tenere conto di richieste di rendering complesse e di richieste che richiedono l’ottenimento di dati da server HTTP esterni, si consiglia di impostare questo valore su almeno 30 secondi (a meno che tale condizione non venga rilevata da questo avviso).
