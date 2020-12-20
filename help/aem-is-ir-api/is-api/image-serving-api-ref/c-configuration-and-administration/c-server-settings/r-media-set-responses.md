---
description: Le impostazioni di questa sezione si applicano alle risposte al set di file multimediali ottenute dal modificatore req=set.
seo-description: Le impostazioni di questa sezione si applicano alle risposte al set di file multimediali ottenute dal modificatore req=set.
seo-title: Risposte ai set di file multimediali
solution: Experience Manager
title: Risposte ai set di file multimediali
topic: Scene7 Image Serving - Image Rendering API
uuid: 9fa6a38a-cd1f-499b-a2b6-e1a9a6c69ed0
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '165'
ht-degree: 0%

---


# Risposte ai set di file multimediali{#media-set-responses}

Le impostazioni di questa sezione si applicano alle risposte al set di file multimediali ottenute dal modificatore req=set.

## PS::fvctx.useCatalogRecordValidation - Criterio di memorizzazione nella cache {#section-9accb087d16548a988993bb30395a6f6}

Questa proprietà controlla il criterio di caching quando si determina se è necessario rigenerare la risposta recuperata dalla cache. Se la proprietà è disabilitata, per la convalida viene utilizzata la marca temporale del file [!DNL catalog.ini]. Se la proprietà è abilitata, per la convalida viene utilizzata la marca temporale `catalog::LastModified` più recente di tutti i record a cui si fa riferimento.

## PS::fvctx.nestingLimit - Limite di nidificazione {#section-280210341f1647fea02590e7069934d2}

La profondità massima di nidificazione di qualsiasi risposta `req=set`. Se questa profondità viene superata, viene restituito un errore.

## PS::fvctx.brochureLimit - Limite brochure {#section-fe36e47db49244cea7f07e9dd3639440}

Il numero massimo di brochure di e-Catalog nella risposta `req=set` che contiene tutti i metadati associati. Una volta superato tale limite, tutte le mappe private e i dati utente associati alla brochure vengono eliminati.
