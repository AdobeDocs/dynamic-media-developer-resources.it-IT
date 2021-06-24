---
description: Imposta la destinazione di zoom associata a un’immagine di una risorsa. Sovrascrive le destinazioni di zoom esistenti.
solution: Experience Manager
title: setZoomTargets
feature: Dynamic Media Classic, SDK/API
role: Developer,Administrator
exl-id: 1b4ac729-00cf-4ea2-9098-60b4af3c7e6d
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '126'
ht-degree: 11%

---

# setZoomTargets{#setzoomtargets}

Imposta la destinazione di zoom associata a un’immagine di una risorsa. Sovrascrive le destinazioni di zoom esistenti.

Sintassi

## Tipi di utenti autorizzati {#section-c5e1863e9cb1426591bfea513620b6ab}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parametri {#section-161f8c733cc4439f94a06e12119d4226}

**Input (setZoomTargetsParam)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Sì | Tratta l&#39;azienda. |
| `*`assetHandle`*` | `xsd:string` | Sì | Risorsa con la destinazione di zoom da impostare. |
| `*`zoomTargetArray`*` | `types:ZoomTargetDefinitionArray` | Sì | Array di definizioni di destinazione dello zoom. |

**Output (setZoomTargetsReturn)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| `*`zoomTargetHandleArray`*` | `types:HandleArray` | Sì | Set di maniglie alle destinazioni di zoom create da questa operazione. |

## Esempi {#section-a2f14c7a1499443e96d099ea8a76c182}

Questo esempio di codice definisce una matrice di destinazioni di zoom per nome, posizione (asse x e y), larghezza, altezza e assegna la matrice a una risorsa. La risposta contiene le maniglie delle destinazioni di zoom appena create.

**Request Contents (Richiesta contenuto)**

```java
<setZoomTargetsParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|6</companyHandle>
   <assetHandle>a|739|1|537</assetHandle>
   <zoomTargetArray>
      <items>
         <name>zoomTarget2</name>
         <xPosition>40</xPosition>
         <yPosition>40</yPosition>
         <width>400</width>
         <height>400</height>
      </items>
      <items>
         <name>zoomTarget3</name>
         <xPosition>40</xPosition>
         <yPosition>40</yPosition>
         <width>400</width>
         <height>400</height>
      </items>
   </zoomTargetArray>
</setZoomTargetsParam>
```

**Risposta**

```java
<setZoomTargetsReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <zoomTargetHandleArray>
      <items>a|947|9|41</items>
      <items>a|948|9|42</items>
   </zoomTargetHandleArray>
</setZoomTargetsReturn>
```
