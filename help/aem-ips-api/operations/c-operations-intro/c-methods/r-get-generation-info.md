---
description: Restituisce 2 diversi tipi di informazioni in base ai parametri trasmessi. originatorHandle restituisce informazioni sulle risorse generate dalla risorsa specificata. generateHandle restituisce informazioni sui passaggi utilizzati per generare la risorsa o il file specificato.
solution: Experience Manager
title: getGenerationInfo
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: fa098e3c-8145-4238-a84c-c545f1c53341
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '198'
ht-degree: 7%

---

# getGenerationInfo{#getgenerationinfo}

Restituisce 2 diversi tipi di informazioni in base ai parametri trasmessi. originatorHandle restituisce informazioni sulle risorse generate dalla risorsa specificata. generateHandle restituisce informazioni sui passaggi utilizzati per generare la risorsa o il file specificato.

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
| Frase codice | `xsd:string` | Sì | La maniglia per l&#39;azienda. |
| Frase codice | `xsd:string` | No | Il motore utilizzato nella generazione. Consulta Stili font. |
| Frase codice | `xsd:string` | No | Handle della risorsa da interrogare per le risorse generate. |
| Frase codice | `xsd:string` | No | Handle della risorsa per la query delle risorse e dei motori utilizzati nella sua generazione. |
| Frase codice | `xsd:StringArray` | No | Proprietà incluse nell&#39;operazione. |
| Frase codice | `xsd:StringArray` | No | Proprietà escluse dall&#39;operazione. |

**Output (getGenerationInfoReturn)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| generationArray | `types:GenerationInfoArray` | Sì | Array di informazioni sulla generazione. |

## Esempi {#section-fdffe6ed82d94c7aa90e47f7ce889403}

In questo esempio di codice vengono restituite informazioni sulle risorse generate da una risorsa specifica. Non recupera informazioni sui passaggi utilizzati per generare la risorsa specificata. La risposta viene troncata per brevità.

**Richiesta**

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
