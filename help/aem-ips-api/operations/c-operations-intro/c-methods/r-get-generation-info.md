---
description: Restituisce 2 diversi tipi di informazioni in base ai parametri passati. cedatorHandle restituisce informazioni sulle risorse generate dalla risorsa specificata. generateHandle restituisce informazioni sui passaggi utilizzati per generare la risorsa o il file specificato.
solution: Experience Manager
title: getGenerationInfo
feature: Dynamic Media Classic, SDK/API
role: Developer,Administrator
exl-id: fa098e3c-8145-4238-a84c-c545f1c53341
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '201'
ht-degree: 8%

---

# getGenerationInfo{#getgenerationinfo}

Restituisce 2 diversi tipi di informazioni in base ai parametri passati. cedatorHandle restituisce informazioni sulle risorse generate dalla risorsa specificata. generateHandle restituisce informazioni sui passaggi utilizzati per generare la risorsa o il file specificato.

Sintassi

## Tipi di utenti autorizzati {#section-9cc2216b32c74107be07aeacecc11401}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parametri {#section-b7fa94c82147455888e8469fa5f6922b}

**Input (getGenerationInfoParam)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| `*`Frase di codice`*` | `xsd:string` | Sì | Il manico per l&#39;azienda. |
| `*`Frase di codice`*` | `xsd:string` | No | Il motore utilizzato nella generazione. Consultare Stili dei font. |
| `*`Frase di codice`*` | `xsd:string` | No | L’handle della risorsa da interrogare per le risorse generate. |
| `*`Frase di codice`*` | `xsd:string` | No | L’handle della risorsa da interrogare per le risorse e i motori utilizzati nella sua generazione. |
| `*`Frase di codice`*` | `xsd:StringArray` | No | Proprietà incluse nell’operazione. |
| `*`Frase di codice`*` | `xsd:StringArray` | No | Proprietà escluse dall’operazione. |

**Output (getGenerationInfoReturn)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| `*`generationArray`*` | `types:GenerationInfoArray` | Sì | Array di informazioni di generazione. |

## Esempi {#section-fdffe6ed82d94c7aa90e47f7ce889403}

Questo esempio di codice restituisce informazioni sulle risorse generate da una risorsa specifica. Non recupera informazioni sui passaggi utilizzati per generare la risorsa specificata. La risposta viene troncata per brevità.

**Request Contents (Richiesta contenuto)**

```java
<getGenerationInfoParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|6</companyHandle>
   <originatorHandle>a|716|25|160</originatorHandle>
</getGenerationInfoParam>
```

**Risposta**

```java
<getGenerationInfoReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <generationArray>
      <items>
         <engine>PostScriptRip</engine>
         <originator>
         ...
         </generated>
         <attributeArray/>
      </items>
   </generationArray>
</getGenerationInfoReturn>
```
