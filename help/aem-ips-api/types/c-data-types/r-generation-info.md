---
description: Proprietà del file PostScript.
solution: Experience Manager
title: GenerationInfo
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 9aac2973-bbcb-4914-9bf9-203f0357527c
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '45'
ht-degree: 6%

---

# [!DNL GenerationInfo]{#generationinfo}

Proprietà del file PostScript.

Sintassi

## Parametri {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Nome | Tipo | Descrizione |
|---|---|---|
| [!DNL engine] | `xsd:string` | Motore di generazione utilizzato (vedere &quot;Informazioni sulla generazione&quot; per i valori). |
| [!DNL originator] | `types:Asset` | Record risorsa della risorsa principale utilizzata nella generazione. |
| [!DNL generated] | `types:Asset` | Record risorsa della risorsa generata. |
| attributeArray | `types:GenerationAttributeArray` | Array di attributi associati al processo di generazione. |
