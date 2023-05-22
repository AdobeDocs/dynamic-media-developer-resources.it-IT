---
description: Crea un set di immagini.
solution: Experience Manager
title: createImageSet
feature: Dynamic Media Classic,SDK/API,Image Sets
role: Developer,Admin
exl-id: 01ccc705-97e4-4e75-a322-e24bb78cb496
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '136'
ht-degree: 11%

---

# createImageSet{#createimageset}

Crea un set di immagini.

Sintassi

## Tipi di utenti autorizzati {#section-58bf5027e6d24ab5a9fcba59776d15dc}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

>[!NOTE]
>
>L&#39;utente deve avere accesso in lettura/scrittura alla cartella di destinazione.

## Parametri {#section-03d22ba7d290477e91c25ca1d4439200}

**Input (createImageSetParam)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| companyHandle | `xsd:string` | Sì | Handle dell&#39;azienda a cui appartiene il set di immagini. |
| folderHandle | `xsd:string` | Sì | Handle della cartella. |
| nome | `xsd:string` | Sì | Nome set di immagini. |
| tipo | `xsd:string` | Sì | Tipo di set di immagini. |
| thumbAssetHandle | `xsd:string` | No | Handle della risorsa che funge da miniatura per il nuovo set di immagini. Se non viene specificato diversamente, IPS tenta di utilizzare la prima risorsa immagine a cui fa riferimento il set. |

**Output**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| assetHandle | `xsd:string` | Sì | Handle del nuovo set di immagini. |

## Esempi {#section-385fe3b0af8044b0a2451336ec137fc5}

In questo esempio di codice viene creato un set di immagini specificato per società, cartella, nome e tipo. La risposta è un handle di risorsa del set di immagini appena creato.

**Request Contents (Richiesta contenuto)**

```java
<ns1:createImageSetParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:folderHandle>MyCompany/eCatalogs/</ns1:folderHandle>
   <ns1:name>My Image Set</ns1:name>
   <ns1:type>ImageSet</ns1:type>
</ns1:createImageSetParam>
```

**Risposta**

```java
<createImageSetReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <assetHandle>25741|22|841</assetHandle>
</createImageSetReturn>
```
