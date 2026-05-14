---
description: Messaggio dettagliato che risponde a uno degli URL forniti nella richiesta di annullamento della validità CDN.
solution: Experience Manager
title: OperationFault
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: e1fa7f66-f9d9-45cd-a9b3-d0ff344b137d
TQID: 'https://experienceleague.adobe.com/1pOPC31lIN9SI3L1hBa1Ssm9ExFEnR6wFTFam8zIbNo'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 51
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
