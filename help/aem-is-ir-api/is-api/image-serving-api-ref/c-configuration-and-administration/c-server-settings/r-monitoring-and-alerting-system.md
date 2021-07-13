---
description: Utilizzare queste impostazioni del server per configurare il sistema di monitoraggio e di avviso.
solution: Experience Manager
title: Sistema di monitoraggio e allarme
feature: Dynamic Media Classic, SDK/API
role: Developer,Administrator,User
exl-id: fe672d1b-93e5-466a-a329-3032095c6ba8
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '241'
ht-degree: 0%

---

# Sistema di monitoraggio e allarme{#monitoring-and-alerting-system}

Utilizzare queste impostazioni del server per configurare il sistema di monitoraggio e di avviso.

## AS::monitorAlertGenerator.enableGlobalAlerting - Abilita sistema di avvisi {#section-612f8ea61794426ab205e22e5f665fa9}

Abilita la notifica via e-mail impostando su &quot;true&quot; e configurando le impostazioni di notifica e-mail. Se si imposta `false` si disattivano tutti gli avvisi e-mail, questo può essere utile quando si interrompe la manutenzione di un server. Booleano.

## AS::mailSender.host - Host SMTP {#section-151df07e7b44446581339bb7abeeba7a}

Indirizzo IP del server di posta elettronica SMTP.

## AS::mailSender.port- Porta SMTP {#section-4b25efca8fd84d5c92dafacd0555e99d}

La porta di ascolto del server di posta elettronica SMTP.

## AS::monitorAlertGenerator.messageTo - Message Recipient {#section-0017bbaa15434117a70900c3f1163960}

Uno o più indirizzi e-mail a cui devono essere inviati gli avvisi. Utilizzare i punti e virgola come separatori.

## AS::monitorAlertGenerator.messageFrom - Mittente del messaggio {#section-db320cba4ac2438ca1cfe6abce4aed87}

L&#39;indirizzo e-mail che deve essere utilizzato nel campo e-mail **[!UICONTROL Da]**.

## AS::monitorAlertGenerator.alertInterval - Intervallo di monitoraggio {#section-99cb2e3380c1499e9d5aec3671ed73c7}

Il sistema di monitoraggio accumulerà le condizioni di allarme durante l&#39;intervallo di allerta e invierà un messaggio e-mail di avviso contenente tutti gli avvisi accumulati alla fine di ogni intervallo. Millisecondi, valore intero, 60000 o superiore. In genere impostato su 5 o 10 minuti.

## AS::monitorAlertGenerator.heapSpaceResetInterval - Intervallo di avviso dello spazio heap {#section-fd5a2bf04ed44fdcaef20f77084151a8}

Tempo minimo dopo un avviso di spazio heap prima che ne venga emesso un altro. Tempo di intervallo in msec. Valore intero pari o superiore a 0.

## AS::monitorAlertGenerator.minTrafficForAlerts - Traffico minimo per abilitare gli avvisi {#section-8b4db2d6f96642309ca35c49eb3ab230}

Richieste al secondo. Se il traffico scende al di sotto di questa soglia, non vengono emessi avvisi relativi a tempi di risposta e errori. Impostare su 0 per inviare gli avvisi relativi al tempo di risposta e agli errori indipendentemente dal volume di traffico. Valore reale 0 o superiore.
