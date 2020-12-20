---
description: Assegnare o aggiornare le risorse in un progetto.
seo-description: Assegnare o aggiornare le risorse in un progetto.
seo-title: setProjectAssets
solution: Experience Manager
title: setProjectAssets
topic: Scene7 Image Production System API
uuid: 98d18948-d387-4890-9c27-e8ab60cded1d
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---


# setProjectAssets{#setprojectassets}

Assegnare o aggiornare le risorse in un progetto.

Sintassi

## Tipi di utenti autorizzati {#section-8d87939db6d547b48ca6d71771bbefa8}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parametri {#section-bd51ef23deaf434ba2efb8cef2a8b4a5}

**Input (setProjectAssetsParam)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| ` *`companyName`*` | `xsd:string` | Sì | Maniglia aziendale. |
| ` *`projectHandle`*` | `xsd:string` | Sì | Handle del progetto. |
| ` *`assetHandleArray`*` | `types:HandleArray` | Sì | L’array di handle di risorsa da associare al progetto. |

**Output (setProjectAssetsReturn)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| ` *`successCount`*` | `xsd:int` | Sì | Numero di risorse aggiunte con successo. |

## Esempi {#section-33c1a909c3dc4aa98da474c23a036596}

Questo esempio di codice assegna una risorsa a un progetto. La richiesta restituisce un conteggio di successo di uno.

**Request Contents (Richiesta contenuto)**

```java
<setProjectAssetsParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|6</companyHandle>
   <projectHandle>p|6|ProjectTestAPI</projectHandle>
   <assetHandleArray>
      <items>a|739|1|537</items>
   </assetHandleArray>
</setProjectAssetsParam>
```

**Risposta**

```java
<setProjectAssetsReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <successCount>1</successCount>
   <warningCount>0</warningCount>
   <errorCount>0</errorCount>
</setProjectAssetsReturn>
```

