---
description: Proprietà del file PostScript.
solution: Experience Manager
title: GenerationInfo
feature: Dynamic Media Classic, SDK/API
role: Developer,Administrator
exl-id: 9aac2973-bbcb-4914-9bf9-203f0357527c
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '54'
ht-degree: 7%

---

# GenerationInfo{#generationinfo}

Proprietà del file PostScript.

Sintassi

## Parametri {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Nome | Tipo | Descrizione |
|---|---|---|
| `*`motore`*` | `xsd:string` | Motore di generazione utilizzato (vedere &quot;Informazioni di generazione&quot; per i valori). |
| `*`creatore`*` | `types:Asset` | Record di risorsa della risorsa principale utilizzata nella generazione. |
| `*`generato`*` | `types:Asset` | Record risorsa della risorsa generata. |
| `*`attributeArray`*` | `types:GenerationAttributeArray` | Array di attributi associati al processo di generazione. |
