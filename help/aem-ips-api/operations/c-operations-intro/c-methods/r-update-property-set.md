---
description: Utilizza una matrice di proprietà per aggiornare un set di proprietà.
solution: Experience Manager
title: updatePropertySet
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: bbe6a664-b6e1-4b46-867d-a134070b13da
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '85'
ht-degree: 8%

---

# updatePropertySet{#updatepropertyset}

Utilizza una matrice di proprietà per aggiornare un set di proprietà.

Sintassi

## Tipi di utenti autorizzati {#section-116693bbfb5d44219e62bbb1ba19de96}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parametri {#section-98361b063e9c41e8b2f744fabc0e13ed}

**Input (updatePropertySetParam)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| setHandle | `xsd:string` | Sì | Gestisci il set di proprietà. |
| replaceProperties | `xsd:string` | No | Impostare su `true` per sostituire le proprietà. |
| propertyArray | `types:PropertyArray` | Sì | Matrice di proprietà aggiornate per il set di proprietà. |

**Output (updatePropertySetReturn)**

L&#39;API IPS non restituisce una risposta per questa operazione.

## Esempi {#section-55d1c9dcd0174c6b9b52b4709f7c8bf9}

Questo esempio di codice aggiorna un set di proprietà con proprietà nella matrice di proprietà.

**Richiesta**

```java
<updatePropertySetParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <setHandle>ps|941</setHandle>
   <replaceProperties>true</replaceProperties>
   <propertyArray>
      <items>
         <name>application_project_whatever</name>
         <value>false</value>
      </items>
      <items>
         <name>application_server_prefix_published_test</name>
         <value>http://s7teton.macromedia.com:8080/is/image/</value>
      </items>
      <items>
         <name>application_server_prefix_origin_test</name>
         <value>http://s7teton:8080/is/image/</value>
      </items>
   </propertyArray>
</updatePropertySetParam>
```

**Risposta**

Nessuno.
