---
description: Crea o modifica una destinazione di zoom.
solution: Experience Manager
title: saveZoomTarget
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 595fd5c8-4e98-4c1a-b396-c8e170aaf454
TQID: 'https://experienceleague.adobe.com/rw-joRwkyumLI261ifPiWTeIgy4mvx-4MpgmaKcX5-E'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 125
ht-degree: 14%

---

# saveZoomTarget{#savezoomtarget}

Crea o modifica una destinazione di zoom.

Sintassi

## Tipo di utente autorizzato {#section-823cd9f0557045bca51da66768b5ba74}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parametri {#section-4a23983cae4e49a098e9bbe736933996}

**Input (saveZoomTargetParam)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| companyHandle | `xsd:string` | Sì | Handle per l&#39;azienda con la destinazione di zoom da salvare. |
| assetHandle | `xsd:string` | Sì | Maniglia della destinazione di zoom. |
| zoomTargetHandle | `xsd:string` | No | Modifica o crea una destinazione di zoom. |
| nome | `xsd:string` | Sì | Nome destinazione di zoom. |
| xPosition | `xsd:int` | Sì | Posizione pixel sinistro. |
| yPosition | `xsd:int` | Sì | Posizione dei pixel principali. |
| larghezza | `xsd:int` | Sì | Zoom larghezza destinazione. |
| altezza | `xsd:int` | Sì | Zoom dell&#39;altezza di destinazione. |
| userData | `xsd:string` | Sì | Per informazioni specifiche per il cliente. Può contenere qualsiasi tipo di dati. |

**Output (saveZoomTargetReturn)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| zoomTargetHandle | `xsd:string` | Sì | Gestisci la destinazione di zoom appena creata. |

## Esempi {#section-509c472c316549cdb228d7e1cfa8400a}

Questo esempio di codice salva una destinazione di zoom. La risposta restituisce l’handle della destinazione di zoom.

**Richiesta**

```java
<saveZoomTargetParam xmlns="http://www.scene7.com/IpsApi/xsd">
   <companyHandle>47</companyHandle>
   <assetHandle>24267|1|17063</assetHandle>
   <name>My Zoom Target</name>
   <xPosition>2</xPosition>
   <yPosition>2</yPosition>
   <width>10</width>
   <height>10</height>
   <userData>My User Data</userData>
</saveZoomTargetParam>
```

**Risposta**

```java
<saveZoomTargetReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <zoomTargetHandle>34194|9|301</zoomTargetHandle>
</saveZoomTargetReturn>
```
