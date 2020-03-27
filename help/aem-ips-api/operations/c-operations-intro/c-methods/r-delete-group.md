---
description: Elimina un gruppo.
seo-description: Elimina un gruppo.
seo-title: deleteGroup
solution: Experience Manager
title: deleteGroup
topic: Scene7 Image Production System API
uuid: 04934b16-b7ef-4657-9f63-c91fcc741ca4
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

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
| ` *`companyHandle`*` | `xsd:string` | Sì | L’handle della società che appartiene al gruppo da eliminare. |
| ` *`groupHandle`*` | `xsd:string` | Sì | L’handle del gruppo da eliminare. |

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
