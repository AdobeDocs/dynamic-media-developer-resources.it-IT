---
description: Imposta o aggiorna un pacchetto di metadati XMP per una risorsa.
solution: Experience Manager
title: updateXMPPacket
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 04d85dba-cc86-4069-ab5d-9a5b3fe542c9
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '68'
ht-degree: 17%

---

# updateXMPPacket{#updatexmppacket}

Imposta o aggiorna un pacchetto di metadati XMP per una risorsa.

Sintassi

## Tipi di utenti autorizzati {#section-ee88a759f4774482a4734201a971f610}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalcontribUser`

## Parametri {#section-7a89621d441840faba639746b410a489}

**Input (updateXMPPacketParam)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| companyHandle | `xsd:string` | Sì | Gestore azienda. |
| assetHandle | `xsd:string` | Sì | Handle risorsa. |
| compressedPacket | `xsd:Base 64 binary` | Sì | [!DNL zlib-compressed] pacchetto XMP da impostare o aggiornare. |

**Output (updateXMPPacketReturn)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| success | `xsd:boolean` | Sì | Restituisce `true` se il pacchetto è stato aggiornato. |

## Esempi {#section-38b556b94e5044bf97a954519ff6c212}

**Richiesta**

```java
<ns:updateXMPPacketParam>
   <ns:companyHandle>c|680</ns:companyHandle>
   <ns:assetHandle>a|918567</ns:assetHandle>
   <ns:compressedPacket>H4sIAAAAAAAAAAGqAVX+eNqNU9FumzAUfc9XWN5rwTbpUGNBpC3RtpdqU9NOe3XABTRsU9sM8vezMUUp6qQhhDg
+955zfX2djXQUneCWgVG00tAxh6xUZ07dv19GEEwh9ncOP3kC/LrQ5KcAxxlGBUwxSEpPtLUm3NyDBeIdIghISkTuKU3qLwfzAQZkunymD8cvs5
lDOayt7ShCwzDEwzZWukJkt9sh7ESSyEVE5iItGyNpPniJoHHkptBNZxslgcfsrHqbQ7jxTkG8q5VVplbdYiFNPO0tLpRAC41IjNF1YlksGV2v2
6mkskC85YJLa1w8CfGLBH3SFZfFJYfbFXFglldKO+bn/ZpqrFv+xsS519WKO1mX9yyoHppveRXrgWTlxX9qJk0ojHG9eaBP3PtKnNaNRNJkq6lN
C8bO5sugbVa5/4Hnd05blc9y1zmGCCI0zcO50PyK40+q4LbWPt3IqGmykqnONnVgUUYNvsdfOH6wzN6C03OMd6zQb0KpSh3LPyoIWfgNKX1Vz4i
8rx5MSHHyX/D3L1+gMvRUL7NWE+sFH8+TvNxla7tx+8xdjuhqNPERMBaoBAAA=</ns:compressedPacket>
</ns:updateXMPPacketParam>
```

**Risposta**

```java
<updateXMPPacketReturn xmlns="http://www.scene7.com/IpsApi/xsd/2010-01-31">
   <success>true</success>
</updateXMPPacketReturn>
```
