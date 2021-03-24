---
description: Crea un set di immagini.
solution: Experience Manager
title: createImageSet
feature: Dynamic Media Classic, SDK/API, Set di immagini
role: Sviluppatore,Amministratore
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '145'
ht-degree: 12%

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
>L’utente deve disporre dell’accesso in lettura/scrittura alla cartella di destinazione.

## Parametri {#section-03d22ba7d290477e91c25ca1d4439200}

**Input (createImageSetParam)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Sì | Il handle della società a cui appartiene il set di immagini. |
| `*`folderHandle`*` | `xsd:string` | Sì | L&#39;handle della cartella. |
| `*`name`*` | `xsd:string` | Sì | Nome del set di immagini. |
| `*`type`*` | `xsd:string` | Sì | Tipo di set di immagini. |
| `*`thumbAssetHandle`*` | `xsd:string` | No | Gestione della risorsa che funge da miniatura del nuovo set di immagini. Se non viene specificato, IPS cerca di utilizzare la prima risorsa immagine a cui fa riferimento il set. |

**Uscita**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| `*`assetHandle`*` | `xsd:string` | Sì | La maniglia del nuovo set di immagini. |

## Esempi {#section-385fe3b0af8044b0a2451336ec137fc5}

Questo esempio di codice crea un set di immagini specificato da società, cartella, nome e tipo. La risposta è un handle di risorsa del set di immagini appena creato.

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

