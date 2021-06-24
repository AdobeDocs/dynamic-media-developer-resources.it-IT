---
description: Mentre l'aggiunta di nuovi file di dati è semplice e diretta, è necessario prestare particolare attenzione alla sostituzione dei file di dati esistenti utilizzati attivamente dal server. Invece di semplicemente sostituire tali file, si consiglia di assegnare al file di sostituzione un nuovo nome (ad esempio, aggiungere un suffisso di versione al nome del file). Una volta che il nuovo file è stato acquisito in tempo reale, è possibile eliminare la versione precedente.
solution: Experience Manager
title: Eliminazione o sostituzione dei file di dati
feature: Dynamic Media Classic, SDK/API
role: Developer,Administrator,Business Practitioner
exl-id: 1624e1b5-ba79-45db-8309-457a44fddab8
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '327'
ht-degree: 0%

---

# Eliminazione o sostituzione dei file di dati{#deleting-or-replacing-data-files}

Mentre l&#39;aggiunta di nuovi file di dati è semplice e diretta, è necessario prestare particolare attenzione alla sostituzione dei file di dati esistenti utilizzati attivamente dal server. Invece di semplicemente sostituire tali file, si consiglia di assegnare al file di sostituzione un nuovo nome (ad esempio, aggiungere un suffisso di versione al nome del file). Una volta che il nuovo file è stato acquisito in tempo reale, è possibile eliminare la versione precedente.

>[!NOTE]
>
>I file di dati non devono mai essere sostituiti o eliminati mentre sono in uso attivo da Image Serving. In caso contrario potrebbero verificarsi errori o anche arresti anomali del server.

In tutti i casi, ricorda che la cache del server Platform e le voci della cache client devono diventare obsolete prima che i dati aggiornati vengano visualizzati dal client. Le voci specifiche della cache possono essere aggiornate immediatamente utilizzando il comando `cache=validate` .

Le modifiche ai file di font e ai file di profilo ICC non vengono tracciate direttamente dal gestore della cache. Se una tale risorsa viene modificata senza modificare il suo ID, la cache del server non sarà a conoscenza della modifica e `cache=validate` non causerà l’aggiornamento della voce della cache. `cache=update` può essere utilizzato per forzare la rigenerazione di tali voci della cache.

Per evitare complicazioni nella sostituzione dei file, si consiglia di assegnare un nuovo nome a un file sostitutivo e aggiornare le voci di catalogo corrispondenti. Questo consentirà di sostituire qualsiasi file di dati mentre il server è in tempo reale e causerà l’obsolescenza immediata delle voci della cache del server senza alcun intervento aggiuntivo. Questo approccio può essere utilizzato per i profili ICC, i font e tutte le immagini gestite dai cataloghi di immagini.
