---
description: I file di vignettatura possono essere sostituiti o eliminati mentre il server è attivo utilizzando il comando req=release immediatamente prima della sovrascrittura del file.
solution: Experience Manager
title: Eliminazione o sostituzione dei file di dati di origine
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 9daf8534-a844-4f4a-8e99-8dc751acd550
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '207'
ht-degree: 0%

---

# Eliminazione o sostituzione dei file di dati di origine{#deleting-or-replacing-source-data-files}

I file di vignettatura possono essere sostituiti o eliminati mentre il server è attivo utilizzando il comando req=release immediatamente prima della sovrascrittura del file.

>[!NOTE]
>
>Un file di dati non deve essere sostituito o eliminato mentre il server di rendering vi accede.

L&#39;eliminazione o la sostituzione di un file di dati di origine determina solo la chiusura del file da parte del server di rendering fino alla successiva richiesta di accesso a tale vignettatura. Se un file viene utilizzato in modo intensivo, potrebbero essere necessari diversi tentativi.

Per sostituire altri file di dati, è necessario arrestare il server di rendering.

[!DNL Platform Server] voci della cache vengono invalidate automaticamente quando vengono sostituiti file di materiale o vignettature. La sostituzione dei file di profilo ICC non invalida le cache.

Per evitare complicazioni legate alla sostituzione dei file, si consiglia di assegnare un nuovo nome al file di sostituzione e di aggiornare le voci di catalogo corrispondenti. Questo consente di sostituire qualsiasi file di dati mentre il server è attivo e fa sì che le voci della cache del server diventino automaticamente obsolete senza alcun intervento aggiuntivo. Questo approccio può essere utilizzato per tutti i file di dati gestiti dai cataloghi di immagini.
