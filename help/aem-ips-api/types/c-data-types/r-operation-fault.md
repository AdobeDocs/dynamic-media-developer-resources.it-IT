---
description: Messaggio dettagliato che risponde a uno degli URL forniti nella richiesta di annullamento della validità CDN.
solution: Experience Manager
title: OperationFault
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: e1fa7f66-f9d9-45cd-a9b3-d0ff344b137d
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '52'
ht-degree: 0%

---

# [!DNL OperationFault]{#operationfault}

Messaggio dettagliato che risponde a uno degli URL forniti nella richiesta di annullamento della validità CDN.

**Supportato da**

4.5.0, patch 2011-02

## Parametri {#section-cf4b0c923cef4c14869319af73ace58b}

| Nome **** | Tipo di **** | Descrizione **** |
|---|---|---|
| codice | `xsd:int` | Codice di errore fornito dal CDN |
| motivo | `xsd:string` | Messaggio di errore fornito dalla rete CDN |
