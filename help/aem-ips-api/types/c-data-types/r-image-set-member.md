---
description: Risorse appartenenti a un set di immagini.
seo-description: Risorse appartenenti a un set di immagini.
seo-title: ImageSetMember
solution: Experience Manager
title: ImageSetMember
topic: Scene7 Image Production System API
uuid: bd013609-aed7-4c85-80f9-16be7fce99a3
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# ImageSetMember{#imagesetmember}

Risorse appartenenti a un set di immagini.

Per reimpostazione pagina si intende l’ [!DNL eCatalog] avvio di una nuova pagina. `RenderSet` indica che fa parte di un `RenderSet` campione. Il valore viene forzato `true` per `eCatalog` e `RenderSet` set.

## Parametri {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Nome | Tipo | Descrizione |
|---|---|---|
| ` *`asset`*` | `type:Asset` | Risorse nell’array dei set di immagini. |
| ` *`pageReset`*` | `xsd:boolean` | Inizia una nuova pagina. L&#39;impostazione viene ignorata e il valore viene forzato a `true` per `eCatalog` e `RenderSet` set. |

