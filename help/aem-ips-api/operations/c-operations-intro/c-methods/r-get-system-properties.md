---
description: Recupera tutte le proprietà del sistema in una singola richiesta.
seo-description: Recupera tutte le proprietà del sistema in una singola richiesta.
seo-title: getSystemProperties
solution: Experience Manager
title: getSystemProperties
uuid: 08ea86ba-bde5-45a1-920a-04f784395e6a
feature: Dynamic Media Classic, SDK/API
role: Sviluppatore,Amministratore
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '71'
ht-degree: 12%

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
| `*`propertyArray`*` | `types:PropertyArray` | Sì | Matrice di proprietà del sistema. |

## Esempi {#section-728cc16fe9954b2daa035b4d4d4b4ce6}

Questo esempio di codice restituisce un array delle proprietà del sistema. Risposta troncata per brevità.

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

