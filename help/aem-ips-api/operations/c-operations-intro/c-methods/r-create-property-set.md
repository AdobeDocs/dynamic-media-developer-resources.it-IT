---
description: I set di proprietà sono set di coppie nome-valore specifici dell'applicazione che possono essere associati a vari oggetti IPS, a seconda del tipo di set di proprietà. Se il tipo di set di proprietà non consente l'associazione di più set a un oggetto (PropertySetType/allowMultipleisfalse) e all'oggetto è già associato un set dello stesso tipo, il nuovo set sostituirà quello esistente.
seo-description: I set di proprietà sono set di coppie nome-valore specifici dell'applicazione che possono essere associati a vari oggetti IPS, a seconda del tipo di set di proprietà. Se il tipo di set di proprietà non consente l'associazione di più set a un oggetto (PropertySetType/allowMultipleisfalse) e all'oggetto è già associato un set dello stesso tipo, il nuovo set sostituirà quello esistente.
seo-title: createPropertySet
solution: Experience Manager
title: createPropertySet
topic: Scene7 Image Production System API
uuid: f0b5b951-143f-4a31-bb6b-cdeabdebbcbb
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# createPropertySet{#createpropertyset}

I set di proprietà sono set di coppie nome-valore specifici dell&#39;applicazione che possono essere associati a vari oggetti IPS, a seconda del tipo di set di proprietà. Se il tipo di set di proprietà non consente l&#39;associazione di più set a un oggetto (PropertySetType/allowMultipleisfalse) e all&#39;oggetto è già associato un set dello stesso tipo, il nuovo set sostituirà quello esistente.

Sintassi

## Tipi di utenti autorizzati {#section-f9b6187ba636475787c997fc27bb192a}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## Parametri {#section-25258e75f5f3419bad165c797eb6cd8e}

**Input (createPropertySetParam)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| ` *`typeHandle`*` | `xsd:string` | Sì | L&#39;handle del tipo di set di proprietà. |
| ` *`mainOwnerHandle`*` | `xsd:string` | Sì | L&#39;handle al proprietario principale dell&#39;insieme di proprietà. |
| ` *`secondariaOwnerHandle`*` | `xsd:string` | No | L&#39;handle del proprietario secondario dell&#39;insieme di proprietà. |
| ` *`propertyArray`*` | `types:PropertyArray` | Sì | L&#39;array di proprietà. |
| ` *`permissionsArray`*` | `types:PermissionUpdateArray` |  |  |

**Output (createPropertySetParam)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| ` *`setHandle`*` | `xsd:string` | Sì | L&#39;handle del nuovo set di proprietà. |

## Esempi {#section-4e1f5b2883664bc88f590fcd253df22b}

Questo esempio di codice crea un set di proprietà contenente nomi e valori di proprietà. La risposta restituisce un handle al nuovo set di proprietà.

**Request Contents (Richiesta contenuto)**

```java
<createPropertySetParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <typeHandle>pt|10801</typeHandle>
   <primaryOwnerHandle>u|41|strangio@adobe.com</primaryOwnerHandle>
   <propertyArray>
      <items>
         <name>application_project_whatever</name>
         <value>true</value>
      </items>
      <items>
         <name>application_server_prefix_published_test</name>
         <value>http://s7everest.macromedia.com:8080/is/image/</value>
      </items>
      <items>
         <name>application_server_prefix_origin_test</name>
         <value>http://s7everest:8080/is/image/</value>
      </items>
   </propertyArray>
</createPropertySetParam>
```

**Risposta**

```java
<createPropertySetReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <setHandle>ps|941</setHandle>
</createPropertySetReturn>
```

