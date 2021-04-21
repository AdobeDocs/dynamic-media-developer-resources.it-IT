---
description: Rinomina una risorsa.
solution: Experience Manager
title: rinominaRisorsa
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Administrator
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '182'
ht-degree: 6%

---


# rinominareAsset{#renameasset}

Rinomina una risorsa.

>[!NOTE]
>
>Il parametro `renameFiles` è stato dichiarato obsoleto per le versioni precedenti e rimosso da `renameAsset`. Il percorso del file virtuale viene modificato in modo che corrisponda al nuovo nome della risorsa (mantenendo l’estensione del file), mentre i percorsi dei file fisici non vengono interessati. I client API devono rimuovere i riferimenti a questo parametro quando si aggiorna alla nuova versione API.

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

**Input (ridenominazioneAssetParam)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Sì | Il handle della società a cui appartiene il cespite. |
| `*`assetHandle`*` | `xsd:string` | Sì | Il handle della risorsa da rinominare. |
| `*`newName`*` | `xsd:string` | Sì | Nuovo nome della risorsa. |
| `*`validateName`*` | `xsd:boolean` | Sì | Se il `validateName` è `true` e il tipo di risorsa richiede un ID IPS univoco, il nuovo nome viene controllato per l’univocità globale e `renameAsset` genera un errore se non è univoco. |

**Output (rinominareAssetReturn)**

L&#39;API IPS non restituisce una risposta per questa operazione. Vedi la descrizione dell&#39;elemento `<ns1:validateName>` per le avvertenze su questo elemento.

## Esempi {#section-a0ddffd62bec42e09069f22ceb486f8a}

Questo codice di esempio rinomina una risorsa

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
