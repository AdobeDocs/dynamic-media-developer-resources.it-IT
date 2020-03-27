---
description: Crea un set di immagini.
seo-description: Crea un set di immagini.
seo-title: createImageSet
solution: Experience Manager
title: createImageSet
topic: Scene7 Image Production System API
uuid: 688f3954-bc8f-4687-8d66-e064561cd4a0
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

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
>L&#39;utente deve disporre dell&#39;accesso in lettura/scrittura alla cartella di destinazione.

## Parametri {#section-03d22ba7d290477e91c25ca1d4439200}

**Input (createImageSetParam)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | Sì | L’handle della società a cui appartiene il set di immagini. |
| ` *`folderHandle`*` | `xsd:string` | Sì | L’handle della cartella. |
| ` *`name`*` | `xsd:string` | Sì | Nome set di immagini. |
| ` *`type`*` | `xsd:string` | Sì | Tipo set di immagini. |
| ` *`thumbAssetHandle`*` | `xsd:string` | No | Gestione della risorsa che funge da miniatura per il nuovo set di immagini. Se non viene specificato, IPS tenta di utilizzare la prima risorsa immagine a cui fa riferimento il set. |

**Uscita**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| ` *`assetHandle`*` | `xsd:string` | Sì | La maniglia del nuovo set di immagini. |

## Esempi {#section-385fe3b0af8044b0a2451336ec137fc5}

Questo esempio di codice crea un set di immagini specificato da società, cartella, nome e tipo. La risposta è una maniglia della risorsa del set di immagini appena creato.

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

