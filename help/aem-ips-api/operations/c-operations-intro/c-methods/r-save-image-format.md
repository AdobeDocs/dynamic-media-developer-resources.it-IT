---
description: Crea un formato immagine.
solution: Experience Manager
title: saveImageFormat
feature: Dynamic Media Classic, SDK/API
role: Developer,Administrator
exl-id: cafbd715-237b-4454-920e-643f0c84e208
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '151'
ht-degree: 11%

---

# saveImageFormat{#saveimageformat}

Crea un formato immagine.

>[!NOTE]
>
>Il valore del campo `urlModifier` deve essere costituito da un XML valido. Ad esempio, modificare `&` in `&`. Ottieni il valore `urlModfier` dall’interfaccia utente IPS.

## Tipi di utenti autorizzati {#section-12c9d8d5933f4692bafb194060b4f882}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## Parametri {#section-b1fc2fe8d606490ba3a2c979ab8bbd78}

**Input (saveImageFormatParam)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Sì | L&#39;handle dell&#39;azienda con il formato immagine con cui desideri lavorare. |
| `*`imageFormatHandle`*` | `xsd:string` | No | Maniglia del formato immagine da salvare. |
| `*`name`*` | `xsd:string` | Sì | Nome del formato immagine. |
| `*`urlModifier`*` | `xsd:string` | Sì | Può essere una qualsiasi stringa di query del protocollo IPS. Il modo più semplice per generare un modificatore URL è quello di crearne uno con l’interfaccia utente IPS, quindi tagliare e incollare la stringa di query. |

**Output (saveImageFormatReturn)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| `*`imageFormatHandle`*` | `xsd:string` | Sì | Gestisci il formato immagine. |

## Esempi {#section-c7bd733212ef494297a97093f3af193f}

Questo esempio di codice crea un formato immagine. In questo esempio, `urlModifier` è stato determinato dal relativo valore nell’interfaccia utente IPS con un formato HTML valido.

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
