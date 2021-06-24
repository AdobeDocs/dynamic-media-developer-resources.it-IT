---
description: Ottiene i set di proprietà associati a un handle di tipo.
solution: Experience Manager
title: getPropertySets
feature: Dynamic Media Classic, SDK/API
role: Developer,Administrator
exl-id: da6923c3-9b86-4595-8205-645fb10e03b0
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '95'
ht-degree: 15%

---

# getPropertySets{#getpropertysets}

Ottiene i set di proprietà associati a un handle di tipo.

Sintassi

## Tipi di utenti autorizzati {#section-da858360b72941bfa8d9558b4da7d4da}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parametri {#section-d8da2847e77e4a95a4441d9848cac775}

**Input (getPropertySetsParam)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| `*`typeHandle`*` | `xsd:string` | Sì | L&#39;handle del tipo di set di proprietà. |
| `*`primaryOwnerHandle`*` | `xsd:string` | Sì | Proprietario principale dei dati associati all&#39;oggetto di database. |
| `*`secondarioOwnerHandle`*` | `xsd:string` | No | Proprietario secondario facoltativo dei dati. |

**Output (getPropertySetsReturn)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| `*`setArray`*` | `types:PropertySetArray` | Sì | Serie di set di proprietà. |

## Esempi {#section-1358af974eab4259864910337a6f0bd2}

Questo esempio di codice restituisce i set di proprietà del proprietario principale, specificati da un handle di tipo.

**Request Contents (Richiesta contenuto)**

```java
<getPropertySetsParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <typeHandle>pt|10801</typeHandle>
   <primaryOwnerHandle>u|41|strangio@adobe.com</primaryOwnerHandle>
</getPropertySetsParam>
```

**Risposta**

```java
<getPropertySetsReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <setArray>
      <items>
         <setHandle>ps|941</setHandle>
         <typeHandle>pt|10801</typeHandle>
         <propertyArray>
            <items>
               <name>application_server_prefix_published_test</name>
               <value>http://s7teton.macromedia.com:8080/is/image/</value>
            </items>
            <items>
               <name>application_project_whatever</name>
               <value>false</value>
            </items>
            <items>
               <name>application_server_prefix_origin_test</name>
               <value>http://s7teton:8080/is/image</value>
            </items>
         </propertyArray>
      </items>
   </setArray>
</getPropertySetsReturn>
```
