---
description: Le voci della cache vengono aggiornate automaticamente utilizzando la convalida della cache basata su catalogo o basata su scadenza, come selezionato con l’attributo CacheValidationPolicy (nel file default.ini o nel file INI di un catalogo immagini specifico).
solution: Experience Manager
title: Convalida della cache di risposta
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: d2baa6e6-2700-450f-af1e-88b6d33d0e0c
source-git-commit: 38afaf2ed0f01868f02e236e941b23eed5b790aa
workflow-type: tm+mt
source-wordcount: '301'
ht-degree: 0%

---

# Convalida della cache di risposta{#response-cache-validation}

Le voci della cache vengono aggiornate automaticamente utilizzando la convalida della cache basata su catalogo o basata su scadenza, come selezionato con l&#39;attributo::CacheValidationPolicy (in default.ini o nel file INI di un catalogo immagini specifico).

Con la convalida basata sul catalogo, una voce della cache esistente viene considerata non aggiornata se `catalog::LastModified` (o `attribute::LastModified`, o l&#39;ora di modifica del file [!DNL catalog.ini]) è più recente dell&#39;ora di creazione della voce della cache.

Con la convalida basata sulla scadenza, una voce della cache diventa obsoleta dopo 5 minuti dalla convalida più recente. In entrambi i casi, il server convalida le voci della cache non aggiornate controllando le date di tutti i file di immagine coinvolti nella creazione della richiesta. Se le date del file non sono state modificate, il timestamp della voce della cache viene aggiornato e la data della cache viene considerata valida.

Per le tipiche applicazioni che coinvolgono principalmente immagini registrate in cataloghi di immagini, la convalida basata su catalogo offre un vantaggio in termini di prestazioni. Le applicazioni che non coinvolgono cataloghi di immagini devono utilizzare la convalida della cache basata sulla scadenza. Un modo per ottenere questo risultato è impostare `attribute::cacheValidationPolicy=0` in [!DNL default.ini] e `1` in tutti i file di catalogo immagini specifici.

Le voci della cache non sono più valide e sono soggette a rigenerazione quando una voce del catalogo coinvolta nella richiesta cambia in un modo che probabilmente causerebbe una modifica dell’immagine di risposta. Ad esempio, il contenuto di `catalog::Modifier` cambia.

>[!NOTE]
>
>Le immagini PTIFF (Dynamic Media pyramid TIFF) mantengono la data del file internamente nell’intestazione del file a scopo di convalida. Il tempo di modifica del file gestito dal file system viene utilizzato per verificare se un file non PTIFF è stato modificato.

Solo i file di immagine partecipano al processo di convalida della cache. Le modifiche apportate ai file di font o ai file di profilo ICC non causano l&#39;annullamento automatico della validità delle voci della cache.
