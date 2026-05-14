---
title: Risposte ai set di file multimediali
description: Le impostazioni in questa sezione si applicano alle risposte del set di file multimediali ottenute dal modificatore req=set.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: e3833726-d345-4741-8096-d74f299ac9fc
TQID: 'https://experienceleague.adobe.com/FNUguOqf8f5FnIeGTzheZU-8zCXqwRMU3YGyvYDA0uM'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 147
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
