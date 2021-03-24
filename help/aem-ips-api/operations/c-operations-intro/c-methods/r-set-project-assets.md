---
description: Assegnare o aggiornare le risorse in un progetto.
solution: Experience Manager
title: setProjectAssets
feature: Dynamic Media Classic,SDK/API,Gestione risorse
role: Sviluppatore,Amministratore
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '92'
ht-degree: 16%

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
| `*`companyName`*` | `xsd:string` | Sì | Tratta l&#39;azienda. |
| `*`projectHandle`*` | `xsd:string` | Sì | Maniglia del progetto. |
| `*`assetHandleArray`*` | `types:HandleArray` | Sì | Matrice di handle di risorsa da associare al progetto. |

**Output (setProjectAssetsReturn)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| `*`successCount`*` | `xsd:int` | Sì | Numero di risorse aggiunte correttamente. |

## Esempi {#section-33c1a909c3dc4aa98da474c23a036596}

Questo codice di esempio assegna una risorsa a un progetto. La richiesta restituisce un conteggio di successo di uno.

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

