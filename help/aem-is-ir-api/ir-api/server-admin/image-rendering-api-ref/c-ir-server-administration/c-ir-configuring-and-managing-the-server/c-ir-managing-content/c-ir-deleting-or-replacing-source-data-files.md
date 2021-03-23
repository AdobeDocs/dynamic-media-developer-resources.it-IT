---
description: I file di vignetta possono essere sostituiti o eliminati mentre il server è attivo utilizzando il comando req=release immediatamente prima della sovrascrittura del file.
seo-description: I file di vignetta possono essere sostituiti o eliminati mentre il server è attivo utilizzando il comando req=release immediatamente prima della sovrascrittura del file.
seo-title: Eliminazione o sostituzione dei file di dati di origine
solution: Experience Manager
title: Eliminazione o sostituzione dei file di dati di origine
uuid: 13dc0489-7ab0-481e-b213-214affe9819e
feature: Dynamic Media Classic, SDK/API
role: Sviluppatore, amministratore, Business Practices
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '248'
ht-degree: 0%

---


# Eliminazione o sostituzione dei file di dati di origine{#deleting-or-replacing-source-data-files}

I file di vignetta possono essere sostituiti o eliminati mentre il server è attivo utilizzando il comando req=release immediatamente prima della sovrascrittura del file.

>[!NOTE]
>
>Un file di dati non deve essere sostituito o eliminato durante l&#39;accesso al server di rendering.

Tieni presente che l’eliminazione o la sostituzione di un file di dati di origine comporta solo la chiusura del file da parte del server di rendering fino alla successiva richiesta di accesso a tale vignetta. Se un file viene utilizzato in modo massiccio, potrebbero essere necessari diversi tentativi.

Per sostituire altri file di dati, è necessario arrestare il server di rendering.

Le voci della cache di Platform Server vengono invalidate automaticamente quando vengono sostituiti i file di materiale o le vignette. La sostituzione dei file di profilo ICC non invalida le cache.

Per evitare complicazioni nella sostituzione dei file, si consiglia di assegnare un nuovo nome a un file sostitutivo e aggiornare le voci di catalogo corrispondenti. Questo consente di sostituire qualsiasi file di dati mentre il server è attivo e fa sì che le voci della cache del server diventino obsolete automaticamente senza alcun intervento aggiuntivo. Questo approccio può essere utilizzato per tutti i file di dati gestiti dai cataloghi di immagini.
