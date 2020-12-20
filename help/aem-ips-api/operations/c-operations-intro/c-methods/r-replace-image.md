---
description: Sostituisce i dati immagine per una risorsa immagine.
seo-description: Sostituisce i dati immagine per una risorsa immagine.
seo-title: replaceImage
solution: Experience Manager
title: replaceImage
topic: Scene7 Image Production System API
uuid: 46824e33-265c-4425-9ab1-8ad6b7ac154d
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '111'
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
| ` *`companyName`*` | `xsd:string` | Sì | L’handle della società con l’immagine da sostituire. |
| ` *`assetHandle`*` | `xsd:string` | Sì | L’handle della risorsa da sostituire. |
| ` *`urlModifier`*` | `xsd:string` | Sì | Comandi Image Server che generano nuovi dati immagine. |

**Output (replaceImageReturn)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| ` *`assetHandle`*` | `xsd:string` | Sì | Consente di passare alla nuova risorsa. |

## Esempi {#section-cebb93576bde4cb98cb27356ca66783b}

Questo esempio di codice sostituisce un&#39;immagine e applica un comando `urlModifier` in cui viene specificato che il server immagini non interverrà in caso di sostituzione.

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

