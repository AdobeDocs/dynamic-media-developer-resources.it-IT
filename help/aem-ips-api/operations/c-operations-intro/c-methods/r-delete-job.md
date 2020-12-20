---
description: Elimina un processo corrente o pianificato.
seo-description: Elimina un processo corrente o pianificato.
seo-title: deleteJob
solution: Experience Manager
title: deleteJob
topic: Scene7 Image Production System API
uuid: c1109cae-a3ca-40db-b641-9a6fc116c964
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '97'
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
| ` *`companyHandle`*` | `xsd:string` | Sì | L&#39;handle della società alla quale il processo appartiene. |
| ` *`jobHandle`*` | `xsd:string` | Sì | L’handle del processo da eliminare. |

**Uscita**

L&#39;API IPS non restituisce una risposta per questa operazione.

## Esempi {#section-732d21d4dad04337b7a5ae1a0cc00eba}

Questo esempio di codice elimina un processo in esecuzione o pianificato per l&#39;esecuzione in IPS. Richiede un handle di processo, che è necessario ottenere da un&#39;altra operazione.

**Request Contents (Richiesta contenuto)**

```java
<deleteJobParam xmlns="http://www.scene7.com/IpsApi/xsd">
   <companyHandle>47</companyHandle>
   <jobHandle>47|My Test Job|</jobHandle>
</deleteJobParam>
```

**Risposta**

Nessuno.
