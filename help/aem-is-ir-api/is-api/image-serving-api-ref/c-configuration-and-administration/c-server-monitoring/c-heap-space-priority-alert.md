---
description: Viene inviato un avviso di priorità quando lo spazio di heap Java gratuito si trova al di sotto della soglia specificata immediatamente dopo un ciclo di raccolta degli oggetti inattivi Java.
seo-description: Viene inviato un avviso di priorità quando lo spazio di heap Java gratuito si trova al di sotto della soglia specificata immediatamente dopo un ciclo di raccolta degli oggetti inattivi Java.
seo-title: Avviso prioritario spazio di heap
solution: Experience Manager
title: Avviso prioritario spazio di heap
uuid: 89956ad3-8a73-40db-92bd-326e3fab37ee
feature: Dynamic Media Classic, SDK/API
role: Sviluppatore, amministratore, Business Practices
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '121'
ht-degree: 0%

---


# Avviso prioritario spazio heap{#heap-space-priority-alert}

Viene inviato un avviso di priorità quando lo spazio di heap Java gratuito si trova al di sotto della soglia specificata immediatamente dopo un ciclo di raccolta degli oggetti inattivi Java.

Gli avvisi ripetuti devono essere risolti aumentando lo spazio di heap Java. Le occorrenze successive di questa condizione non generano un avviso e-mail fino alla scadenza del periodo di ritardo specificato con `AS::monitorAlertGenerator.heapSpaceResetInterval`.
