---
description: Assets che appartengono a un set di immagini.
solution: Experience Manager
title: ImageSetMember
feature: Dynamic Media Classic,SDK/API,Image Sets
role: Developer,Admin
exl-id: f0857d98-be79-40a6-8a84-c2c7b4c423c5
TQID: 'https://experienceleague.adobe.com/53rc6Cq1i15GdzOpBek7ls7ixq4RN8z0OfZMOZsqYWI'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 68
ht-degree: 5%

---

# [!DNL ImageSetMember]{#imagesetmember}

Assets che appartengono a un set di immagini.

La reimpostazione della pagina implica che un [!DNL eCatalog] deve avviare una nuova pagina. `RenderSet` indica che fa parte di un campione `RenderSet`. Il valore è forzato a `true` per `eCatalog` e `RenderSet` set.

## Parametri {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Nome | Tipo | Descrizione |
|---|---|---|
| asset | `type:Asset` | Assets nell’array del set di immagini. |
| pageReset | `xsd:boolean` | Avvia una nuova pagina. L&#39;impostazione viene ignorata e il valore viene forzato a `true` per `eCatalog` e `RenderSet` set. |
