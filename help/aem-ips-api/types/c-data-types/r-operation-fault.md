---
description: Messaggio di dettaglio che risponde a uno degli URL forniti nella richiesta di invalidazione del CDN.
solution: Experience Manager
title: OperationFault
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: e1fa7f66-f9d9-45cd-a9b3-d0ff344b137d
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '48'
ht-degree: 8%

---

# [!DNL OperationFault]{#operationfault}

Messaggio di dettaglio che risponde a uno degli URL forniti nella richiesta di invalidazione del CDN.

**Supportato da**

4.5.0, patch 2011-02

## Parametri {#section-cf4b0c923cef4c14869319af73ace58b}

| ** Nome** | ** Tipo** | ** Descrizione** |
|---|---|---|
| codice | `xsd:int` | Codice di errore fornito dalla CDN |
| motivo | `xsd:string` | Messaggio di errore fornito dalla CDN |
