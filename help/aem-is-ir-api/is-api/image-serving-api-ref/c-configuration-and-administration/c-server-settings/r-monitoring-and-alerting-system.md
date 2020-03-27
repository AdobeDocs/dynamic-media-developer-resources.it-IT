---
description: Utilizzate queste impostazioni del server per configurare il sistema di monitoraggio e di avvisi.
seo-description: Utilizzate queste impostazioni del server per configurare il sistema di monitoraggio e di avvisi.
seo-title: Sistema di monitoraggio e allarme
solution: Experience Manager
title: Sistema di monitoraggio e allarme
topic: Scene7 Image Serving - Image Rendering API
uuid: 944c7d53-09ec-443e-ac8c-85684d8fda0f
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Sistema di monitoraggio e allarme{#monitoring-and-alerting-system}

Utilizzate queste impostazioni del server per configurare il sistema di monitoraggio e di avvisi.

## AS::monitorAlertGenerator.enableGlobalAlerting - Attivazione del sistema di avvisi {#section-612f8ea61794426ab205e22e5f665fa9}

Attivate la notifica e-mail impostando &#39;true&#39; e configurando le impostazioni di notifica e-mail. L&#39;impostazione per `false` disattivare tutti gli avvisi e-mail può essere utile quando un server viene disattivato per la manutenzione. Booleano.

## AS::mailSender.host - Host SMTP {#section-151df07e7b44446581339bb7abeeba7a}

L&#39;indirizzo IP del server di posta elettronica SMTP.

## AS::mailSender.port- Porta SMTP {#section-4b25efca8fd84d5c92dafacd0555e99d}

La porta di ascolto per il server di posta elettronica SMTP.

## AS::monitorAlertGenerator.messageTo - Message Recipient {#section-0017bbaa15434117a70900c3f1163960}

Uno o più indirizzi e-mail cui inviare gli avvisi. Utilizzare il punto e virgola come separatori.

## AS::monitorAlertGenerator.messageFrom - Message Sender {#section-db320cba4ac2438ca1cfe6abce4aed87}

L&#39;indirizzo e-mail da utilizzare nel campo **[!UICONTROL Da]** .

## AS::monitorAlertGenerator.alertInterval - Intervallo di monitoraggio {#section-99cb2e3380c1499e9d5aec3671ed73c7}

Il sistema di monitoraggio accumulerà le condizioni di allarme durante l&#39;intervallo di allerta e invierà un messaggio e-mail di avviso contenente tutti gli avvisi accumulati alla fine di ogni intervallo. Millisecondi, valore intero, 60000 o superiore. In genere, impostate su 5 o 10 minuti.

## AS::monitorAlertGenerator.heapSpaceResetInterval - Intervallo di avviso spazio heap {#section-fd5a2bf04ed44fdcaef20f77084151a8}

Tempo minimo dopo un avviso di spazio di heap prima che ne venga emesso un altro. Tempo intervallo in msec. Valore intero pari o superiore a 0.

## AS::monitorAlertGenerator.minTrafficForAlerts - Traffico minimo per attivare gli avvisi {#section-8b4db2d6f96642309ca35c49eb3ab230}

Richieste al secondo. Se il traffico scende al di sotto di questa soglia, non verranno emessi avvisi di errore e tempi di risposta. Impostare su 0 per inviare gli avvisi relativi a tempi di risposta e errori indipendentemente dal volume di traffico. Valore reale 0 o maggiore.
