---
description: Recupera tutte le proprietà del sistema in una singola richiesta.
seo-description: Recupera tutte le proprietà del sistema in una singola richiesta.
seo-title: getSystemProperties
solution: Experience Manager
title: getSystemProperties
topic: Scene7 Image Production System API
uuid: 08ea86ba-bde5-45a1-920a-04f784395e6a
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# getSystemProperties{#getsystemproperties}

Recupera tutte le proprietà del sistema in una singola richiesta.

Sintassi

## Tipi di utenti autorizzati {#section-fc311ce90a54400fa95b9dd36b756e23}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`
* `ImagePortalUser`
* `TrialSiteAdmin`
* `TrialSiteUser`

## Parametri {#section-b2a4fb7068424223aec87c50f0586d73}

**Input (getSystemPropertiesParam)**

Nessuno.

**Output (getSystemPropertiesReturn)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| ` *`propertyArray`*` | `types:PropertyArray` | Sì | Un array di proprietà del sistema. |

## Esempi {#section-728cc16fe9954b2daa035b4d4d4b4ce6}

Questo esempio di codice restituisce un array di proprietà del sistema. Risposta troncata per brevità.

**Request Contents (Richiesta contenuto)**

```java
<getSystemPropertiesParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-09-10"/>
```

**Risposta**

```java
<getSystemPropertiesReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-09-10"> 
   <propertyArray> 
      <items> 
         <name>SvgRenderEnabled</name> 
         <value>true</value> 
      </items> 
      <items> 
         <name>SwfRootUrl</name> 
         <value>/SWFs/</value> 
      </items> 
      ... 
   </propertyArray> 
</getSystemPropertiesReturn>
```

