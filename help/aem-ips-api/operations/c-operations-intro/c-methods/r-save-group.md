---
description: Creare o modificare un gruppo.
solution: Experience Manager
title: saveGroup
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 1dd980e7-eb38-4c90-b4fc-83327d4a95f5
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '92'
ht-degree: 16%

---

# saveGroup{#savegroup}

Creare o modificare un gruppo.

Sintassi

## Tipi di utenti autorizzati {#section-a6c1ce4c69f44ad0bcd41bbf3893bc45}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## Parametri {#section-743610e98dd5494baffcbad6401038eb}

**Input (saveGroupParam)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| companyHandle | `xsd:string` | Sì | Handle per l&#39;azienda con il gruppo che si desidera salvare. |
| groupHandle | `xsd:string` | No | Handle del gruppo. |
| nome | `xsd:string` | Sì | Nome del gruppo. |
| isSystemDefined | `xsd:boolean` | Sì | `false` è l&#39;impostazione predefinita. |

**Output (saveGroupReturn)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| groupHandle | `xsd:string` | Sì | Handle di gruppo. |

## Esempi {#section-26eee227ff1f4edabb7fa1240b4d9999}

In questo esempio di codice viene creato un gruppo che appartiene a un&#39;azienda specifica. Se il gruppo esiste già, viene salvato con i valori dei parametri specificati.

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
