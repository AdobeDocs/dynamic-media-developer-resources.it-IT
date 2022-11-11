---
description: Risorse che appartengono a un set di immagini.
solution: Experience Manager
title: ImageSetMember
feature: Dynamic Media Classic,SDK/API,Image Sets
role: Developer,Admin
exl-id: f0857d98-be79-40a6-8a84-c2c7b4c423c5
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '68'
ht-degree: 7%

---

# [!DNL ImageSetMember]{#imagesetmember}

Risorse che appartengono a un set di immagini.

Per reimpostazione della pagina si intende un [!DNL eCatalog] deve iniziare una nuova pagina. `RenderSet` indica che fa parte di un `RenderSet` campione. Il valore viene forzato a `true` per `eCatalog` e `RenderSet` set.

## Parametri {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Nome | Tipo | Descrizione |
|---|---|---|
| asset | `type:Asset` | Risorse nell’array del set di immagini. |
| pageReset | `xsd:boolean` | Avvia una nuova pagina. L&#39;impostazione viene ignorata e il valore viene forzato `true` per `eCatalog` e `RenderSet` set. |
