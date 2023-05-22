---
description: Le impostazioni in questa sezione si applicano alle risposte del set di file multimediali ottenute dal modificatore req=set.
solution: Experience Manager
title: Risposte ai set di file multimediali
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: e3833726-d345-4741-8096-d74f299ac9fc
source-git-commit: 38afaf2ed0f01868f02e236e941b23eed5b790aa
workflow-type: tm+mt
source-wordcount: '146'
ht-degree: 0%

---

# Risposte ai set di file multimediali{#media-set-responses}

Le impostazioni in questa sezione si applicano alle risposte del set di file multimediali ottenute dal modificatore req=set.

## PS::fvctx.useCatalogRecordValidation - Criterio di memorizzazione nella cache {#section-9accb087d16548a988993bb30395a6f6}

Questa proprietà controlla i criteri di caching quando si stabilisce se è necessario rigenerare o meno la risposta del set recuperata dalla cache. Se la proprietà è disabilitata, la marca temporale del [!DNL catalog.ini] per la convalida. Se la proprietà è abilitata, l’ultima `catalog::LastModified` per la convalida viene utilizzata la marca temporale di tutti i record a cui si fa riferimento.

## PS::fvctx.nestingLimit - Limite di nidificazione {#section-280210341f1647fea02590e7069934d2}

Profondità massima di nidificazione di qualsiasi `req=set` risposta. Se questa profondità viene superata, viene restituito un errore.

## PS::fvctx.brochureLimit - Limite brochure {#section-fe36e47db49244cea7f07e9dd3639440}

Numero massimo di brochure di cataloghi elettronici nel `req=set` che contiene tutti i metadati associati. Una volta superato questo limite, tutte le mappe private e i dati utente associati all’elemento della brochure vengono eliminati.
