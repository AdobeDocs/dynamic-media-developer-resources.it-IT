---
description: Le voci della cache vengono aggiornate automaticamente utilizzando la convalida della cache basata sul catalogo o sulla scadenza, come selezionato con l'attributo CacheValidationPolicy (in default.ini o il file .ini di un catalogo di immagini specifico).
solution: Experience Manager
title: Convalida della cache della risposta
feature: Dynamic Media Classic, SDK/API
role: Developer,Administrator,Business Practitioner
exl-id: d2baa6e6-2700-450f-af1e-88b6d33d0e0c
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '305'
ht-degree: 0%

---

# Convalida della cache della risposta{#response-cache-validation}

Le voci della cache vengono aggiornate automaticamente utilizzando la convalida della cache basata su catalogo o su scadenza, come selezionato con attributo::CacheValidationPolicy (in default.ini o nel file .ini di un catalogo di immagini specifico).

Con la convalida basata su catalogo, una voce cache esistente viene considerata obsoleta se `catalog::LastModified` (o `attribute::LastModified`, o l’ora di modifica del file [!DNL catalog.ini]) è più recente del momento in cui è stata creata la voce cache.

Con la convalida basata sulla scadenza, una voce della cache diventa obsoleta dopo 5 minuti dalla convalida più recente. In entrambi i casi, il server convalida le voci della cache non aggiornate controllando le date dei file di tutti i file di immagine coinvolti nella creazione della richiesta. Se le date del file non sono state modificate, la marca temporale della voce cache viene aggiornata e la data cache viene considerata valida.

Per le applicazioni tipiche che coinvolgono principalmente immagini registrate nei cataloghi di immagini, la convalida basata su catalogo fornisce un vantaggio in termini di prestazioni. Le applicazioni che non richiedono cataloghi di immagini devono utilizzare la convalida della cache basata sulla scadenza. Un modo per farlo è impostare `attribute::cacheValidationPolicy=0` in [!DNL default.ini] e `1` in tutti i file di catalogo immagini specifici.

Le voci della cache diventano non valide e sono soggette a rigenerazione quando una voce del catalogo coinvolta nella richiesta cambia in modo tale da causare probabilmente una modifica dell&#39;immagine di risposta. Ad esempio, il contenuto di `catalog::Modifier` cambia.

>[!NOTE]
>
>Le immagini TIFF a piramide di Dynamic Media (PTIFF) mantengono la data del file internamente nell’intestazione del file a scopo di convalida. Il tempo di modifica dei file gestito dal file system viene utilizzato per verificare se un file non PTIFF è stato modificato.

Solo i file di immagine partecipano al processo di convalida della cache. Le modifiche ai file di font o ai file di profilo ICC non causano l’annullamento automatico della validità delle voci della cache.
