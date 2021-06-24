---
description: Sostituisce i dati immagine per una risorsa immagine.
solution: Experience Manager
title: replaceImage
feature: Dynamic Media Classic,SDK/API,Gestione risorse
role: Developer,Administrator
exl-id: bf8c1f5c-7829-4750-b5b7-b8b20d115d17
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '110'
ht-degree: 13%

---

# replaceImage{#replaceimage}

Sostituisce i dati immagine per una risorsa immagine.

Sintassi

## Tipi di utenti autorizzati {#section-e2aad71fb2a54612badc7b16f82ed544}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parametri {#section-0d0ab668fa6d4310a93fb7ef8d8dd1e0}

**Input (replaceImageParam)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| `*`companyName`*` | `xsd:string` | Sì | L&#39;handle dell&#39;azienda con l&#39;immagine che si desidera sostituire. |
| `*`assetHandle`*` | `xsd:string` | Sì | Il handle della risorsa da sostituire. |
| `*`urlModifier`*` | `xsd:string` | Sì | Comandi Image Server che generano nuovi dati immagine. |

**Output (replaceImageReturn)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| `*`assetHandle`*` | `xsd:string` | Sì | Gestisci la nuova risorsa. |

## Esempi {#section-cebb93576bde4cb98cb27356ca66783b}

Questo esempio di codice sostituisce un&#39;immagine e applica un `urlModifier` con un comando che specifica che Image Server non interverrà in caso di sostituzione.

**Request Contents (Richiesta contenuto)**

```java
<replaceImageParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|21</companyHandle>
   <assetHandle>a|140626|1|102524</assetHandle>
   <urlModifier>action=none</urlModifier>
</replaceImageParam>
```

**Risposta**

```java
<replaceImageReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <assetHandle>a|140626|1|102524</assetHandle>
</replaceImageReturn>
```
