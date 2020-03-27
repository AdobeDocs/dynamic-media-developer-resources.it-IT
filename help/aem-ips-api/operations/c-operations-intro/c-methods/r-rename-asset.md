---
description: Rinomina una risorsa.
seo-description: Rinomina una risorsa.
seo-title: renameAsset
solution: Experience Manager
title: renameAsset
topic: Scene7 Image Production System API
uuid: f285d7e4-00df-4d90-a05a-71747a4c54cc
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# renameAsset{#renameasset}

Rinomina una risorsa.

>[!NOTE]
>
>Il `renameFiles` parametro è stato dichiarato obsoleto per le versioni precedenti e rimosso da `renameAsset`. Il percorso del file virtuale viene modificato per corrispondere al nuovo nome della risorsa (mantenendo l’estensione del file), mentre i percorsi dei file fisici non vengono modificati. I client API devono rimuovere i riferimenti a questo parametro quando si aggiorna alla nuova versione dell&#39;API.

## Tipi di utenti autorizzati {#section-cc27ad713c6d498b8f056850b20976f4}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImpagePortalContribUser`

>[!NOTE]
>
>L’utente deve disporre dell’accesso in lettura e scrittura alla risorsa.

## Parametri {#section-ef95a994106841e0ab346dd4cf672258}

**Input (renameAssetParam)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | Sì | L’handle della società alla quale la risorsa appartiene. |
| ` *`assetHandle`*` | `xsd:string` | Sì | L’handle della risorsa da rinominare. |
| ` *`newName`*` | `xsd:string` | Sì | Il nuovo nome della risorsa. |
| ` *`validateName`*` | `xsd:boolean` | Sì | Se `validateName` è `true` e il tipo di risorsa richiede un ID IPS univoco, il nuovo nome viene controllato per verificare l&#39;univocità globale e `renameAsset` genera un errore se non è univoco. |

**Output (renameAssetReturn)**

L&#39;API IPS non restituisce una risposta per questa operazione. Vedere la descrizione dell&#39; `<ns1:validateName>` elemento per le avvertenze su questo elemento.

## Esempi {#section-a0ddffd62bec42e09069f22ceb486f8a}

Questo esempio di codice rinomina una risorsa

**Request Contents (Richiesta contenuto)**

```java
<ns1:renameAssetParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:assetHandle>24265|1|17061</ns1:assetHandle>
   <ns1:newName>My Newly Renamed Image</ns1:newName>
   <ns1:validateName>true</ns1:validateName>
   <ns1:renameFiles>true</ns1:renameFiles>
</ns1:renameAssetParam>
```

**Risposta**

Nessuno.
