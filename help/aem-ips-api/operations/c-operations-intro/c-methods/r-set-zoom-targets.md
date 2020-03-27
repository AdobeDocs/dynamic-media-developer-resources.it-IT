---
description: Imposta la destinazione di zoom associata a un’immagine di risorsa. Sovrascrive le destinazioni di zoom esistenti.
seo-description: Imposta la destinazione di zoom associata a un’immagine di risorsa. Sovrascrive le destinazioni di zoom esistenti.
seo-title: setZoomTargets
solution: Experience Manager
title: setZoomTargets
topic: Scene7 Image Production System API
uuid: 5d0aecec-ebd8-4c69-9514-c29fae347ee6
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# setZoomTargets{#setzoomtargets}

Imposta la destinazione di zoom associata a un’immagine di risorsa. Sovrascrive le destinazioni di zoom esistenti.

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
| ` *`companyHandle`*` | `xsd:string` | Sì | Maniglia aziendale. |
| ` *`assetHandle`*` | `xsd:string` | Sì | Risorsa con la destinazione di zoom da impostare. |
| ` *`zoomTargetArray`*` | `types:ZoomTargetDefinitionArray` | Sì | Array di definizioni delle destinazioni di zoom. |

**Output (setZoomTargetsReturn)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| ` *`zoomTargetHandleArray`*` | `types:HandleArray` | Sì | Set di maniglie alle destinazioni di zoom create da questa operazione. |

## Esempi {#section-a2f14c7a1499443e96d099ea8a76c182}

Questo esempio di codice definisce un array di destinazioni di zoom per nome, posizione (asse x e y), larghezza, altezza e assegna l’array a una risorsa. La risposta contiene le maniglie delle destinazioni di zoom appena create.

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

