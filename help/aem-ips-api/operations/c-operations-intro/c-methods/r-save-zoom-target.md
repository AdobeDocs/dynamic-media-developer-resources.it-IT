---
description: Crea o modifica una destinazione di zoom.
solution: Experience Manager
title: saveZoomTarget
feature: Dynamic Media Classic, SDK/API
role: Developer,Administrator
exl-id: 595fd5c8-4e98-4c1a-b396-c8e170aaf454
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '129'
ht-degree: 19%

---

# saveZoomTarget{#savezoomtarget}

Crea o modifica una destinazione di zoom.

Sintassi

## Tipo utente autorizzato {#section-823cd9f0557045bca51da66768b5ba74}

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
| `*`companyHandle`*` | `xsd:string` | Sì | La maniglia dell&#39;azienda con la destinazione di zoom che si desidera salvare. |
| `*`assetHandle`*` | `xsd:string` | Sì | La maniglia della destinazione dello zoom. |
| `*`zoomTargetHandle`*` | `xsd:string` | No | Modifica o crea una destinazione di zoom. |
| `*`name`*` | `xsd:string` | Sì | Nome della destinazione dello zoom. |
| `*`xPosition`*` | `xsd:int` | Sì | Posizione del pixel sinistro. |
| `*`yPosition`*` | `xsd:int` | Sì | Posizione pixel superiore. |
| `*`width`*` | `xsd:int` | Sì | Zoom della larghezza della destinazione. |
| `*`height`*` | `xsd:int` | Sì | Zoom altezza destinazione. |
| `*`Dati utente`*` | `xsd:string` | Sì | Per informazioni specifiche per il cliente. Può contenere qualsiasi tipo di dati. |

**Output (saveZoomTargetReturn)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| `*`zoomTargetHandle`*` | `xsd:string` | Sì | Gestisci la nuova destinazione di zoom creata. |

## Esempi {#section-509c472c316549cdb228d7e1cfa8400a}

Questo esempio di codice salva una destinazione di zoom. La risposta restituisce la maniglia di destinazione dello zoom.

**Request Contents (Richiesta contenuto)**

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
