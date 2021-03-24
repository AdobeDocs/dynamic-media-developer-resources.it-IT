---
description: Risorse che appartengono a un set di immagini.
solution: Experience Manager
title: ImageSetMember
feature: Dynamic Media Classic, SDK/API, Set di immagini
role: Sviluppatore,Amministratore
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '78'
ht-degree: 6%

---


# ImageSetMember{#imagesetmember}

Risorse che appartengono a un set di immagini.

Per reimpostazione della pagina, [!DNL eCatalog] deve iniziare una nuova pagina. `RenderSet` indica che fa parte di un  `RenderSet` campione. Il valore viene forzato su `true` per i set `eCatalog` e `RenderSet`.

## Parametri {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Nome | Tipo | Descrizione |
|---|---|---|
| `*`asset`*` | `type:Asset` | Risorse nell’array del set di immagini. |
| `*`pageReset`*` | `xsd:boolean` | Avvia una nuova pagina. L&#39;impostazione viene ignorata e il valore viene forzato a `true` per i set `eCatalog` e `RenderSet`. |

