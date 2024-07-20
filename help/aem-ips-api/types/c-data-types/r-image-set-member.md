---
description: Assets che appartengono a un set di immagini.
solution: Experience Manager
title: ImageSetMember
feature: Dynamic Media Classic,SDK/API,Image Sets
role: Developer,Admin
exl-id: f0857d98-be79-40a6-8a84-c2c7b4c423c5
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '68'
ht-degree: 5%

---

# [!DNL ImageSetMember]{#imagesetmember}

Assets che appartengono a un set di immagini.

La reimpostazione della pagina implica che un [!DNL eCatalog] deve avviare una nuova pagina. `RenderSet` indica che fa parte di un campione `RenderSet`. Il valore è forzato a `true` per `eCatalog` e `RenderSet` set.

## Parametri {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Nome | Tipo | Descrizione |
|---|---|---|
| asset | `type:Asset` | Assets nell’array del set di immagini. |
| pageReset | `xsd:boolean` | Avvia una nuova pagina. L&#39;impostazione viene ignorata e il valore viene forzato a `true` per `eCatalog` e `RenderSet` set. |
