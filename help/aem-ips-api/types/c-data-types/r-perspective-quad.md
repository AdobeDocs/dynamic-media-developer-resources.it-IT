---
description: Coordinate di posizione immagine restituite dall'operazione getPhotoshopPath.
solution: Experience Manager
title: PerspectiveQuad
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: dae44565-083d-47f5-8a08-2567590315a4
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '71'
ht-degree: 16%

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

Il `PerspectiveQuad` type restituisce i dati nell&#39;ordine seguente:

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

