---
description: Proprietà della vista Livello.
solution: Experience Manager
title: InformazioniVisualizzazioneLivello
feature: Dynamic Media Classic, SDK/API
role: Developer,Administrator
exl-id: 25199c86-1df0-41af-b210-e7668a60295e
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '52'
ht-degree: 7%

---

# InformazioniVisualizzazioneLivello{#layerviewinfo}

Proprietà della vista Livello.

Sintassi

## Parametri {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Nome | Tipo | Descrizione |
|---|---|---|
| `*`url`*` | `xsd:string` | URL del server di immagini che rappresenta il modello. Combina i campi `urlModifier` e `urlPostAp- plyModifier`. |
| `*`urlModifier`*` | `xsd:string` | Comandi del protocollo di trasmissione delle immagini da applicare prima dei comandi di richiesta o `urlPostApplyModifier`. |
| `*`urlPostApplyModifier`*` | `xsd:string` | Comandi del protocollo di trasmissione delle immagini da applicare dopo `urlModifier` e richiedere i comandi. |
