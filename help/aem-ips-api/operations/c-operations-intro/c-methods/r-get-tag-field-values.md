---
description: Ottiene tutti i valori dei dizionari di tag definiti per uno o più campi di tag.
solution: Experience Manager
title: getTagFieldValues
feature: Dynamic Media Classic, SDK/API
role: Sviluppatore,Amministratore
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '92'
ht-degree: 15%

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
| `*`companyHandle`*` | `xsd:string` | Sì | L&#39;handle della società contenente il campo tag. |
| `*`fieldHandleArray`*` | `types:HandleArray` | Sì | Matrice di handle di campo per assegnare tag ai valori da restituire. |

**Output (getTagFieldValuesReturn)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| `*`fieldArray`*` | `types:TagFieldValuesArray` | Sì | Matrice dei valori tag nel dizionario per ciascun campo richiesto. |

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

