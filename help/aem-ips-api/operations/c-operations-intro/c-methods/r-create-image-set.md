---
description: Crea un set di immagini.
solution: Experience Manager
title: createImageSet
feature: Dynamic Media Classic,SDK/API,Image Sets
role: Developer,Admin
exl-id: 01ccc705-97e4-4e75-a322-e24bb78cb496
TQID: 'https://experienceleague.adobe.com/os4DfkGa5cTZfMN1vc5HeA8Qvauvwb5Q0dZ2P3HFI-c'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 136
ht-degree: 10%

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

**Richiesta**

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
