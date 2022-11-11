---
title: AssetContextStateUpdate
description: Imposta un nuovo set di flag per lo stato di pubblicazione per il contesto di pubblicazione associato a una risorsa.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: ecbadafc-e77d-4c7e-a3d5-31c2b2a9b2ea
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '62'
ht-degree: 6%

---

# [!DNL AssetContextStateUpdate]{#assetcontextstateupdate}

Imposta un nuovo set di flag per lo stato di pubblicazione per il contesto di pubblicazione associato a una risorsa.

**Parametri**

| Nome | Tipo | Descrizione |
|---|---|---|
| assetHandle | `xsd:string` | Gestisci la risorsa da aggiornare. |
| contextStateUpdateArray | `types:ContextStateUpdateArray` | Array di stati di contatto di pubblicazione per la risorsa da aggiornare. |
