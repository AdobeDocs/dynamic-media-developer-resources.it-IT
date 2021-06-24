---
description: Elimina un processo corrente o pianificato.
solution: Experience Manager
title: deleteJob
feature: Dynamic Media Classic, SDK/API
role: Developer,Administrator
exl-id: d38dd1e2-668e-4956-b854-54bf466d6d45
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '95'
ht-degree: 10%

---

# deleteJob{#deletejob}

Elimina un processo corrente o pianificato.

Sintassi

## Tipi di utenti autorizzati {#section-1b959679dc8147c291126ddf7e061742}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parametri {#section-000c42bc93744b1a8e777f3ec3c272b0}

**Input (deleteJobParam)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Sì | L&#39;handle dell&#39;azienda a cui appartiene il lavoro. |
| `*`jobHandle`*` | `xsd:string` | Sì | L&#39;handle del processo da eliminare. |

**Uscita**

L&#39;API IPS non restituisce una risposta per questa operazione.

## Esempi {#section-732d21d4dad04337b7a5ae1a0cc00eba}

Questo esempio di codice elimina un processo in esecuzione o pianificato per l&#39;esecuzione in IPS. Richiede un handle di lavoro, che è necessario ottenere da un&#39;altra operazione.

**Request Contents (Richiesta contenuto)**

```java
<deleteJobParam xmlns="http://www.scene7.com/IpsApi/xsd">
   <companyHandle>47</companyHandle>
   <jobHandle>47|My Test Job|</jobHandle>
</deleteJobParam>
```

**Risposta**

Nessuno.
