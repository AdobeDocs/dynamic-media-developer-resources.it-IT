---
description: Risorse che appartengono a un set di immagini.
solution: Experience Manager
title: ImageSetMember
feature: Dynamic Media Classic, SDK/API, Set di immagini
role: Developer,Administrator
exl-id: f0857d98-be79-40a6-8a84-c2c7b4c423c5
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '76'
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
