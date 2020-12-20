---
description: Ottiene tutti i valori dei dizionari di tag definiti per uno o più campi di tag.
seo-description: Ottiene tutti i valori dei dizionari di tag definiti per uno o più campi di tag.
seo-title: getTagFieldValues
solution: Experience Manager
title: getTagFieldValues
topic: Scene7 Image Production System API
uuid: 92d84dfc-6a6c-4876-9670-1152adb6317c
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '98'
ht-degree: 14%

---


# getTagFieldValues{#gettagfieldvalues}

Ottiene tutti i valori dei dizionari di tag definiti per uno o più campi di tag.

Sintassi

## Tipi di utenti autorizzati {#section-cc36a437394c491594e704a08a161c87}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parametri {#section-9ad806e7736e4d51ae42cad185050cf9}

**Input (getTagFieldValuesReturn)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | Sì | L’handle della società che contiene il campo del tag. |
| ` *`fieldHandleArray`*` | `types:HandleArray` | Sì | Un array di handle di campo per assegnare i tag ai valori da restituire. |

**Output (getTagFieldValuesReturn)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| ` *`fieldArray`*` | `types:TagFieldValuesArray` | Sì | Un array di valori di tag nel dizionario per ciascun campo richiesto. |

## Esempi {#section-4492742614e44bb191a7d397dc1a1407}

**Request Contents (Richiesta contenuto)**

```java
<getTagFieldValuesParam xmlns="http://www.scene7.com/IpsApi/xsd/2010-01-31">
   <companyHandle>c|3</companyHandle>
   <fieldHandleArray>
      <items>m|3|ASSET|SingleOpenTag</items>
      <items>m|3|ASSET|SingleFixedTag</items>
   </fieldHandleArray>
</getTagFieldValuesParam>
```

**Risposta**

```java
<getTagFieldValuesReturn xmlns="http://www.scene7.com/IpsApi/xsd/2010-01-31">
   <fieldArray>
      <items>
         <fieldHandle>m|3|ASSET|SingleOpenTag</fieldHandle>
         <valueArray>
            <items>GroupB</items>
            <items>GroupA</items>
         </valueArray>
      </items>
      <items>
         <fieldHandle>m|3|ASSET|SingleFixedTag</fieldHandle>
         <valueArray>
            <items>North</items>
            <items>South</items>
            <items>East</items><items>West</items>
         </valueArray>
      </items>
   </fieldArray>
</getTagFieldValuesReturn>
```

