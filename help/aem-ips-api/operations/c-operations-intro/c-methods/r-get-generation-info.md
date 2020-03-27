---
description: Restituisce 2 diversi tipi di informazioni in base ai parametri passati. originatorHandle restituisce informazioni sulle risorse generate dalla risorsa specificata. generateHandle restituisce informazioni sui passaggi utilizzati per generare la risorsa o il file specificato.
seo-description: Restituisce 2 diversi tipi di informazioni in base ai parametri passati. originatorHandle restituisce informazioni sulle risorse generate dalla risorsa specificata. generateHandle restituisce informazioni sui passaggi utilizzati per generare la risorsa o il file specificato.
seo-title: getGenerationInfo
solution: Experience Manager
title: getGenerationInfo
topic: Scene7 Image Production System API
uuid: 4310a702-c08b-4479-9f57-9f2bc1d6b032
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# getGenerationInfo{#getgenerationinfo}

Restituisce 2 diversi tipi di informazioni in base ai parametri passati. originatorHandle restituisce informazioni sulle risorse generate dalla risorsa specificata. generateHandle restituisce informazioni sui passaggi utilizzati per generare la risorsa o il file specificato.

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
| ` *`Frase codice`*` | `xsd:string` | Sì | L&#39;handle della società. |
| ` *`Frase codice`*` | `xsd:string` | No | Il motore utilizzato nella generazione. Consultate Stili font. |
| ` *`Frase codice`*` | `xsd:string` | No | La maniglia della risorsa da sottoporre a query per le risorse generate. |
| ` *`Frase codice`*` | `xsd:string` | No | La maniglia della risorsa da interrogare per le risorse e i motori utilizzati nella generazione. |
| ` *`Frase codice`*` | `xsd:StringArray` | No | Proprietà incluse nell&#39;operazione. |
| ` *`Frase codice`*` | `xsd:StringArray` | No | Proprietà escluse dall&#39;operazione. |

**Output (getGenerationInfoReturn)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| ` *`generationArray`*` | `types:GenerationInfoArray` | Sì | Array di informazioni di generazione. |

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

