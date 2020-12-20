---
description: Un avviso di priorità viene inviato quando lo spazio di heap gratuito Java è al di sotto della soglia specificata immediatamente dopo un ciclo di raccolta dei rifiuti Java.
seo-description: Un avviso di priorità viene inviato quando lo spazio di heap gratuito Java è al di sotto della soglia specificata immediatamente dopo un ciclo di raccolta dei rifiuti Java.
seo-title: Avviso priorità spazio heap
solution: Experience Manager
title: Avviso priorità spazio heap
topic: Scene7 Image Serving - Image Rendering API
uuid: 89956ad3-8a73-40db-92bd-326e3fab37ee
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---


# Avviso priorità spazio heap{#heap-space-priority-alert}

Un avviso di priorità viene inviato quando lo spazio di heap gratuito Java è al di sotto della soglia specificata immediatamente dopo un ciclo di raccolta dei rifiuti Java.

Gli avvisi ripetuti devono essere risolti aumentando lo spazio di heap Java. Le occorrenze successive di questa condizione non generano un avviso e-mail finché il periodo di ritardo specificato con `AS::monitorAlertGenerator.heapSpaceResetInterval` non è scaduto.
