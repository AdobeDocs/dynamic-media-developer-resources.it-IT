---
description: Proprietà della vista livello.
solution: Experience Manager
title: InfoVistaLivello
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 25199c86-1df0-41af-b210-e7668a60295e
TQID: 'https://experienceleague.adobe.com/cx-B-BmcEP6vefJY5tsrNMZcwWIKM-pW0CYfP7BjxMM'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 46
ht-degree: 6%

---

# [!DNL LayerViewInfo]{#layerviewinfo}

Proprietà della vista livello.

Sintassi

## Parametri {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Nome | Tipo | Descrizione |
|---|---|---|
| url | `xsd:string` | URL del server immagini che rappresenta il modello. Combina `urlModifier` e `urlPostAp- plyModifier` campi. |
| urlModifier | `xsd:string` | Comandi del protocollo Image Server da applicare prima della richiesta o di `urlPostApplyModifier` comandi. |
| urlPostApplyModifier | `xsd:string` | Comandi del protocollo Image Server da applicare dopo `urlModifier` e richiedere comandi. |
