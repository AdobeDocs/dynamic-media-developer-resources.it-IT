---
description: Imposta i comandi del protocollo Image Server o Image Rendering per la risorsa specificata. Questi comandi modificano la rappresentazione della risorsa senza distruggerla.
seo-description: Imposta i comandi del protocollo Image Server o Image Rendering per la risorsa specificata. Questi comandi modificano la rappresentazione della risorsa senza distruggerla.
seo-title: setUrlModifier
solution: Experience Manager
title: setUrlModifier
topic: Scene7 Image Production System API
uuid: ec423e57-338b-4a32-be5a-a73fa96712ce
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# setUrlModifier{#seturlmodifier}

Imposta i comandi del protocollo Image Server o Image Rendering per la risorsa specificata. Questi comandi modificano la rappresentazione della risorsa senza distruggerla.

Per Image Server, i comandi nel `urlModifier` parametro vengono pubblicati nel campo del catalogo modificatore e applicati prima di qualsiasi comando specificato nell’URL della richiesta. I comandi in `urlPostApplyModifier` verranno pubblicati nel campo `PostModifier` catalogo e ignoreranno eventuali comandi presenti nell’URL della richiesta o in `urlModifier`. Per il rendering delle immagini, i comandi in `urlModifier` e `urlPostApplyModifier` vengono concatenati e pubblicati nel campo Catalogo modificatori.

## Tipi di utenti autorizzati {#section-fefcd732ccf64c78956606538f96c73d}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parametri {#section-3304fe49bbe24ea1a886e19aaf41fb7d}

**Input (setUrlModifierParam)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | Sì | Maniglia aziendale. |
| ` *`assetHandle`*` | `xsd:string` | Sì | Handle risorsa. |
| ` *`urlModifier`*` | `xsd:string` | No | Comandi del protocollo Image Server o Image Rendering da applicare prima della richiesta o dei `urlPostApplyModifier` comandi. |
| ` *`urlPostApplyModifier`*` | `xsd:string` | No | Comandi del protocollo Image Server o Image Rendering da applicare dopo `urlModifier` e richiedere i comandi. |

**Output (setUrlModifierReturn)**

L&#39;API IPS non restituisce una risposta per questa operazione.

## Esempi {#section-801d4b9b986443f59a5783a3d6bf44aa}

**Request Contents (Richiesta contenuto)**

```java
<setUrlModifierParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|6</companyHandle>
   <assetHandle>a|942|1|579</assetHandle>
   <urlModifier>modify=that</urlModifier>
   <urlPostApplyModifier>action=awesomeToo</urlPostApplyModifier>
</setUrlModifierParam>
```

**Risposta**

Nessuno.
