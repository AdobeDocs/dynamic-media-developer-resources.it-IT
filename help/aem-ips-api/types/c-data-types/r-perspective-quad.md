---
description: Coordinate di posizione immagine restituite dall'operazione getPhotoshopPath.
solution: Experience Manager
title: PerspectiveQuad
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: dae44565-083d-47f5-8a08-2567590315a4
TQID: 'https://experienceleague.adobe.com/jJYhv5-HhU2t1CyVeRVzmIsprZ3xM4ZQtcMDS-Zgt6I'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 79
ht-degree: 5%

---

# [!DNL PerspectiveQuad]{#perspectivequad}

Coordinate di posizione immagine restituite dall&#39;operazione getPhotoshopPath.

Sintassi

## Parametri {#section-59792c446366456d90de7f5875bad1b0}

| Nome | Tipo | Descrizione |
|---|---|---|
| x0 | `xsd:double` | Coordinata dell&#39;asse x in alto a sinistra. |
| y0 | `xsd:double` | Coordinata dell&#39;asse y in alto a sinistra. |
| x1 | `xsd:double` | Coordinata dell&#39;asse x superiore destro. |
| y1 | `xsd:double` | Coordinata dell&#39;asse y superiore destro. |
| x2 | `xsd:double` | Coordinate dell&#39;asse x in basso a destra. |
| y2 | `xsd:double` | Coordinate dell&#39;asse y in basso a destra. |
| x3 | `xsd:double` | Coordinata asse x in basso a sinistra. |
| y3 | `xsd:double` | Coordinata dell&#39;asse y in basso a sinistra. |

## Esempio {#section-19ed4409ff3a41c9b52a9c9424612927}

Il tipo `PerspectiveQuad` restituisce i dati in questo ordine:

```
<complexType name="PerspectiveQuad">
        <sequence>
            <element name="x0" type="xsd:double"/>
            <element name="y0" type="xsd:double"/>
            <element name="x1" type="xsd:double"/>
            <element name="y1" type="xsd:double"/>
            <element name="x2" type="xsd:double"/>
            <element name="y2" type="xsd:double"/>
            <element name="x3" type="xsd:double"/>
            <element name="y3" type="xsd:double"/>
        </sequence>
```

>[!MORELIKETHIS]
>
>* [getPhotoshopPath](../../operations/c-operations-intro/c-methods/r-get-photoshop-path.md#reference-545f902f84194951ac04e947fdc803b9)
