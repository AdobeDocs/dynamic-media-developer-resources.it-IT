---
description: L’aggiunta di nuovi file di dati è semplice e diretta, ma è necessario prestare particolare attenzione quando si sostituiscono file di dati esistenti utilizzati attivamente dal server. Invece di sostituire semplicemente tali file, si consiglia di assegnare al file sostitutivo un nuovo nome (ad esempio, aggiungere al nome del file un suffisso di versione). Una volta che il nuovo file è stato reso live, è possibile eliminare la versione precedente.
solution: Experience Manager
title: Eliminazione o sostituzione di file di dati
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 1624e1b5-ba79-45db-8309-457a44fddab8
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '319'
ht-degree: 0%

---

# Eliminazione o sostituzione di file di dati{#deleting-or-replacing-data-files}

L’aggiunta di nuovi file di dati è semplice e diretta, ma è necessario prestare particolare attenzione quando si sostituiscono file di dati esistenti utilizzati attivamente dal server. Invece di sostituire semplicemente tali file, si consiglia di assegnare al file sostitutivo un nuovo nome (ad esempio, aggiungere al nome del file un suffisso di versione). Una volta che il nuovo file è stato reso live, è possibile eliminare la versione precedente.

>[!NOTE]
>
>I file di dati non devono mai essere sostituiti o eliminati mentre sono in uso da Image Server. In caso contrario potrebbero verificarsi errori o anche un arresto anomalo del server.

In tutti i casi, ricorda che il [!DNL Platform Server] la cache e le voci della cache del client devono diventare obsolete prima che il client visualizzi i dati aggiornati. Voci specifiche della cache possono essere aggiornate immediatamente utilizzando `cache=validate` comando.

Le modifiche apportate ai file di font e ai file di profilo ICC non vengono registrate direttamente dal gestore della cache. Se una tale risorsa viene modificata senza modificarne l’ID, la cache del server non sarà a conoscenza della modifica e `cache=validate` non provocherà l’aggiornamento della voce della cache. `cache=update` può essere utilizzato per forzare la rigenerazione di tali voci della cache.

Per evitare complicazioni legate alla sostituzione dei file, si consiglia di assegnare un nuovo nome al file di sostituzione e di aggiornare le voci di catalogo corrispondenti. In questo modo è possibile sostituire qualsiasi file di dati mentre il server è attivo e rendere immediatamente obsolete le voci della cache del server senza alcun intervento aggiuntivo. Questo approccio può essere utilizzato per profili ICC, font e tutte le immagini gestite da cataloghi di immagini.
