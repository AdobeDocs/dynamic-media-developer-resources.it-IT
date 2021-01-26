---
description: Utilizza una matrice di proprietà per aggiornare un set di proprietà.
seo-description: Utilizza una matrice di proprietà per aggiornare un set di proprietà.
seo-title: updatePropertySet
solution: Experience Manager
title: updatePropertySet
topic: Dynamic Media Image Production System API
uuid: 21a59c5a-7799-4af6-ab9f-b0311f5f7254
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '95'
ht-degree: 11%

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
| `*`setHandle`*` | `xsd:string` | Sì | Gestire l&#39;insieme di proprietà. |
| `*`replaceProperties`*` | `xsd:string` | No | Impostare su `true` per sostituire le proprietà. |
| `*`propertyArray`*` | `types:PropertyArray` | Sì | Array di proprietà aggiornate per l&#39;insieme di proprietà. |

**Output (updatePropertySetReturn)**

L&#39;API IPS non restituisce una risposta per questa operazione.

## Esempi {#section-55d1c9dcd0174c6b9b52b4709f7c8bf9}

Questo esempio di codice aggiorna un set di proprietà con proprietà nell&#39;array delle proprietà.

**Request Contents (Richiesta contenuto)**

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
