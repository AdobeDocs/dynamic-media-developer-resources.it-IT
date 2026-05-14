---
description: Utilizzare queste impostazioni del server per configurare il sistema di monitoraggio e avvisi.
solution: Experience Manager
title: Sistema di monitoraggio e allarme
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: fe672d1b-93e5-466a-a329-3032095c6ba8
TQID: 'https://experienceleague.adobe.com/n8Xw2xwdJNYlTVQusHBqP0aEpMYyPuE135TR30FLZKQ'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 240
ht-degree: 0%

---

# Sistema di monitoraggio e allarme{#monitoring-and-alerting-system}

Utilizzare queste impostazioni del server per configurare il sistema di monitoraggio e avvisi.

## AS::monitorAlertGenerator.enableGlobalAlerting - Attivazione sistema di avvisi {#section-612f8ea61794426ab205e22e5f665fa9}

Abilita la notifica e-mail impostando su &quot;true&quot; e configurando le impostazioni di notifica e-mail. L&#39;impostazione su `false` disattiva tutti gli avvisi e-mail. Questo può essere utile quando si disattiva un server per manutenzione. Booleano.

## AS::mailSender.host - Host SMTP {#section-151df07e7b44446581339bb7abeeba7a}

L&#39;indirizzo IP del server di posta elettronica SMTP.

## AS::mailSender.port- Porta SMTP {#section-4b25efca8fd84d5c92dafacd0555e99d}

Porta di ascolto per il server di posta elettronica SMTP.

## AS::monitorAlertGenerator.messageTo - Destinatario messaggio {#section-0017bbaa15434117a70900c3f1163960}

Uno o più indirizzi e-mail a cui inviare gli avvisi. Utilizzare il punto e virgola come separatori.

## AS::monitorAlertGenerator.messageFrom - Mittente del messaggio {#section-db320cba4ac2438ca1cfe6abce4aed87}

Indirizzo e-mail da utilizzare nel campo e-mail **[!UICONTROL Da]**.

## AS::monitorAlertGenerator.alertInterval - Intervallo di monitoraggio {#section-99cb2e3380c1499e9d5aec3671ed73c7}

Il sistema di monitoraggio accumula le condizioni di avviso durante l&#39;intervallo e invia un messaggio e-mail contenente tutti gli avvisi accumulati alla fine di ogni intervallo. Millisecondi, valore intero, 60000 o maggiore. In genere è impostato su 5 o 10 minuti.

## AS::monitorAlertGenerator.heapSpaceResetInterval - Intervallo avviso spazio heap {#section-fd5a2bf04ed44fdcaef20f77084151a8}

Tempo minimo dopo un avviso dello spazio heap prima che ne venga emesso un altro. Tempo di intervallo in millisecondi. Valore intero, 0 o maggiore.

## AS::monitorAlertGenerator.minTrafficForAlerts - Traffico minimo per abilitare gli avvisi {#section-8b4db2d6f96642309ca35c49eb3ab230}

Richieste al secondo. Se il traffico scende al di sotto di questa soglia, non vengono generati avvisi relativi a tempi di risposta e errori. Imposta questo valore su 0 per inviare avvisi di errore e tempi di risposta indipendentemente dal volume di traffico. Valore reale 0 o maggiore.
