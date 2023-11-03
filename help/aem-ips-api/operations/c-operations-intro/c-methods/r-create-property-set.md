---
description: Gli insiemi di proprietà sono insiemi di coppie nome-valore specifiche dell'applicazione che possono essere associate a vari oggetti IPS, a seconda del tipo di insieme di proprietà. Se il tipo di set di proprietà non consente di associare più set a un oggetto (PropertySetType/allowMultipleisfalse) e all'oggetto è già associato un set dello stesso tipo, il nuovo set sostituisce quello esistente.
solution: Experience Manager
title: createPropertySet
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: e9f85e65-4a2f-4b82-b7b8-d0d60b8345cd
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '213'
ht-degree: 7%

---

# createPropertySet{#createpropertyset}

Gli insiemi di proprietà sono insiemi di coppie nome-valore specifiche dell&#39;applicazione che possono essere associate a vari oggetti IPS, a seconda del tipo di insieme di proprietà. Se il tipo di set di proprietà non consente di associare più set a un oggetto (PropertySetType/allowMultipleisfalse) e all&#39;oggetto è già associato un set dello stesso tipo, il nuovo set sostituisce quello esistente.

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
| typeHandle | `xsd:string` | Sì | Handle del tipo di set di proprietà. |
| primaryOwnerHandle | `xsd:string` | Sì | Handle per il proprietario primario del set di proprietà. |
| secondaryOwnerHandle | `xsd:string` | No | Handle per il proprietario secondario del set di proprietà. |
| propertyArray | `types:PropertyArray` | Sì | Array di proprietà. |
| permissionArray | `types:PermissionUpdateArray` |  |  |

**Output (createPropertySetParam)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| setHandle | `xsd:string` | Sì | Handle del nuovo set di proprietà. |

## Esempi {#section-4e1f5b2883664bc88f590fcd253df22b}

In questo esempio di codice viene creato un set di proprietà contenente nomi e valori di proprietà. La risposta restituisce un handle per il nuovo set di proprietà.

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
