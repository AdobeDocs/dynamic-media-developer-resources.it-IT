---
description: Le impostazioni in questa sezione si applicano alle risposte del set di file multimediali ottenute dal modificatore req=set .
solution: Experience Manager
title: Risposte al set di file multimediali
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '155'
ht-degree: 0%

---


# Risposte al set di file multimediali{#media-set-responses}

Le impostazioni in questa sezione si applicano alle risposte del set di file multimediali ottenute dal modificatore req=set .

## PS::fvctx.useCatalogRecordValidation - Criterio di memorizzazione nella cache {#section-9accb087d16548a988993bb30395a6f6}

Questa proprietà controlla il criterio di caching quando si determina se è necessario rigenerare o meno la risposta recuperata dalla cache. Se la proprietà è disabilitata, per la convalida viene utilizzata la marca temporale del file [!DNL catalog.ini] . Se la proprietà è abilitata, per la convalida viene utilizzata la marca temporale più recente `catalog::LastModified` di tutti i record a cui si fa riferimento.

## PS::fvctx.nestingLimit - Limite di nidificazione {#section-280210341f1647fea02590e7069934d2}

La profondità massima di nidificazione di qualsiasi risposta `req=set`. Se questa profondità viene superata, viene restituito un errore.

## PS::fvctx.brochureLimit - Limite della brochure {#section-fe36e47db49244cea7f07e9dd3639440}

Il numero massimo di brochure dell&#39;e-catalog nella risposta `req=set` che contiene tutti i metadati associati. Una volta superato questo limite, vengono soppresse tutte le mappe private e i dati utente associati alla voce della brochure.
