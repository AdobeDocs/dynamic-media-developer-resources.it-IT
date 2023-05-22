---
description: Rinomina una risorsa.
solution: Experience Manager
title: renameAsset
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: f3fff3c1-1b48-4d86-8a81-f75be00fc329
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '173'
ht-degree: 6%

---

# renameAsset{#renameasset}

Rinomina una risorsa.

>[!NOTE]
>
>Il `renameFiles` Il parametro è stato dichiarato obsoleto per le versioni precedenti e rimosso da `renameAsset`. Il percorso del file virtuale viene modificato in modo da corrispondere al nuovo nome della risorsa (mantenendo l’estensione del file), mentre i percorsi dei file fisici non vengono interessati. I client API devono rimuovere i riferimenti a questo parametro durante l’aggiornamento alla nuova versione API.

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
| companyHandle | `xsd:string` | Sì | Handle dell&#39;azienda a cui appartiene il bene. |
| assetHandle | `xsd:string` | Sì | Handle della risorsa da rinominare. |
| newName | `xsd:string` | Sì | Nuovo nome della risorsa. |
| validateName | `xsd:boolean` | Sì | Se il `validateName` è `true` e il tipo di risorsa richiede un ID IPS univoco, quindi viene verificato se il nuovo nome è univoco a livello globale e `renameAsset` genera un errore se non è univoco. |

**Output (renameAssetReturn)**

L&#39;API IPS non restituisce una risposta per questa operazione. Vedi la descrizione della `<ns1:validateName>` per avvertenze su questo elemento.

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
