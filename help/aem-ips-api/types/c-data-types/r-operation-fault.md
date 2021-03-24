---
description: Messaggio di dettaglio che risponde a uno degli URL forniti nella richiesta di invalidazione del CDN.
solution: Experience Manager
title: OperationFault
feature: Dynamic Media Classic, SDK/API
role: Sviluppatore,Amministratore
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '56'
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

