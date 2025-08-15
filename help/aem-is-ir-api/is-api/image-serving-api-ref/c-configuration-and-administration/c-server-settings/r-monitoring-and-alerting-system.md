---
description: Utilizzare queste impostazioni del server per configurare il sistema di monitoraggio e allarme.
solution: Experience Manager
title: Sistema di monitoraggio e allerta
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: fe672d1b-93e5-466a-a329-3032095c6ba8
source-git-commit: 97fbf820590b53de5a1e6ce904e44d6b0ef9a214
workflow-type: tm+mt
source-wordcount: '239'
ht-degree: 0%

---

# Sistema di monitoraggio e allerta{#monitoring-and-alerting-system}

Utilizzare queste impostazioni del server per configurare il sistema di monitoraggio e allarme.

## AS::monitorAlertGenerator.enableGlobalAlerting - Sistema di avvisi Abilita {#section-612f8ea61794426ab205e22e5f665fa9}

Abilita notifica e-mail impostando su &quot;true&quot; e configurando le impostazioni del notifica e-mail. Impostazione per `false` disattivare tutti gli avvisi e-mail - questo può essere utile quando si porta un server off-line per manutenzione. Booleano.

## AS::mailSender.host - SMTP Host {#section-151df07e7b44446581339bb7abeeba7a}

L&#39;indirizzo IP del server di posta elettronica SMTP.

## AS::mailSender.porta- Porta SMTP {#section-4b25efca8fd84d5c92dafacd0555e99d}

Il porta di ascolto per il server di posta elettronica SMTP.

## AS::monitorAlertGenerator.messageTo - Destinatario Invia messaggio {#section-0017bbaa15434117a70900c3f1163960}

Uno o più indirizzi e-mail a cui inviare gli avvisi. Utilizzare punti e virgola come separatori.

## AS::monitorAlertGenerator.messageFrom - Invia messaggio mittente {#section-db320cba4ac2438ca1cfe6abce4aed87}

Indirizzo e-mail da utilizzare nel **[!UICONTROL campo E-mail Da]** .

## AS::monitorAlertGenerator.alertInterval - Intervallo di monitoraggio {#section-99cb2e3380c1499e9d5aec3671ed73c7}

Il sistema di monitoraggio accumula le condizioni di allerta durante l&#39;intervallo di allerta e invia un&#39;e-mail di avviso contenente tutti gli avvisi accumulati alla fine di ogni intervallo. Millisecondi, valore intero, 60000 o superiore. In genere impostato su 5 o 10 minuti.

## AS::monitorAlertGenerator.heapSpaceResetInterval - Intervallo di avviso spazio heap {#section-fd5a2bf04ed44fdcaef20f77084151a8}

Tempo minimo dopo un avviso di spazio di heap prima che ne venga emesso un altro. Tempo di intervallo in msec. Valore intero, 0 o superiore.

## AS::monitorAlertGenerator.minTrafficForAlerts - Traffico minimo per abilitare gli avvisi {#section-8b4db2d6f96642309ca35c49eb3ab230}

Richieste al secondo. Se traffico scende al di sotto di questo soglia, non vengono emessi tempi di risposta e avvisi di errore. Imposta questo valore su 0 per inviare avvisi relativi al tempo di risposta e agli errori a prescindere dal volume traffico. Valore reale pari o superiore a 0.
