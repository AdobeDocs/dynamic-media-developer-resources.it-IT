---
description: Elimina una risorsa.
solution: Experience Manager
title: deleteAsset
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: dacea36e-3d40-4aaf-94fd-f0709830caf9
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '92'
ht-degree: 6%

---

# deleteAsset{#deleteasset}

Elimina una risorsa.

Sintassi

## Tipi di utenti autorizzati {#section-e913be43b684491daf02bc73211e4290}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

>[!NOTE]
>
>L’utente deve disporre dell’accesso in lettura ed eliminazione alla risorsa.

## Parametri {#section-0eed164e278b456fbdfb7a50727a0416}

**Input (deleteAssetParam)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| companyHandle | `xsd:string` | Sì | Handle dell&#39;azienda a cui appartiene la cartella. |
| assetHandle | `xsd:string` | Sì | Handle della risorsa da eliminare. |

**Output (deleteAssetParam)**

L&#39;API IPS non restituisce una risposta per questa operazione.

## Esempi {#section-d5657289f5234bb0a613dcf691507958}

Questo codice di esempio elimina qualsiasi tipo di risorsa da una società specifica. Richiede un handle di risorsa, che devi ottenere da un’altra operazione.

**Richiesta**

```java
<ns1:deleteAssetParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:assetHandle>24265|1|17061</ns1:assetHandle>
</ns1:deleteAssetParam>
```

**Risposta**

Nessuno.
