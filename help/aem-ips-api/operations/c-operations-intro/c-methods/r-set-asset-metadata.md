---
description: Imposta i valori dei metadati per una risorsa. Funziona con un array di aggiornamenti dei metadati per impostare i valori in un batch.
solution: Experience Manager
title: setAssetMetadata
feature: Dynamic Media Classic, SDK/API, metadati, gestione delle risorse
role: Developer,Administrator
exl-id: 811e44e1-774a-49bd-a2bd-a7504e5f7f5f
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '131'
ht-degree: 8%

---

# setAssetMetadata{#setassetmetadata}

Imposta i valori dei metadati per una risorsa. Funziona con un array di aggiornamenti dei metadati per impostare i valori in un batch.

Sintassi

## Tipi di utenti autorizzati {#section-9dcacb0c924044648f8324bfed183dca}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

>[!NOTE]
>
>L’utente deve disporre dell’accesso in lettura alla risorsa.

## Parametri {#section-bcdcff30905e444388811e897b2824bd}

**Input (setAssetMetadataParam)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Sì | L’handle della società con la risorsa da aggiornare. |
| `*`assetHandle`*` | `xsd:string` | Sì | L’handle della risorsa. |
| `*`updateArray`*` | `types:MetadataUpdateArray` | Sì | Aggiornamenti in un array di aggiornamento metadati. |

**Output (setAssetMetadataReturn)**

L&#39;API IPS non restituisce una risposta per questa operazione.

## Esempi {#section-1ab412e7ee1d4d6d8469b0b403598c42}

Questo esempio di codice utilizza una serie di aggiornamenti di metadati per impostare i metadati della risorsa specificata.

**Request Contents (Richiesta contenuto)**

```java
<ns1:setAssetMetadataParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:assetHandle>24265|1|17061</ns1:assetHandle>
   <ns1:updateArray>
      <ns1:items>
         <ns1:fieldHandle>47|ALL|Resolution</ns1:fieldHandle>
         <ns1:value>320</ns1:value>
      </ns1:items>
   </ns1:updateArray>
</ns1:setAssetMetadataParam>
```

**Risposta**

Nessuno.
