---
description: Esegui il targeting per un’azione di clic nel browser.
solution: Experience Manager
title: Mappa immagine
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 123eba56-2a59-44c5-93f0-205c362d071d
TQID: 'https://experienceleague.adobe.com/ikMxCQ23L0HzbfmRlcYGL-fRJFK2uhwbZHNzcy1c25k'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 91
ht-degree: 3%

---

# [!DNL ImageMap]{#imagemap}

Esegui il targeting per un’azione di clic nel browser.

Sempre associato a un&#39;immagine. È possibile ottenere una destinazione `ImageMap` da `ImageInfo`.

## Parametri {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Nome | Tipo | Descrizione |
|---|---|---|
| imageMapHandle | `xsd:string` | Handle mappa immagine. |
| [!DNL name] | `xsd:string` | Nome mappa immagine. |
| [!DNL region] | `xsd:string` | Coordinate mappa immagine. Il formato è basato sull&#39;attributo tag `<area>` di HTML. |
| [!DNL action] | `xsd:string` | Altri attributi da includere nel tag HTML `<area>`, incluso l&#39;URL `href`. |
| shapeType | `xsd:boolean` | Un valore [!DNL RegionShape]. |
| [!DNL position] | `xsd:string` | Posizione nel formato dell&#39;attributo [!DNL coords] dell&#39;elemento `<area>` di HTML. Esempio: `coords ="0,0,84,128"`. |
| [!DNL enabled] | `xsd:boolean` | True se la mappa immagine è abilitata. |
| lastModified | `xsd:dateTime` | Data e ora dell&#39;ultima modifica apportata alla mappa immagine. |
