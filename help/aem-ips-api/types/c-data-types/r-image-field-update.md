---
description: Aggiorna il campo immagine associato a una risorsa immagine.
solution: Experience Manager
title: ImageFieldUpdate
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 82bc016b-8a2b-4811-a0b4-1e2a93add3b6
TQID: 'https://experienceleague.adobe.com/IsOZvDzvJTa0KJfUkYblEln9Qrx7nQm79FEEbnFVjiw'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 56
ht-degree: 5%

---

# [!DNL ImageFieldUpdate]{#imagefieldupdate}

Aggiorna il campo immagine associato a una risorsa immagine.

Sintassi

## Parametri {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Nome | Tipo | Descrizione |
|---|---|---|
| assetHandle | `xsd:string` | Handle risorsa. |
| [!DNL resolution] | `xsd:double` | Risoluzione immagine in pixel per pollice. |
| [!DNL anchorX] | `xsd:int` | Ancoraggio immagine asse X. |
| [!DNL anchorY] | `xsd:int` | Ancoraggio immagine asse Y. |
| [!DNL userData] | `xsd:string` | Valore del campo di metadati `userData`, pubblicato nel campo del catalogo dati utente di Image Server. |
