---
description: Imposta i comandi del protocollo Image Server o Image Rendering per la risorsa specificata. Questi comandi modificano la rappresentazione della risorsa senza distruggerla.
solution: Experience Manager
title: setUrlModifier
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 9e96ffc8-5a38-46b8-9ba8-956c86b32c7a
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '175'
ht-degree: 4%

---

# setUrlModifier{#seturlmodifier}

Imposta i comandi del protocollo Image Server o Image Rendering per la risorsa specificata. Questi comandi modificano la rappresentazione della risorsa senza distruggerla.

Per Image Server, i comandi nel parametro `urlModifier` vengono pubblicati nel campo del catalogo dei modificatori e applicati prima dei comandi specificati nell&#39;URL della richiesta. I comandi in `urlPostApplyModifier` vengono pubblicati nel campo del catalogo `PostModifier` e sostituiscono eventuali comandi nell&#39;URL della richiesta o in `urlModifier`. Per Image Rendering, i comandi in `urlModifier` e `urlPostApplyModifier` sono concatenati e pubblicati nel campo del catalogo dei modificatori.

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
| companyHandle | `xsd:string` | Sì | Gestore azienda. |
| assetHandle | `xsd:string` | Sì | Handle risorsa. |
| urlModifier | `xsd:string` | No | Comandi del protocollo Image Server o Image Rendering da applicare prima della richiesta o di `urlPostApplyModifier`. |
| urlPostApplyModifier | `xsd:string` | No | Comandi del protocollo Image Server o Image Rendering da applicare dopo `urlModifier` e richiedere i comandi. |

**Output (setUrlModifierReturn)**

L&#39;API IPS non restituisce una risposta per questa operazione.

## Esempi {#section-801d4b9b986443f59a5783a3d6bf44aa}

**Richiesta**

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
