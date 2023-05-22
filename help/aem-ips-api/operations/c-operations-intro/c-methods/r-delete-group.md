---
description: Elimina un gruppo.
solution: Experience Manager
title: deleteGroup
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 0de188de-b4b6-4f48-9918-bcf962fa9482
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '86'
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
| companyHandle | `xsd:string` | Sì | Handle dell&#39;azienda appartenente al gruppo che si desidera eliminare. |
| groupHandle | `xsd:string` | Sì | Handle del gruppo che si desidera eliminare. |

**Output (deleteGroupParam)**

L&#39;API IPS non restituisce una risposta per questa operazione.

## Esempi {#section-8f8501af3b3348a1b5701cf9622bf6e4}

Questo codice di esempio elimina un gruppo da un’azienda. Richiede un handle di gruppo che è necessario ottenere da un&#39;altra operazione.

**Request Contents (Richiesta contenuto)**

```java
<ns1:deleteGroupParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:groupHandle>241</ns1:groupHandle>
</ns1:deleteGroupParam>
```

**Risposta**

Nessuno.
