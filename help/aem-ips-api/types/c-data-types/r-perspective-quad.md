---
description: Le coordinate della posizione dell'immagine restituite dall'operazione getPhotoshopPath.
seo-description: Le coordinate della posizione dell'immagine restituite dall'operazione getPhotoshopPath.
seo-title: PerspectiveQuad
solution: Experience Manager
title: PerspectiveQuad
uuid: e83b7b8c-995b-4ac0-ace5-491f7e98674d
feature: Dynamic Media Classic, SDK/API
role: Sviluppatore,Amministratore
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '88'
ht-degree: 14%

---


# PerspectiveQuad{#perspectivequad}

Le coordinate della posizione dell&#39;immagine restituite dall&#39;operazione getPhotoshopPath.

Sintassi

## Parametri {#section-59792c446366456d90de7f5875bad1b0}

| Nome | Tipo | Descrizione |
|---|---|---|
| `*`x0`*` | `xsd:double` | Coordinata dell&#39;asse x in alto a sinistra. |
| `*`y0`*` | `xsd:double` | Coordinata dell&#39;asse y superiore sinistro. |
| `*`x1`*` | `xsd:double` | Coordinata dell&#39;asse x in alto a destra. |
| `*`y1`*` | `xsd:double` | Coordinata dell&#39;asse y superiore destra. |
| `*`x2`*` | `xsd:double` | Coordinata dell&#39;asse x in basso a destra. |
| `*`y2`*` | `xsd:double` | Coordinata dell&#39;asse y in basso a destra. |
| `*`x3`*` | `xsd:double` | Coordinata dell&#39;asse x in basso a sinistra. |
| `*`y3`*` | `xsd:double` | Coordinata dell&#39;asse y in basso a sinistra. |

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

