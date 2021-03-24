---
description: Messaggio di dettaglio che risponde a uno degli URL forniti nella richiesta di invalidazione del CDN.
solution: Experience Manager
title: OperationFault
feature: Dynamic Media Classic, SDK/API
role: Sviluppatore,Amministratore
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
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

