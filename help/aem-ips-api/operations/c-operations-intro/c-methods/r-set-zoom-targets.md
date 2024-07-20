---
description: Imposta la destinazione di zoom associata a un’immagine della risorsa. Sovrascrive le destinazioni di zoom esistenti.
solution: Experience Manager
title: setZoomTargets
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 1b4ac729-00cf-4ea2-9098-60b4af3c7e6d
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '121'
ht-degree: 9%

---

# setZoomTargets{#setzoomtargets}

Imposta la destinazione di zoom associata a un’immagine della risorsa. Sovrascrive le destinazioni di zoom esistenti.

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
| companyHandle | `xsd:string` | Sì | Gestore azienda. |
| assetHandle | `xsd:string` | Sì | Risorsa con la destinazione di zoom da impostare. |
| zoomTargetArray | `types:ZoomTargetDefinitionArray` | Sì | Array delle definizioni delle destinazioni di zoom. |

**Output (setZoomTargetsReturn)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| zoomTargetHandleArray | `types:HandleArray` | Sì | Set di handle per le destinazioni di zoom create dall&#39;operazione. |

## Esempi {#section-a2f14c7a1499443e96d099ea8a76c182}

Questo esempio di codice definisce una matrice di destinazioni di zoom per nome, posizione (assi x e y), larghezza, altezza e assegna la matrice a una risorsa. La risposta contiene handle per le nuove destinazioni di zoom create.

**Richiesta**

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
