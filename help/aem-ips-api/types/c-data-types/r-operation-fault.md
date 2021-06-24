---
description: Messaggio di dettaglio che risponde a uno degli URL forniti nella richiesta di invalidazione del CDN.
solution: Experience Manager
title: OperationFault
feature: Dynamic Media Classic, SDK/API
role: Developer,Administrator
exl-id: e1fa7f66-f9d9-45cd-a9b3-d0ff344b137d
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '54'
ht-degree: 7%

---

# OperationFault{#operationfault}

Messaggio di dettaglio che risponde a uno degli URL forniti nella richiesta di invalidazione del CDN.

**Supportato da**

4.5.0, patch 2011-02

## Parametri {#section-cf4b0c923cef4c14869319af73ace58b}

| ** Nome** | ** Tipo** | ** Descrizione** |
|---|---|---|
| `*`codice`*` | `xsd:int` | Codice di errore fornito dalla CDN |
| `*`motivo`*` | `xsd:string` | Messaggio di errore fornito dalla CDN |
