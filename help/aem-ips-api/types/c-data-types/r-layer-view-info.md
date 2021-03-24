---
description: Proprietà della vista Livello.
solution: Experience Manager
title: InformazioniVisualizzazioneLivello
feature: Dynamic Media Classic, SDK/API
role: Sviluppatore,Amministratore
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '54'
ht-degree: 7%

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

