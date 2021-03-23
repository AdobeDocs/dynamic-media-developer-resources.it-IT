---
description: Risorse che appartengono a un set di immagini.
seo-description: Risorse che appartengono a un set di immagini.
seo-title: ImageSetMember
solution: Experience Manager
title: ImageSetMember
uuid: bd013609-aed7-4c85-80f9-16be7fce99a3
feature: Dynamic Media Classic, SDK/API, Set di immagini
role: Sviluppatore,Amministratore
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '86'
ht-degree: 5%

---


# ImageSetMember{#imagesetmember}

Risorse che appartengono a un set di immagini.

Per reimpostazione della pagina, [!DNL eCatalog] deve iniziare una nuova pagina. `RenderSet` indica che fa parte di un  `RenderSet` campione. Il valore viene forzato su `true` per i set `eCatalog` e `RenderSet`.

## Parametri {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Nome | Tipo | Descrizione |
|---|---|---|
| `*`asset`*` | `type:Asset` | Risorse nell’array del set di immagini. |
| `*`pageReset`*` | `xsd:boolean` | Avvia una nuova pagina. L&#39;impostazione viene ignorata e il valore viene forzato a `true` per i set `eCatalog` e `RenderSet`. |

