---
description: Restituisce i formati immagine, ad esempio PDF, EPS, SWF e altri.
solution: Experience Manager
title: getImageFormats
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: c2fa4cdd-fb4f-4e6a-8197-8f64c986c3a0
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '74'
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
| companyHandle | `xsd:string` | Sì | Handle per l&#39;azienda con i formati immagine che si desidera ottenere. |

**Output (getImageFormatsParam)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| imageFormatArray | `types:ImageFormatArray` | Sì | Matrice di formato immagine. |

## Esempi {#section-73881e12839b4904bf3299b0920bdd0c}

In questo esempio di codice vengono restituiti tutti i formati immagine per l&#39;azienda specificata.

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
