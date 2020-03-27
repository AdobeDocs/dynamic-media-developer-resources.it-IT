---
description: Ottiene progetti per un gruppo di risorse correlate.
seo-description: Ottiene progetti per un gruppo di risorse correlate.
seo-title: getProjects
solution: Experience Manager
title: getProjects
topic: Scene7 Image Production System API
uuid: 46ec9a5d-4414-4c9c-aaf2-0db654204b61
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# getProjects{#getprojects}

Ottiene progetti per un gruppo di risorse correlate.

Sintassi

## Tipi di utenti autorizzati {#section-337649866b1f4098844d1974ed7ab5d0}

* `IpsUser`
* `IpsAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parametri {#section-8d549237b8c440b4872a0a086ddc00a1}

**Input (getProjectsParam)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | Sì | L&#39;handle della società. |

**Output (getProjectsReturn)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| ` *`projectArray`*` | `types:ProjectArray` | Sì | Array di progetti associati alla società. |

## Esempi {#section-8b12d0b948f644f68bf9a16060d3849a}

Questo esempio di codice restituisce tutti gli handle di progetto in un array di progetto.

**Request Contents (Richiesta contenuto)**

```java
<ns1:getProjectsParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
</ns1:getProjectsParam>
```

**Risposta**

```java
<getProjectsReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <projectArray>
      <items>
         <projectHandle>47|My Project 1</projectHandle>
         <name>My Project 1</name>
      </items>
      <items>
         <projectHandle>47|My Project 2</projectHandle>
         <name>My Project 2</name>
      </items>
   </projectArray>
</getProjectsReturn>
```

