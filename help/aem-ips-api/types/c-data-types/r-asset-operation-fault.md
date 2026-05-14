---
title: AssetOperationFault
description: Contiene informazioni sulle condizioni di avvertenza o di errore generate durante un'operazione di risorsa batch. I campi del codice e del motivo corrispondono ai campi del messaggio di errore che sarebbero stati generati per l'operazione non batch equivalente.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: c97fc35b-76f8-4ff7-a1ae-e5f9749f376c
TQID: 'https://experienceleague.adobe.com/LCiMAp-8grDIfCEGX3sF2kBhDamlxZ8iFHT1BjBLkCY'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 92
ht-degree: 3%

---

# [!DNL AssetOperationFault]{#assetoperationfault}

Contiene informazioni sulle condizioni di avvertenza o di errore generate durante un&#39;operazione di risorsa batch. I campi del codice e del motivo corrispondono ai campi del messaggio di errore che sarebbero stati generati per l&#39;operazione non batch equivalente.

Sintassi

## Parametri {#section-c906f052f43e4785ba46d92b514b0923}

| Nome | Tipo | Descrizione |
|---|---|---|
| assetHandle | `xsd:string` | Handle risorsa per l’operazione non riuscita. |
| codice | `xsd:int` | Codice di errore dell&#39;operazione. |
| motivo | `xsd:string` | Descrizione o motivo dell&#39;errore. |
