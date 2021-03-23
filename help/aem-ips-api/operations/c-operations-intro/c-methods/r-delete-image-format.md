---
description: Elimina un formato immagine. Ottenere la maniglia del formato immagine da saveImageFormat.
seo-description: Elimina un formato immagine. Ottenere la maniglia del formato immagine da saveImageFormat.
seo-title: deleteImageFormat
solution: Experience Manager
title: deleteImageFormat
uuid: 70dddde9-830b-4267-8ef5-df5241f549e3
feature: Dynamic Media Classic, SDK/API
role: Sviluppatore,Amministratore
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '121'
ht-degree: 8%

---


# deleteImageFormat{#deleteimageformat}

Elimina un formato immagine. Ottenere la maniglia del formato immagine da saveImageFormat.

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
| `*`companyHandle`*` | `xsd:string` | Sì | L&#39;handle della società che contiene il formato immagine da eliminare. |
| `*`imageFormatHandle`*` | `xsd:string` | Sì | Il punto di manipolazione del formato immagine che si desidera eliminare. |

**Output (deleteImageFormatParam)**

L&#39;API IPS non restituisce una risposta per questa operazione.

## Esempi {#section-9ed9baaba13549bfaad1bc9cd7ec7009}

Questo esempio di codice elimina un formato immagine da un&#39;azienda. Ottenere la maniglia del formato immagine da un&#39;altra operazione.

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
