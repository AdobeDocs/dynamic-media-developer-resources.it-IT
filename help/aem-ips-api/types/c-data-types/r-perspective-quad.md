---
description: Le coordinate della posizione dell'immagine restituite dall'operazione getPhotoshopPath.
seo-description: Le coordinate della posizione dell'immagine restituite dall'operazione getPhotoshopPath.
seo-title: PerspectiveQuad
solution: Experience Manager
title: PerspectiveQuad
topic: Scene7 Image Production System API
uuid: e83b7b8c-995b-4ac0-ace5-491f7e98674d
translation-type: tm+mt
source-git-commit: 22b447e66c223126f4e6b91f9a0102e86731c4a4

---


# PerspectiveQuad{#perspectivequad}

Le coordinate della posizione dell&#39;immagine restituite dall&#39;operazione getPhotoshopPath.

Sintassi

## Parametri {#section-59792c446366456d90de7f5875bad1b0}

| Nome | Tipo | Descrizione |
|---|---|---|
| ` *`x0`*` | `xsd:double` | Coordinata dell&#39;asse x superiore sinistro. |
| ` *`y0`*` | `xsd:double` | Coordinata dell&#39;asse y superiore sinistro. |
| ` *`x1`*` | `xsd:double` | Coordinata dell&#39;asse x superiore destro. |
| ` *`y1`*` | `xsd:double` | Coordinata dell&#39;asse y superiore destro. |
| ` *`x2`*` | `xsd:double` | Coordinata dell&#39;asse x inferiore destra. |
| ` *`y2`*` | `xsd:double` | Coordinata dell&#39;asse y inferiore destra. |
| ` *`x3`*` | `xsd:double` | Coordinata asse x in basso a sinistra. |
| ` *`y3`*` | `xsd:double` | Coordinata asse y in basso a sinistra. |

## Esempio {#section-19ed4409ff3a41c9b52a9c9424612927}

Il `PerspectiveQuad` tipo restituisce i dati nell&#39;ordine seguente:

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

