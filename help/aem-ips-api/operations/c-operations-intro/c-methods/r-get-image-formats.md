---
description: Restituisce i formati immagine, ad esempio PDF, EPS, SWF e altri.
solution: Experience Manager
title: getImageFormats
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '81'
ht-degree: 16%

---


# getImageFormats{#getimageformats}

Restituisce i formati immagine, ad esempio PDF, EPS, SWF e altri.

Sintassi

## Tipi di utenti autorizzati {#section-6a386ad8641b4aa1a281600fc94fd3f6}

* `IpsUser`
* `IspAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parametri {#section-eefa36a70b74498f8727ef61d98cfb63}

**Input (getImageFormatsParam)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Sì | L&#39;handle dell&#39;azienda con i formati immagine che si desidera ottenere. |

**Output (getImageFormatsParam)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| `*`imageFormatArray`*` | `types:ImageFormatArray` | Sì | Matrice di formato immagine. |

## Esempi {#section-73881e12839b4904bf3299b0920bdd0c}

Questo esempio di codice restituisce tutti i formati immagine per la società specificata.

**Request Contents (Richiesta contenuto)**

```java
<ns1:getImageFormatsParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
</ns1:getImageFormatsParam>
```

**Risposta**

```java
<getImageFormatsReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <imageFormatArray></imageFormatArray>
</getImageFormatsReturn>
```

