---
description: Create o modificate una destinazione di zoom.
seo-description: Create o modificate una destinazione di zoom.
seo-title: saveZoomTarget
solution: Experience Manager
title: saveZoomTarget
topic: Scene7 Image Production System API
uuid: 197f7a2a-39ea-41cc-8e3a-76f9fe1b37d0
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# saveZoomTarget{#savezoomtarget}

Create o modificate una destinazione di zoom.

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
| ` *`companyHandle`*` | `xsd:string` | Sì | La maniglia della società con la destinazione di zoom da salvare. |
| ` *`assetHandle`*` | `xsd:string` | Sì | La maniglia della destinazione di zoom. |
| ` *`zoomTargetHandle`*` | `xsd:string` | No | Modifica o crea una destinazione di zoom. |
| ` *`name`*` | `xsd:string` | Sì | Nome destinazione di zoom. |
| ` *`xPosition`*` | `xsd:int` | Sì | Posizione in pixel a sinistra. |
| ` *`yPosition`*` | `xsd:int` | Sì | Posizione in pixel in alto. |
| ` *`width`*` | `xsd:int` | Sì | Zoom della larghezza di destinazione. |
| ` *`height`*` | `xsd:int` | Sì | Zoom altezza destinazione. |
| ` *`Dati utente`*` | `xsd:string` | Sì | Per informazioni specifiche per il cliente. Può contenere qualsiasi tipo di dati. |

**Output (saveZoomTargetReturn)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| ` *`zoomTargetHandle`*` | `xsd:string` | Sì | Consente di passare alla destinazione di zoom appena creata. |

## Esempi {#section-509c472c316549cdb228d7e1cfa8400a}

Questo esempio di codice salva una destinazione di zoom. La risposta restituisce la maniglia della destinazione di zoom.

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

