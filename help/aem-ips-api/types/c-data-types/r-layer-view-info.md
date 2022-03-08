---
description: Proprietà della vista Livello.
solution: Experience Manager
title: InformazioniVisualizzazioneLivello
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 25199c86-1df0-41af-b210-e7668a60295e
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '47'
ht-degree: 8%

---

# InformazioniVisualizzazioneLivello{#layerviewinfo}

Proprietà della vista Livello.

Sintassi

## Parametri {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Nome | Tipo | Descrizione |
|---|---|---|
| url | `xsd:string` | URL del server di immagini che rappresenta il modello. Combinazioni `urlModifier` e `urlPostAp- plyModifier` campi. |
| urlModifier | `xsd:string` | Comandi del protocollo di trasmissione delle immagini da applicare prima della richiesta o `urlPostApplyModifier` comandi. |
| urlPostApplyModifier | `xsd:string` | Comandi del protocollo di servizio immagine da applicare dopo `urlModifier` e richiede i comandi. |
