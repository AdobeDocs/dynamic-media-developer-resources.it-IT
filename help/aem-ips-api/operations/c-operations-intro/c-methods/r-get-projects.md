---
description: Ottiene i progetti per un gruppo di risorse correlate.
solution: Experience Manager
title: getProjects
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '73'
ht-degree: 17%

---


# getProjects{#getprojects}

Ottiene i progetti per un gruppo di risorse correlate.

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
| `*`companyHandle`*` | `xsd:string` | Sì | Il manico per l&#39;azienda. |

**Output (getProjectsReturn)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| `*`projectArray`*` | `types:ProjectArray` | Sì | L&#39;array di progetti associati all&#39;azienda. |

## Esempi {#section-8b12d0b948f644f68bf9a16060d3849a}

Questo esempio di codice restituisce tutti gli handle di progetto in una matrice di progetto.

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

