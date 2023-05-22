---
description: Ottiene gli insiemi di proprietà associati a un handle di tipo.
solution: Experience Manager
title: getPropertySets
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: da6923c3-9b86-4595-8205-645fb10e03b0
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '90'
ht-degree: 15%

---

# getPropertySets{#getpropertysets}

Ottiene gli insiemi di proprietà associati a un handle di tipo.

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
| typeHandle | `xsd:string` | Sì | Handle del tipo di set di proprietà. |
| primaryOwnerHandle | `xsd:string` | Sì | Proprietario principale dei dati associati all&#39;oggetto di database. |
| secondaryOwnerHandle | `xsd:string` | No | Proprietario secondario facoltativo dei dati. |

**Output (getPropertySetsReturn)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| setArray | `types:PropertySetArray` | Sì | Serie di insiemi di proprietà. |

## Esempi {#section-1358af974eab4259864910337a6f0bd2}

In questo esempio di codice vengono restituiti set di proprietà del proprietario primario, specificati da un handle di tipo.

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
