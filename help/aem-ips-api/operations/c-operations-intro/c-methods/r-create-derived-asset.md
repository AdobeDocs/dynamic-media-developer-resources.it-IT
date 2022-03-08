---
description: Crea una nuova risorsa derivata da una risorsa immagine sorgente principale esistente.
solution: Experience Manager
title: createDeriedAsset
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: a3b20a8a-ed0d-40be-9a8c-41ba09b1d724
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '261'
ht-degree: 8%

---

# createDeriedAsset{#createderivedasset}

Crea una nuova risorsa derivata da una risorsa immagine sorgente principale esistente.

Sintassi

<!--<a id="section_FE43FF204ED644C2AC901AF45982E942"></a>-->

Le risorse derivate specificano i comandi del protocollo Image Server che modificano la rappresentazione dell&#39;immagine proprietaria. La `AdjustedView` il tipo derivato consente di applicare semplici modifiche a una singola immagine (ad esempio, specificando un rettangolo di ritaglio), mentre il `LayerView` consente di creare una visualizzazione a più livelli che può includere testo o immagini aggiuntive.

A differenza di una copia immagine (vedi [copyImage](../../../operations/c-operations-intro/c-methods/r-copy-image.md#reference-0785131e690b4ad08be69172023f35d0)), un&#39;immagine derivata è collegata all&#39;immagine proprietaria. Le modifiche all&#39;immagine del proprietario modificano le risorse derivate associate. L&#39;eliminazione dell&#39;immagine del proprietario comporta l&#39;eliminazione di tutte le immagini derivate associate.

## Tipi di utenti autorizzati {#authorized-user-types}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parametri {#section-5a0dde01cff6454da3646ea805c2be1e}

**Input (createDeriedAssetParam)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| companyHandle | `xsd:string` | Sì | L’handle della società che contiene la risorsa da cui deriverai la nuova risorsa. |
| ownerHandle | `xsd:string` | Sì | L’handle della risorsa immagine principale da cui deriva la nuova immagine. |
| folderHandle | `xsd:string` | Sì | L’handle della cartella in cui viene creata la nuova risorsa derivata. |
| name | `xsd:string` | Sì | Nome della risorsa derivata. |
| Testo | `xsd:string` | Sì | Il tipo di risorsa della nuova risorsa derivata: `AdjustedView` o `LayerView`. |
| urlModifier | `xsd:string` | No | Comandi applicati al protocollo di rendering delle immagini o di rendering delle immagini *prima* la richiesta o `urlPostApplyModifier` comandi. |
| urlPostApplyModifier | `xsd:string` | No | Comandi applicati al protocollo di rendering delle immagini o di rendering delle immagini *dopo* alla richiesta o `urlPostApplyModifier` comandi. |

**Output (createDeriedAssetParam)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| assetHandle | `xsd:string` | Sì | L’handle della risorsa derivata. |

## Esempi {#section-5d5ea893a1ef4edc8b3a396f1936e8c9}

Il codice di esempio crea una risorsa derivata con una vista adeguata e `urlModifier` e `urlPostApplyModifier` con valori arbitrari. La risposta restituisce l&#39;handle alla nuova risorsa derivata.

**Request Contents (Richiesta contenuto)**

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
