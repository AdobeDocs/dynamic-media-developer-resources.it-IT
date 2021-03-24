---
description: Le coordinate della posizione dell'immagine restituite dall'operazione getPhotoshopPath.
solution: Experience Manager
title: PerspectiveQuad
feature: Dynamic Media Classic, SDK/API
role: Sviluppatore,Amministratore
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '79'
ht-degree: 16%

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

