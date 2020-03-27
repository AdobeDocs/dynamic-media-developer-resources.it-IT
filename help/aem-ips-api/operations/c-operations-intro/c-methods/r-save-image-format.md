---
description: Crea un formato immagine.
seo-description: Crea un formato immagine.
seo-title: saveImageFormat
solution: Experience Manager
title: saveImageFormat
topic: Scene7 Image Production System API
uuid: b11ea668-7a82-439c-b16b-909dc86c00a2
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# saveImageFormat{#saveimageformat}

Crea un formato immagine.

>[!NOTE]
>
>Il valore del `urlModifier` campo deve essere costituito da un XML valido. Ad esempio, passate `&` a `&`. Ottenete il `urlModfier` valore dall&#39;interfaccia utente IPS.

## Tipi di utenti autorizzati {#section-12c9d8d5933f4692bafb194060b4f882}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## Parametri {#section-b1fc2fe8d606490ba3a2c979ab8bbd78}

**Input (saveImageFormatParam)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | Sì | L’handle della società con il formato immagine con cui desiderate lavorare. |
| ` *`imageFormatHandle`*` | `xsd:string` | No | Handle del formato immagine da salvare. |
| ` *`name`*` | `xsd:string` | Sì | Nome del formato immagine. |
| ` *`urlModifier`*` | `xsd:string` | Sì | Può trattarsi di una qualsiasi stringa di query del protocollo IPS. Il modo più semplice per generare un modificatore URL consiste nel crearne uno con l’interfaccia utente IPS, quindi tagliare e incollare la stringa di query. |

**Output (saveImageFormatReturn)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| ` *`imageFormatHandle`*` | `xsd:string` | Sì | Gestite il formato dell’immagine. |

## Esempi {#section-c7bd733212ef494297a97093f3af193f}

Questo esempio di codice crea un formato immagine. In questo esempio, `urlModifier` è stato determinato dal relativo valore nell&#39;interfaccia utente IPS con un formato HTML valido.

**Request Contents (Richiesta contenuto)**

```java
<saveImageFormatParam xmlns="http://www.scene7.com/IpsApi/xsd"> 
   <companyHandle>47</companyHandle> 
   <name>My Image Format Name</name> 
   <urlModifier>wid=400&amp;hei=400&amp;fmt=jpeg&amp;qlt=750&amp;op_sharpen=0&amp; 
   resMode=bicub&amp;op_usm=0.0,0.0,0,0&amp;iccEmbed=0 
   </urlModifier> 
</saveImageFormatParam>
```

**Risposta**

```java
<saveImageFormatReturn xmlns="http://www.scene7.com/IpsApi/xsd"> 
   <imageFormatHandle>47|301</imageFormatHandle> 
</saveImageFormatReturn>
```

