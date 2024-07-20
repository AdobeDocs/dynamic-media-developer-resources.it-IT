---
title: Risposte ai set di file multimediali
description: Le impostazioni in questa sezione si applicano alle risposte del set di file multimediali ottenute dal modificatore req=set.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: e3833726-d345-4741-8096-d74f299ac9fc
source-git-commit: 163ac6a6f44193f1b66ae24059630521d7247eae
workflow-type: tm+mt
source-wordcount: '146'
ht-degree: 0%

---

# Risposte ai set di file multimediali{#media-set-responses}

Le impostazioni in questa sezione si applicano alle risposte del set di file multimediali ottenute dal modificatore `req=set`.

## PS::fvctx.useCatalogRecordValidation - Criterio di memorizzazione nella cache {#section-9accb087d16548a988993bb30395a6f6}

Questa proprietà controlla i criteri di caching quando si determina se è necessario rigenerare una risposta del set recuperata da una cache. Se la proprietà è disabilitata, per la convalida viene utilizzato il timestamp del file [!DNL catalog.ini]. Se la proprietà è abilitata, per la convalida viene utilizzata la marca temporale `catalog::LastModified` più recente da tutti i record a cui si fa riferimento.

## PS::fvctx.nestingLimit - Limite di nidificazione {#section-280210341f1647fea02590e7069934d2}

Profondità massima di nidificazione di qualsiasi risposta `req=set`. Se questa profondità viene superata, viene restituito un errore.

## PS::fvctx.brochureLimit - Limite brochure {#section-fe36e47db49244cea7f07e9dd3639440}

Numero massimo di brochure di e-catalog nella risposta `req=set` che contiene tutti i metadati associati. Una volta superato questo limite, tutte le mappe private e i dati utente associati all’elemento della brochure vengono eliminati.
