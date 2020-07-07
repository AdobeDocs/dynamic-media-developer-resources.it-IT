---
description: Mentre l'aggiunta di nuovi file di dati è semplice e lineare, occorre prestare particolare attenzione alla sostituzione dei file di dati esistenti che sono attivamente utilizzati dal server. Invece di sostituire semplicemente tali file, si consiglia di assegnare al file sostitutivo un nuovo nome (ad esempio, aggiungere un suffisso di versione al nome del file). Dopo che il nuovo file è stato acquisito dal vivo, è possibile eliminare la versione precedente.
seo-description: Mentre l'aggiunta di nuovi file di dati è semplice e lineare, occorre prestare particolare attenzione alla sostituzione dei file di dati esistenti che sono attivamente utilizzati dal server. Invece di sostituire semplicemente tali file, si consiglia di assegnare al file sostitutivo un nuovo nome (ad esempio, aggiungere un suffisso di versione al nome del file). Dopo che il nuovo file è stato acquisito dal vivo, è possibile eliminare la versione precedente.
seo-title: Eliminazione o sostituzione dei file di dati
solution: Experience Manager
title: Eliminazione o sostituzione dei file di dati
topic: Scene7 Image Serving - Image Rendering API
uuid: 7b446144-48f6-4b50-93ec-0287425d932a
translation-type: tm+mt
source-git-commit: e8e5b07329bde3e23ee095d5022da62d67e9478c
workflow-type: tm+mt
source-wordcount: '393'
ht-degree: 0%

---


# Eliminazione o sostituzione dei file di dati{#deleting-or-replacing-data-files}

Mentre l&#39;aggiunta di nuovi file di dati è semplice e lineare, occorre prestare particolare attenzione alla sostituzione dei file di dati esistenti che sono attivamente utilizzati dal server. Invece di sostituire semplicemente tali file, si consiglia di assegnare al file sostitutivo un nuovo nome (ad esempio, aggiungere un suffisso di versione al nome del file). Dopo che il nuovo file è stato acquisito dal vivo, è possibile eliminare la versione precedente.

>[!NOTE]
>
>I file di dati non devono mai essere sostituiti o eliminati durante l’utilizzo attivo da Image Server. In caso contrario si potrebbero verificare errori o addirittura un arresto anomalo del server.

In tutti i casi, ricordate che la cache di Platform Server e le voci della cache client devono diventare obsolete prima che i dati aggiornati vengano visualizzati dal client. È possibile aggiornare immediatamente determinate voci della cache utilizzando il `cache=validate` comando.

Le modifiche apportate ai file di font e ai file di profilo ICC non vengono tracciate direttamente dal gestore cache. Se tale risorsa viene modificata senza modificarne l’ID, la cache del server non sarà a conoscenza della modifica e non `cache=validate` causerà l’aggiornamento della voce della cache. `cache=update` può essere utilizzato per forzare la rigenerazione di tali voci della cache.

Per evitare complicazioni nella sostituzione dei file, si consiglia di assegnare a un file sostitutivo un nuovo nome e aggiornare le voci di catalogo corrispondenti. Questo consentirà di sostituire qualsiasi file di dati mentre il server è attivo e le voci della cache del server diventano immediatamente obsolete senza alcun intervento aggiuntivo. Questo approccio può essere utilizzato per i profili ICC, i font e tutte le immagini gestite dai cataloghi di immagini.
