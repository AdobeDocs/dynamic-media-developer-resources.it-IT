---
description: Proprietà della vista Livello.
seo-description: Proprietà della vista Livello.
seo-title: InformazioniVisualizzazioneLivello
solution: Experience Manager
title: InformazioniVisualizzazioneLivello
uuid: 58d26f4d-03a6-4f57-bc8e-117355c0d74c
feature: Dynamic Media Classic, SDK/API
role: Sviluppatore,Amministratore
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '58'
ht-degree: 6%

---


# LayerViewInfo{#layerviewinfo}

Proprietà della vista Livello.

Sintassi

## Parametri {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Nome | Tipo | Descrizione |
|---|---|---|
| `*`url`*` | `xsd:string` | URL del server di immagini che rappresenta il modello. Combina i campi `urlModifier` e `urlPostAp- plyModifier`. |
| `*`urlModifier`*` | `xsd:string` | Comandi del protocollo di trasmissione delle immagini da applicare prima dei comandi di richiesta o `urlPostApplyModifier`. |
| `*`urlPostApplyModifier`*` | `xsd:string` | Comandi del protocollo di trasmissione delle immagini da applicare dopo `urlModifier` e richiedere i comandi. |

