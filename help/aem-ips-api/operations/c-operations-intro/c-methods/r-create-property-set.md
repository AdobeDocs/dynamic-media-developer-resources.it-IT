---
description: I set di proprietà sono set di coppie nome-valore specifici dell’applicazione che possono essere associati a vari oggetti IPS, a seconda del tipo di set di proprietà. Se il tipo di set di proprietà non consente l'associazione di più set a un oggetto (PropertySetType/allowMultipleisfalse) e l'oggetto dispone già di un set associato dello stesso tipo, il nuovo set sostituirà quello esistente.
solution: Experience Manager
title: createPropertySet
feature: Dynamic Media Classic, SDK/API
role: Sviluppatore,Amministratore
exl-id: e9f85e65-4a2f-4b82-b7b8-d0d60b8345cd
translation-type: tm+mt
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '222'
ht-degree: 7%

---

# createPropertySet{#createpropertyset}

I set di proprietà sono set di coppie nome-valore specifici dell’applicazione che possono essere associati a vari oggetti IPS, a seconda del tipo di set di proprietà. Se il tipo di set di proprietà non consente l&#39;associazione di più set a un oggetto (PropertySetType/allowMultipleisfalse) e l&#39;oggetto dispone già di un set associato dello stesso tipo, il nuovo set sostituirà quello esistente.

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
| `*`typeHandle`*` | `xsd:string` | Sì | L&#39;handle del tipo di set di proprietà. |
| `*`primaryOwnerHandle`*` | `xsd:string` | Sì | L&#39;handle al proprietario principale dell&#39;insieme di proprietà. |
| `*`secondarioOwnerHandle`*` | `xsd:string` | No | L&#39;handle al proprietario secondario dell&#39;insieme di proprietà. |
| `*`propertyArray`*` | `types:PropertyArray` | Sì | Matrice di proprietà. |
| `*`permissionArray`*` | `types:PermissionUpdateArray` |  |  |

**Output (createPropertySetParam)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| `*`setHandle`*` | `xsd:string` | Sì | L&#39;handle del nuovo set di proprietà. |

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
