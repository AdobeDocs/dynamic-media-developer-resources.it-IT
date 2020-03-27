---
description: Le voci della cache vengono aggiornate automaticamente utilizzando la convalida della cache basata su catalogo o sulla scadenza, come selezionata con l'attributo CacheValidationPolicy (in default.ini o nel file .ini di un catalogo immagini specifico).
seo-description: Le voci della cache vengono aggiornate automaticamente utilizzando la convalida della cache basata su catalogo o sulla scadenza, come selezionata con l'attributo CacheValidationPolicy (in default.ini o nel file .ini di un catalogo immagini specifico).
seo-title: Convalida cache di risposta
solution: Experience Manager
title: Convalida cache di risposta
topic: Scene7 Image Serving - Image Rendering API
uuid: d1aad5ae-f0fa-489b-a48b-b0ac8c8f43bb
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Convalida cache di risposta{#response-cache-validation}

Le voci della cache vengono aggiornate automaticamente utilizzando la convalida della cache basata su catalogo o sulla scadenza, come selezionata con l&#39;attributo::CacheValidationPolicy (in default.ini o nel file .ini di un catalogo immagini specifico).

Con la convalida basata su catalogo, una voce cache esistente viene considerata obsoleta se `catalog::LastModified` (o `attribute::LastModified`, o se il tempo di modifica del file del [!DNL catalog.ini] file) è più recente rispetto all&#39;ora in cui è stata creata la voce della cache.

Con la convalida basata sulla scadenza, una voce della cache diventa obsoleta dopo 5 minuti dalla convalida più recente. In entrambi i casi, il server convalida le voci della cache scadenti controllando le date dei file di tutti i file di immagine coinvolti nella creazione della richiesta. Se le date del file non sono cambiate, l&#39;indicatore di data e ora della voce della cache viene aggiornato e la data memorizzata nella cache viene considerata valida.

Per le applicazioni tipiche che coinvolgono principalmente immagini registrate nei cataloghi di immagini, la convalida basata su catalogo offre un vantaggio in termini di prestazioni. Le applicazioni che non richiedono cataloghi di immagini devono utilizzare la convalida della cache basata sulla scadenza. Un modo per ottenere questo risultato è impostare `attribute::cacheValidationPolicy=0` in [!DNL default.ini]e `1` in tutti i file di catalogo immagini specifici.

Le voci della cache diventano non valide e sono soggette a rigenerazione quando una voce del catalogo coinvolta nella richiesta cambia in modo tale da causare probabilmente una modifica dell&#39;immagine di risposta. Ad esempio, il contenuto delle `catalog::Modifier` modifiche.

>[!NOTE] {class=&quot;- topic/note &quot;}
>
>Le immagini TIFF (PTIFF) piramidali di Scene7 mantengono la data del file internamente nell’intestazione del file a scopo di convalida. Il tempo di modifica del file gestito dal file system viene utilizzato per verificare se un file non PTIFF è stato modificato.

Solo i file di immagine partecipano al processo di convalida della cache. Le modifiche apportate ai file di font o ai file di profilo ICC non causano l&#39;annullamento automatico della convalida delle voci della cache.
