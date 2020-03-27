---
description: I file di vignettatura possono essere sostituiti o eliminati mentre il server è attivo utilizzando il comando req=release subito prima della sovrascrittura del file.
seo-description: I file di vignettatura possono essere sostituiti o eliminati mentre il server è attivo utilizzando il comando req=release subito prima della sovrascrittura del file.
seo-title: Eliminazione o sostituzione dei file di dati di origine
solution: Experience Manager
title: Eliminazione o sostituzione dei file di dati di origine
topic: Scene7 Image Serving - Image Rendering API
uuid: 13dc0489-7ab0-481e-b213-214affe9819e
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Eliminazione o sostituzione dei file di dati di origine{#deleting-or-replacing-source-data-files}

I file di vignettatura possono essere sostituiti o eliminati mentre il server è attivo utilizzando il comando req=release subito prima della sovrascrittura del file.

>[!NOTE] {class=&quot;- topic/note &quot;}
>
>Un file di dati non deve essere sostituito o eliminato mentre il server di rendering vi accede.

Tenere presente che l’eliminazione o la sostituzione di un file di dati di origine comporta solo la chiusura del file da parte del server di rendering fino alla richiesta successiva che accede a tale vignettatura. Se un file viene utilizzato in modo eccessivo, potrebbero essere necessari diversi tentativi.

Il server di rendering deve essere arrestato per sostituire altri file di dati.

Le voci della cache di Platform Server vengono automaticamente invalidate quando vengono sostituiti i file di materiale o le vignettature. La sostituzione dei file di profilo ICC non invalida le cache.

Per evitare complicazioni nella sostituzione dei file, si consiglia di assegnare a un file sostitutivo un nuovo nome e aggiornare le voci di catalogo corrispondenti. Questo consente di sostituire qualsiasi file di dati mentre il server è attivo e le voci della cache del server diventano automaticamente obsolete senza alcun intervento aggiuntivo. Questo approccio può essere utilizzato per tutti i file di dati gestiti da cataloghi di immagini.
