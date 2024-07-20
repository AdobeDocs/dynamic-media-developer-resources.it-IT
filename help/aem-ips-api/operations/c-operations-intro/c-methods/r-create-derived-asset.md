---
description: Crea una nuova risorsa derivata da una risorsa immagine di origine principale esistente.
solution: Experience Manager
title: createDerivedAsset
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: a3b20a8a-ed0d-40be-9a8c-41ba09b1d724
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '259'
ht-degree: 6%

---

# createDerivedAsset{#createderivedasset}

Crea una nuova risorsa derivata da una risorsa immagine di origine principale esistente.

Sintassi

<!--<a id="section_FE43FF204ED644C2AC901AF45982E942"></a>-->

Le risorse derivate specificano i comandi del protocollo Image Server che modificano la rappresentazione dell&#39;immagine proprietaria. Il tipo derivato `AdjustedView` consente di applicare semplici modifiche a una singola immagine (ad esempio, specificando un rettangolo di ritaglio), mentre `LayerView` consente di creare una visualizzazione a più livelli che può includere testo o immagini aggiuntive.

A differenza di una copia immagine (vedi [copyImage](../../../operations/c-operations-intro/c-methods/r-copy-image.md#reference-0785131e690b4ad08be69172023f35d0)), un&#39;immagine derivata è collegata all&#39;immagine proprietaria. Le modifiche all’immagine del proprietario modificano le risorse derivate associate. Se si elimina l&#39;immagine del proprietario, verranno eliminate anche le eventuali immagini derivate associate.

## Tipi di utenti autorizzati {#authorized-user-types}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parametri {#section-5a0dde01cff6454da3646ea805c2be1e}

**Input (createDerivedAssetParam)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| companyHandle | `xsd:string` | Sì | Handle dell&#39;azienda che contiene la risorsa da cui si ottiene la nuova risorsa. |
| ownerHandle | `xsd:string` | Sì | Handle della risorsa immagine principale da cui deriva la nuova immagine. |
| folderHandle | `xsd:string` | Sì | Handle della cartella in cui viene creata la nuova risorsa derivata. |
| nome | `xsd:string` | Sì | Nome della risorsa derivata. |
| tipo | `xsd:string` | Sì | Tipo di risorsa della nuova risorsa derivata: `AdjustedView` o `LayerView`. |
| urlModifier | `xsd:string` | No | I comandi del protocollo Image Server o Image Rendering hanno applicato *prima* della richiesta o `urlPostApplyModifier` comandi. |
| urlPostApplyModifier | `xsd:string` | No | Comandi del protocollo Image Server o Image Rendering applicati *dopo* alla richiesta o `urlPostApplyModifier` comandi. |

**Output (createDerivedAssetParam)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| assetHandle | `xsd:string` | Sì | Handle della risorsa derivata. |

## Esempi {#section-5d5ea893a1ef4edc8b3a396f1936e8c9}

Il codice di esempio crea una risorsa derivata con una vista regolata e `urlModifier` e `urlPostApplyModifier` con valori arbitrari. La risposta restituisce l’handle della risorsa appena derivata.

**Richiesta**

```java
<createDerivedAssetParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|6</companyHandle>
   <ownerHandle>a|943|1|580</ownerHandle>
   <folderHandle>ApiTestCo/</folderHandle>
   <name>ApiDerivedAsset</name>
   <type>AdjustedView</type>
   <urlModifier>modify=this</urlModifier>
   <urlPostApplyModifier>action=awesome</urlPostApplyModifier>
</createDerivedAssetParam>
```

**Risposta**

```java
<createDerivedAssetReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <assetHandle>a|944|10|2</assetHandle>
</createDerivedAssetReturn>
```
