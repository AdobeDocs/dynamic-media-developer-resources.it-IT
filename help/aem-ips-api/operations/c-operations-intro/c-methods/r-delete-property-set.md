---
description: Elimina un set di proprietà e tutte le proprietà associate.
seo-description: Elimina un set di proprietà e tutte le proprietà associate.
seo-title: deletePropertySet
solution: Experience Manager
title: deletePropertySet
uuid: b4fdf51f-89ec-4a69-9179-078ee8e1937f
feature: Dynamic Media Classic, SDK/API
role: Sviluppatore,Amministratore
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '99'
ht-degree: 9%

---


# deletePropertySet{#deletepropertyset}

Elimina un set di proprietà e tutte le proprietà associate.

Sintassi

## Tipi di utenti autorizzati {#section-b54aa8c854de400a989b4957412ff42c}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## Parametri {#section-e5fc868f69494cf6858e03027db09101}

**Input (deletePropertySetParam)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| `*`setHandle`*` | `xsd:string` | Sì | L&#39;handle della proprietà impostata per l&#39;eliminazione. |

**Output (deletePropertySetParam)**

L&#39;API IPS non restituisce una risposta per questa operazione.

## Esempi {#section-cf319fc8f86a40ab9cbd838b031973fe}

Questo esempio di codice utilizza l&#39;handle del set come campo nel `deletePropertySetParam` inviato al server dei servizi Web IPS per eliminare il set di proprietà.

**Request Contents (Richiesta contenuto)**

```java
<deletePropertySetParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <setHandle>ps|941</setHandle>
</deletePropertySetParam>
```

**Risposta**

Nessuno.
