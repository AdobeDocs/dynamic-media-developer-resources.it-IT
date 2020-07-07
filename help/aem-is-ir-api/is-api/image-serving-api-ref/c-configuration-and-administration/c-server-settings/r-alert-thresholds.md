---
description: Utilizzate queste impostazioni del server per configurare le soglie di avviso.
seo-description: Utilizzate queste impostazioni del server per configurare le soglie di avviso.
seo-title: Soglie di avviso
solution: Experience Manager
title: Soglie di avviso
topic: Scene7 Image Serving - Image Rendering API
uuid: 032cb396-1a03-4ba9-82d6-ed2cb06e8cf2
translation-type: tm+mt
source-git-commit: e8e5b07329bde3e23ee095d5022da62d67e9478c
workflow-type: tm+mt
source-wordcount: '406'
ht-degree: 0%

---


# Soglie di avviso{#alert-thresholds}

Utilizzate queste impostazioni del server per configurare le soglie di avviso.

## AS: monitorAlertGenerator.maxAverageResponseTime - Soglia tempo di rispostaAS: monitorAlertGenerator.maxAverageResponseTime - Tempo di risposta {#section-35111039ac6c4a63ba23fc2c828ab726}

Viene emesso un avviso sul tempo di risposta quando il tempo medio di elaborazione di una richiesta durante l’intervallo di campionamento supera la soglia qui impostata. Espressi in msec; numero intero pari o superiore a 0. I valori tipici sono compresi tra 100 e 1000 msec, a seconda della complessità delle operazioni.

>[!NOTE]
>
>Per questo avviso non vengono considerate le richieste che generano lo stato di risposta 4xx o 5xx.

## AS::monitorAlertGenerator.maxErrorRate - Soglia frequenza di risposta di erroreAS::monitorAlertGenerator.maxErrorRate - Frequenza di risposta di errore {#section-76ba77fd3102419395e0f86719a1f3ec}

Viene emesso un avviso di errore quando il rapporto tra le risposte di errore HTTP e le risposte totali durante l’intervallo di campionamento supera la soglia specificata.

Valore reale compreso tra 0,0 e 1,0. In genere, è impostato tra 0,005 e 0,1. Impostare su 1 per disabilitare gli avvisi di errore.

## AS::monitorAlertGenerator.minRequestRate - Soglia traffico bassa {#section-8dfb89ed138640fd86f5ce1dae2a533e}

Viene inviato un avviso di traffico minimo quando il numero medio di richieste al secondo ricevute nell’intervallo di campionamento corrente scende al di sotto di tale soglia. Disattiva l’avviso impostando questo valore su 0. Espressa in richieste al secondo. Valore reale 0 o maggiore.

## AS::monitorAlertGenerator.minFreeHeapSpace -Soglia spazio heap gratuito {#section-ce6705045f6842769030ccb1894594cc}

Specifica lo spazio di heap Java gratuito minimo. Un avviso di priorità viene inviato immediatamente dopo un ciclo di raccolta dei rifiuti Java quando lo spazio di heap gratuito è inferiore a tale soglia. Si consiglia di 50 MB per il funzionamento sicuro del server Platform. Mantenendo lo spazio di heap gratuito al di sopra di questo valore si riduce la frequenza dei cicli di raccolta dei rifiuti, il che potrebbe migliorare le prestazioni complessive del server. Valore intero in byte, 0 o superiore.

## AS::monitorAlertGenerator.maxOverlap - Numero massimo di richieste simultanee {#section-ddc6925bff944758ab19bcc9cf3f2589}

Viene attivato un avviso di sovrapposizione quando il numero medio di richieste elaborate contemporaneamente durante l&#39;intervallo di media supera tale soglia. Una sovrapposizione elevata può indicare una possibile condizione di sovraccarico del server.

Valore intero 1 o maggiore. L&#39;intervallo tipico è compreso tra 20 e 50, a seconda della frequenza di hit della cache e della complessità richiesta.

## AS::monitorAlertGenerator.lockThreshold - Soglia richiesta bloccata {#section-012a1c9937d445708380339279c62d80}

Specifica il numero di secondi di attesa di una richiesta prima che venga considerata bloccata o appesa. Viene emesso un avviso di richiesta bloccata se alla fine di un intervallo di tempo medio almeno una richiesta è rimasta in sospeso per un periodo superiore a quello specificato. Valore intero positivo in msec.

Per tenere conto di richieste di rendering complesse e richieste che richiedono il recupero di dati da server HTTP esterni, si consiglia di impostare questo valore su almeno 30 secondi (a meno che tale condizione non venga rilevata da questo avviso).
