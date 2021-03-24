---
description: Viene inviato un avviso di priorità quando lo spazio di heap Java gratuito si trova al di sotto della soglia specificata immediatamente dopo un ciclo di raccolta degli oggetti inattivi Java.
solution: Experience Manager
title: Avviso prioritario spazio di heap
feature: Dynamic Media Classic, SDK/API
role: Sviluppatore, amministratore, Business Practices
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '94'
ht-degree: 0%

---


# Avviso prioritario spazio heap{#heap-space-priority-alert}

Viene inviato un avviso di priorità quando lo spazio di heap Java gratuito si trova al di sotto della soglia specificata immediatamente dopo un ciclo di raccolta degli oggetti inattivi Java.

Gli avvisi ripetuti devono essere risolti aumentando lo spazio di heap Java. Le occorrenze successive di questa condizione non generano un avviso e-mail fino alla scadenza del periodo di ritardo specificato con `AS::monitorAlertGenerator.heapSpaceResetInterval`.
