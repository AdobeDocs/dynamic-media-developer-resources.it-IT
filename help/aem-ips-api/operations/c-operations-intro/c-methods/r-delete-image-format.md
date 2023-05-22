---
description: Elimina un formato immagine. Ottieni l'handle del formato immagine da saveImageFormat.
solution: Experience Manager
title: deleteImageFormat
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: bd717c08-6da4-47f1-8614-e4ba79d8176c
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '102'
ht-degree: 8%

---

# deleteImageFormat{#deleteimageformat}

Elimina un formato immagine. Ottieni l&#39;handle del formato immagine da saveImageFormat.

Sintassi

## Tipi di utenti autorizzati {#section-827e24a3019543418b0a635d46c1edfd}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## Parametri {#section-462c05d9aad746ee8d2be0656041b693}

**Input (deleteImageFormatParam)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| companyHandle | `xsd:string` | Sì | Handle dell&#39;azienda contenente il formato immagine da eliminare. |
| imageFormatHandle | `xsd:string` | Sì | Handle del formato immagine da eliminare. |

**Output (deleteImageFormatParam)**

L&#39;API IPS non restituisce una risposta per questa operazione.

## Esempi {#section-9ed9baaba13549bfaad1bc9cd7ec7009}

Questo esempio di codice elimina un formato immagine da un’azienda. Ottieni la maniglia del formato immagine da un’altra operazione.

**Request Contents (Richiesta contenuto)**

```java
<deleteImageFormatParam xmlns="http://www.scene7.com/IpsApi/xsd">
   <companyHandle>47</companyHandle>
   <imageFormatHandle>47|301</imageFormatHandle>
</deleteImageFormatParam>
```

**Risposta**

Nessuno.

**Argomento correlato:**

[saveImageFormat](../../../operations/c-operations-intro/c-methods/r-save-image-format.md#reference-d15c27f533ef41e38b54a539a304bd1d)
