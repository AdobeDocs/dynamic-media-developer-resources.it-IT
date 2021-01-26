---
description: Restituisce i contesti di pubblicazione per le risorse contrassegnate per la pubblicazione.
solution: Experience Manager
title: batchGetAssetPublishContext
topic: Dynamic Media Image Production System API
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '97'
ht-degree: 14%

---


# batchGetAssetPublishContext{#batchgetassetpublishcontexts}

Restituisce i contesti di pubblicazione per le risorse contrassegnate per la pubblicazione.

Sintassi

## Tipi di utenti autorizzati {#section-d5362ca8a6ab42949cd648ba38dbf2f8}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

>[!NOTE]
>
>* Per restituire le risorse, l’utente deve disporre dell’accesso in lettura.
>* Tutti gli utenti hanno accesso alla società condivisa.

>



## Parametri {#section-1742fcb196224545b270eb8241f757a8}

**Input (batchGetAssetPublishContextsParam)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Sì | Gestite l&#39;azienda. |
| `*`assetHandleArray`*` | ` `type:HandleArray&quot; | Sì | Elenco delle risorse per le quali eseguire una query per i contesti attivi (contrassegnati per la pubblicazione). |

**Output (batchGetAssetPublishContextsReturn)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| `*`assetPublishContextArray`*` | `types:assetPublishContextsArray` | Sì | Un array di contesti di pubblicazione in cui ogni risorsa è contrassegnata per la pubblicazione. |

## Esempi {#section-457f6809ccfa425b9a0976313d613f4e}

**Request Contents (Richiesta contenuto)**

```java
<batchGetAssetPublishContextsParam xmlns="http://www.scene7.com/IpsApi/xsd/2011-11-04">
  <companyHandle>c|301</companyHandle>
  <assetHandleArray>
    <items>a|27007</items>
    <items>a|27008</items>
  </assetHandleArray>
</batchGetAssetPublishContextsParam>
```

**Risposta**

```java
<batchGetAssetPublishContextsReturn xmlns="http://www.scene7.com/IpsApi/xsd/2011-11-04">
  <assetPublishContextsArray>
    <items>
      <assetHandle>a|27007</assetHandle>
      <publishContextArray>
        <items>
          <contextHandle>pc|3002</contextHandle>
          <contextName>ImageServing</contextName>
          <contextType>ImageServing</contextType>
        </items>
      </publishContextArray>
    </items>
    <items>
      <assetHandle>a|27008</assetHandle>
      <publishContextArray>
        <items>
          <contextHandle>pc|3004</contextHandle>
          <contextName>Video</contextName>
          <contextType>Video</contextType>
        </items>
        <items>
          <contextHandle>pc|3001</contextHandle>
          <contextName>ImageRendering</contextName>
          <contextType>ImageRendering</contextType>
        </items>
      </publishContextArray>
    </items>
  </assetPublishContextsArray>
</batchGetAssetPublishContextsReturn>
```

