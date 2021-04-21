---
description: Restituisce i contesti di pubblicazione per le risorse contrassegnate per la pubblicazione.
solution: Experience Manager
title: batchGetAssetPublishContexts
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Administrator
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '106'
ht-degree: 13%

---


# batchGetAssetPublishContexts{#batchgetassetpublishcontexts}

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
| `*`companyHandle`*` | `xsd:string` | Sì | Manda all&#39;azienda. |
| `*`assetHandleArray`*` | ` `tipi:HandleArray&quot; | Sì | Elenco delle risorse per le quali si desidera eseguire una query per i contesti attivi (contrassegnati per la pubblicazione). |

**Output (batchGetAssetPublishContextsReturn)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| `*`assetPublishContextsArray`*` | `types:assetPublishContextsArray` | Sì | Matrice di contesti di pubblicazione in cui ogni risorsa è contrassegnata per la pubblicazione. |

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

