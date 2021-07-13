---
description: Viene inviato un avviso di priorità quando lo spazio di heap Java gratuito si trova al di sotto della soglia specificata immediatamente dopo un ciclo di raccolta degli oggetti inattivi Java.
solution: Experience Manager
title: Avviso prioritario spazio di heap
feature: Dynamic Media Classic, SDK/API
role: Developer,Administrator,User
exl-id: 32951003-386f-4ea2-a5a0-f4d2e6d95ba5
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '90'
ht-degree: 0%

---

# Avviso prioritario spazio di heap{#heap-space-priority-alert}

Viene inviato un avviso di priorità quando lo spazio di heap Java gratuito si trova al di sotto della soglia specificata immediatamente dopo un ciclo di raccolta degli oggetti inattivi Java.

Gli avvisi ripetuti devono essere risolti aumentando lo spazio di heap Java. Le occorrenze successive di questa condizione non generano un avviso e-mail fino alla scadenza del periodo di ritardo specificato con `AS::monitorAlertGenerator.heapSpaceResetInterval`.
