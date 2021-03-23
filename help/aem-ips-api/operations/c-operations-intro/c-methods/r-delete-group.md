---
description: Elimina un gruppo.
seo-description: Elimina un gruppo.
seo-title: deleteGroup
solution: Experience Manager
title: deleteGroup
uuid: 04934b16-b7ef-4657-9f63-c91fcc741ca4
feature: Dynamic Media Classic, SDK/API
role: Sviluppatore,Amministratore
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '97'
ht-degree: 10%

---


# deleteGroup{#deletegroup}

Elimina un gruppo.

Sintassi

## Tipi di utenti autorizzati {#section-ebcc67723663494db0562275b1873460}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## Parametri {#section-42775102ec724c36ae5241eea1a00b8e}

**Input (deleteGroupParam)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Sì | L&#39;handle della società che appartiene al gruppo che si desidera eliminare. |
| `*`groupHandle`*` | `xsd:string` | Sì | L&#39;handle del gruppo da eliminare. |

**Output (deleteGroupParam)**

L&#39;API IPS non restituisce una risposta per questa operazione.

## Esempi {#section-8f8501af3b3348a1b5701cf9622bf6e4}

Questo codice di esempio elimina un gruppo da una società. Richiede un handle di gruppo, che è necessario ottenere da un&#39;altra operazione.

**Request Contents (Richiesta contenuto)**

```java
<ns1:deleteGroupParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:groupHandle>241</ns1:groupHandle>
</ns1:deleteGroupParam>
```

**Risposta**

Nessuno.
