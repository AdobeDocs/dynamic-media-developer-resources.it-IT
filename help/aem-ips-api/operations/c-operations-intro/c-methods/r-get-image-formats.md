---
description: Restituisce i formati immagine, ad esempio PDF, EPS, SWF e altri.
seo-description: Restituisce i formati immagine, ad esempio PDF, EPS, SWF e altri.
seo-title: getImageFormats
solution: Experience Manager
title: getImageFormats
topic: Scene7 Image Production System API
uuid: 0adf989d-9c72-4337-99c0-de6931943e78
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

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
| ` *`companyHandle`*` | `xsd:string` | Sì | L’handle della società con i formati immagine che si desidera ottenere. |

**Output (getImageFormatsParam)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| ` *`imageFormatArray`*` | `types:ImageFormatArray` | Sì | L’array del formato immagine. |

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

