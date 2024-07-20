---
description: Imposta i valori dei metadati per una risorsa. Funziona con un array di aggiornamenti dei metadati per impostare i valori in un batch.
solution: Experience Manager
title: setAssetMetadata
feature: Dynamic Media Classic,SDK/API,Metadata,Asset Management
role: Developer,Admin
exl-id: 811e44e1-774a-49bd-a2bd-a7504e5f7f5f
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '123'
ht-degree: 5%

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
>L’utente deve avere accesso in lettura alla risorsa.

## Parametri {#section-bcdcff30905e444388811e897b2824bd}

**Input (setAssetMetadataParam)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| companyHandle | `xsd:string` | Sì | Handle dell’azienda con la risorsa da aggiornare. |
| assetHandle | `xsd:string` | Sì | Handle della risorsa. |
| updateArray | `types:MetadataUpdateArray` | Sì | Aggiornamenti in un array di aggiornamento dei metadati. |

**Output (setAssetMetadataReturn)**

L&#39;API IPS non restituisce una risposta per questa operazione.

## Esempi {#section-1ab412e7ee1d4d6d8469b0b403598c42}

In questo esempio di codice viene utilizzata una matrice di aggiornamenti dei metadati per impostare i metadati della risorsa specificata.

**Richiesta**

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
