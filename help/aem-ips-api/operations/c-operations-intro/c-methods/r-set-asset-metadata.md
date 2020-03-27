---
description: Imposta i valori di metadati per una risorsa. Funziona con una serie di aggiornamenti di metadati per impostare i valori in un batch.
seo-description: Imposta i valori di metadati per una risorsa. Funziona con una serie di aggiornamenti di metadati per impostare i valori in un batch.
seo-title: setAssetMetadata
solution: Experience Manager
title: setAssetMetadata
topic: Scene7 Image Production System API
uuid: 17fe8277-a164-4f91-af96-ea43d41bd4f2
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# setAssetMetadata{#setassetmetadata}

Imposta i valori di metadati per una risorsa. Funziona con una serie di aggiornamenti di metadati per impostare i valori in un batch.

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
| ` *`companyHandle`*` | `xsd:string` | Sì | L’handle della società con la risorsa da aggiornare. |
| ` *`assetHandle`*` | `xsd:string` | Sì | La maniglia della risorsa. |
| ` *`updateArray`*` | `types:MetadataUpdateArray` | Sì | Aggiornamenti in un array di aggiornamenti di metadati. |

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
