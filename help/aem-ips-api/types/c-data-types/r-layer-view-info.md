---
description: Proprietà della visualizzazione dei livelli.
seo-description: Proprietà della visualizzazione dei livelli.
seo-title: LayerViewInfo
solution: Experience Manager
title: LayerViewInfo
topic: Scene7 Image Production System API
uuid: 58d26f4d-03a6-4f57-bc8e-117355c0d74c
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '51'
ht-degree: 7%

---


# LayerViewInfo{#layerviewinfo}

Proprietà della visualizzazione dei livelli.

Sintassi

## Parametri {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Nome | Tipo | Descrizione |
|---|---|---|
| ` *`url`*` | `xsd:string` | URL del server immagini che rappresenta il modello. Combina i campi `urlModifier` e `urlPostAp- plyModifier`. |
| ` *`urlModifier`*` | `xsd:string` | Comandi del protocollo di trasmissione delle immagini da applicare prima della richiesta o dei comandi `urlPostApplyModifier`. |
| ` *`urlPostApplyModifier`*` | `xsd:string` | Comandi del protocollo di trasmissione delle immagini da applicare dopo `urlModifier` e richiedere i comandi. |

