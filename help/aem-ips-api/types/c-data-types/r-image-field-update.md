---
description: Aggiorna il campo immagine associato a una risorsa immagine.
solution: Experience Manager
title: ImageFieldUpdate
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 82bc016b-8a2b-4811-a0b4-1e2a93add3b6
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '61'
ht-degree: 8%

---

# ImageFieldUpdate{#imagefieldupdate}

Aggiorna il campo immagine associato a una risorsa immagine.

Sintassi

## Parametri {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Nome | Tipo | Descrizione |
|---|---|---|
| assetHandle | `xsd:string` | Gestione risorse. |
| resolution | `xsd:double` | Risoluzione dell&#39;immagine in pixel per pollice. |
| anchorX | `xsd:int` | Ancoraggio immagine asse X. |
| anchorY | `xsd:int` | Ancoraggio immagine asse Y. |
| Dati utente | `xsd:string` | Valore di `userData` campo metadati, pubblicato nel campo del catalogo dati utente del server di immagini. |
