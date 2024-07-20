---
description: Un avviso di priorità viene inviato quando lo spazio heap Java libero è inferiore alla soglia specificata subito dopo un ciclo di Garbage Collection Java.
solution: Experience Manager
title: Avviso priorità spazio heap
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 32951003-386f-4ea2-a5a0-f4d2e6d95ba5
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '85'
ht-degree: 0%

---

# Avviso priorità spazio heap{#heap-space-priority-alert}

Un avviso di priorità viene inviato quando lo spazio heap Java libero è inferiore alla soglia specificata subito dopo un ciclo di Garbage Collection Java.

Gli avvisi ripetuti devono essere gestiti aumentando lo spazio heap Java. Le occorrenze successive di questa condizione non generano un avviso e-mail fino alla scadenza del periodo di ritardo specificato con `AS::monitorAlertGenerator.heapSpaceResetInterval`.
