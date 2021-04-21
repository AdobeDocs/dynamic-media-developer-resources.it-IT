---
description: Crea o modifica un gruppo.
solution: Experience Manager
title: saveGroup
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '99'
ht-degree: 17%

---


# saveGroup{#savegroup}

Crea o modifica un gruppo.

Sintassi

## Tipi di utenti autorizzati {#section-a6c1ce4c69f44ad0bcd41bbf3893bc45}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## Parametri {#section-743610e98dd5494baffcbad6401038eb}

**Input (saveGroupParam)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Sì | L&#39;handle della società con il gruppo che si desidera salvare. |
| `*`groupHandle`*` | `xsd:string` | No | L&#39;handle del gruppo. |
| `*`name`*` | `xsd:string` | Sì | Nome del gruppo. |
| `*`isSystemDefined`*` | `xsd:boolean` | Sì | `false` è il valore predefinito. |

**Output (saveGroupReturn)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| `*`groupHandle`*` | `xsd:string` | Sì | Maniglia di gruppo. |

## Esempi {#section-26eee227ff1f4edabb7fa1240b4d9999}

Questo esempio di codice crea un gruppo che appartiene a una società specifica. Se il gruppo esiste già, viene salvato con i valori dei parametri specificati.

**Request Contents (Richiesta contenuto)**

```java
<ns1:saveGroupParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:name>My Other Group</ns1:name>
   <ns1:isSystemDefined>false</ns1:isSystemDefined>
</ns1:saveGroupParam>
```

**Risposta**

```java
<saveGroupReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <groupHandle>281</groupHandle>
</saveGroupReturn>
```

