---
description: Impostate o aggiornate lo stato di pubblicazione per una o più risorse. Potete impostare stati di pubblicazione separati per ciascun contesto di pubblicazione di una società.
seo-description: Impostate o aggiornate lo stato di pubblicazione per una o più risorse. Potete impostare stati di pubblicazione separati per ciascun contesto di pubblicazione di una società.
seo-title: setAssetsContextState
solution: Experience Manager
title: setAssetsContextState
topic: Dynamic Media Image Production System API
uuid: 4b94f9ea-3f7b-45ee-9381-6434f2bc4e31
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '183'
ht-degree: 9%

---


# setAssetsContextState{#setassetscontextstate}

Impostate o aggiornate lo stato di pubblicazione per una o più risorse. Potete impostare stati di pubblicazione separati per ciascun contesto di pubblicazione di una società.

## Tipi di utenti autorizzati {#section-815eb031f85143278c1560c18c5e3431}

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
>Per restituire la risorsa, l’utente deve disporre dell’accesso in lettura.

## Parametri {#section-009b9006de8e4c16ad657c47f28ace9f}

**Input (setAssetsContextStateParam)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Sì | Gestite l&#39;azienda. |
| `*`assetsContextHandle`*` | `types:AssetsContextStateUpdateArray` | Sì | Un array di risorse e relativi nuovi stati di pubblicazione. |

**Output (setAssetsContexStateReturn)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| `*`successCount`*` | `xsd:int` | Sì | Numero di risorse modificate. |
| `*`warningCount`*` | `xsd:int` | Sì | Numero di avvisi generati quando l’operazione tentava di modificare le risorse. |
| `*`errorCount`*` | `xsd:int` | Sì | Numero di errori generati quando l’operazione tentava di modificare le risorse. |
| `*`warningDetailArray`*` | `types:AssetOperationFaultArray` | No | Array di errori generati dalle risorse quando l&#39;operazione tentava di modificarli. |

## Esempi {#section-283a073f3cb14bcda5abed863c538aa4}

Questo esempio di codice imposta lo stato di pubblicazione di una risorsa utilizzando `NotMarkedForPublish`.

**Request Contents (Richiesta contenuto)**

```java
<setAssetsContextStateParam xmlns="http://www.scene7.com/IpsApi/xsd/2011-11-04">
  <companyHandle>c|301</companyHandle>
  <assetsContextStateUpdateArray>
    <items>
      <assetHandle>a|27007</assetHandle>
      <contextStateUpdateArray>
        <items>
          <contextHandle>pc|3001</contextHandle>
          <publishState>NotMarkedForPublish</publishState>
        </items>
        <items>
          <contextHandle>pc|3002</contextHandle>
          <publishState>MarkedForPublish</publishState>
        </items>
        <items>
          <contextHandle>pc|3003</contextHandle>
          <publishState>NotMarkedForPublish</publishState>
        </items>
        <items>
          <contextHandle>pc|3004</contextHandle>
          <publishState>NotMarkedForPublish</publishState>
        </items>
      </contextStateUpdateArray>
    </items>
    <items>
      <assetHandle>a|27008</assetHandle>
      <contextStateUpdateArray>
        <items>
          <contextHandle>pc|3001</contextHandle>
          <publishState>MarkedForPublish</publishState>
        </items>
        <items>
          <contextHandle>pc|3002</contextHandle>
          <publishState>NotMarkedForPublish</publishState>
        </items>
        <items>
          <contextHandle>pc|3003</contextHandle>
          <publishState>NotMarkedForPublish</publishState>
        </items>
        <items>
          <contextHandle>pc|3004</contextHandle>
          <publishState>MarkedForPublish</publishState>
        </items>
      </contextStateUpdateArray>
    </items>
  </assetsContextStateUpdateArray>
</setAssetsContextStateParam>
```

**Risposta**

```java
<setAssetsContextStateReturn xmlns="http://www.scene7.com/IpsApi/xsd/2011-11-04-beta">
  <successCount>8</successCount>
  <warningCount>0</warningCount>
  <errorCount>0</errorCount>
</setAssetsContextStateReturn>
```

