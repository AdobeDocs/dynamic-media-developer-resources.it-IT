---
description: Utilizzare queste impostazioni del server per configurare le soglie di avviso.
solution: Experience Manager
title: Soglie di avviso
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 1ae76692-2688-4902-82a0-d0751408eee7
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '394'
ht-degree: 0%

---

# Soglie di avviso{#alert-thresholds}

Utilizzare queste impostazioni del server per configurare le soglie di avviso.

## AS: monitorAlertGenerator.maxAverageResponseTime -Soglia tempo di risposta AS:: monitorAlertGenerator.maxAverageResponseTime -Tempo di risposta {#section-35111039ac6c4a63ba23fc2c828ab726}

Un avviso relativo al tempo di risposta viene emesso quando il tempo medio di elaborazione di una richiesta durante l&#39;intervallo di campionamento supera la soglia impostata in questo campo. Espresso in msec; numero intero 0 o maggiore. I valori tipici sono compresi tra 100 e 1000 msec, a seconda della complessità delle operazioni.

>[!NOTE]
>
>Le richieste che determinano lo stato di risposta 4xx o 5xx non vengono considerate per questo avviso.

## AS::monitorAlertGenerator.maxErrorRate - Soglia tasso di risposta di errore AS::monitorAlertGenerator.maxErrorRate - Tasso di risposta di errore {#section-76ba77fd3102419395e0f86719a1f3ec}

Quando il rapporto tra le risposte di errore HTTP e le risposte totali durante l&#39;intervallo di campionamento supera la soglia specificata, viene generato un avviso di errore.

Valore reale compreso tra 0,0 e 1,0. In genere viene impostato su un valore compreso tra 0,005 e 0,1. Impostate questo valore su 1 per disattivare gli avvisi di errore.

## AS::monitorAlertGenerator.minRequestRate - Soglia traffico bassa {#section-8dfb89ed138640fd86f5ce1dae2a533e}

Viene inviato un avviso di traffico minimo quando il numero medio di richieste ricevute al secondo durante l’intervallo di campionamento corrente è inferiore a questa soglia. Disattivare l&#39;avviso impostando questo valore su 0. Espresso in richieste al secondo. Valore reale 0 o maggiore.

## AS::monitorAlertGenerator.minFreeHeapSpace -Soglia spazio heap disponibile {#section-ce6705045f6842769030ccb1894594cc}

Specifica lo spazio heap Java minimo disponibile. Un avviso di priorità viene inviato subito dopo un ciclo di Garbage Collection Java quando lo spazio heap libero è inferiore a questa soglia. Si consigliano 50 MB per il funzionamento sicuro del [!DNL Platform Server]. Mantenendo lo spazio heap libero al di sopra di questo valore si riduce la frequenza dei cicli di Garbage Collection, che possono migliorare le prestazioni complessive del server. Valore intero in byte, 0 o maggiore.

## AS::monitorAlertGenerator.maxOverlap - Numero massimo di richieste concorrenti {#section-ddc6925bff944758ab19bcc9cf3f2589}

Un avviso di sovrapposizione viene attivato quando il numero medio di richieste elaborate contemporaneamente durante l’intervallo di calcolo della media supera questa soglia. Una sovrapposizione elevata può indicare una possibile condizione di sovraccarico del server.

Valore intero 1 o maggiore. L’intervallo tipico è compreso tra 20 e 50, a seconda della frequenza di hit della cache e della complessità delle richieste.

## AS::monitorAlertGenerator.lockedThreshold - Soglia richiesta bloccata {#section-012a1c9937d445708380339279c62d80}

Specifica per quanti secondi una richiesta deve essere in sospeso prima che venga considerata bloccata o bloccata. Viene emesso un avviso di richiesta bloccata se al termine di un intervallo di calcolo della media almeno una richiesta è stata in sospeso per un periodo di tempo superiore a quello specificato. Valore intero positivo in msec.

Per tenere conto di richieste di rendering complesse e di richieste che richiedono l’ottenimento di dati da server HTTP esterni, si consiglia di impostare questo valore su almeno 30 secondi (a meno che tale condizione non venga rilevata da questo avviso).
