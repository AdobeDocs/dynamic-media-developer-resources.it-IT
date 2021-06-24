---
description: Imposta i comandi del protocollo Image Server o Image Rendering per la risorsa specificata. Questi comandi modificano la rappresentazione della risorsa senza distruggerla.
solution: Experience Manager
title: setUrlModifier
feature: Dynamic Media Classic, SDK/API
role: Developer,Administrator
exl-id: 9e96ffc8-5a38-46b8-9ba8-956c86b32c7a
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '182'
ht-degree: 6%

---

# setUrlModifier{#seturlmodifier}

Imposta i comandi del protocollo Image Server o Image Rendering per la risorsa specificata. Questi comandi modificano la rappresentazione della risorsa senza distruggerla.

Per Image Server, i comandi nel parametro `urlModifier` vengono pubblicati nel campo del catalogo dei modificatori e applicati prima di qualsiasi comando specificato nell’URL della richiesta. I comandi in `urlPostApplyModifier` verranno pubblicati nel campo di catalogo `PostModifier` e sostituiranno eventuali comandi nell’URL della richiesta o in `urlModifier`. Per Image Rendering, i comandi in `urlModifier` e `urlPostApplyModifier` vengono concatenati e pubblicati nel campo del catalogo modificatore.

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
| `*`companyHandle`*` | `xsd:string` | Sì | Tratta l&#39;azienda. |
| `*`assetHandle`*` | `xsd:string` | Sì | Gestione risorse. |
| `*`urlModifier`*` | `xsd:string` | No | Comandi del protocollo Image Server o Image Rendering da applicare prima della richiesta o dei comandi `urlPostApplyModifier`. |
| `*`urlPostApplyModifier`*` | `xsd:string` | No | Comandi del protocollo Image Server o Image Rendering da applicare dopo i comandi `urlModifier` e richiedere. |

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
