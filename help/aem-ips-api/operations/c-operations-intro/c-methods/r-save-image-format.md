---
description: Crea un formato immagine.
solution: Experience Manager
title: saveImageFormat
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: cafbd715-237b-4454-920e-643f0c84e208
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '146'
ht-degree: 10%

---

# saveImageFormat{#saveimageformat}

Crea un formato immagine.

>[!NOTE]
>
>Il `urlModifier` il valore del campo deve essere costituito da un XML valido. Ad esempio, modifica `&` a `&`. Ottieni `urlModfier` dall&#39;interfaccia utente IPS.

## Tipi di utenti autorizzati {#section-12c9d8d5933f4692bafb194060b4f882}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## Parametri {#section-b1fc2fe8d606490ba3a2c979ab8bbd78}

**Input (saveImageFormatParam)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| companyHandle | `xsd:string` | Sì | Handle per l&#39;azienda con il formato immagine che si desidera utilizzare. |
| imageFormatHandle | `xsd:string` | No | Handle di formato immagine da salvare. |
| nome | `xsd:string` | Sì | Nome formato immagine. |
| urlModifier | `xsd:string` | Sì | Può trattarsi di qualsiasi stringa di query del protocollo IPS. Il modo più semplice per generare un modificatore URL è crearne uno con l’interfaccia utente IPS e quindi tagliare e incollare la stringa di query. |

**Output (saveImageFormatReturn)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| imageFormatHandle | `xsd:string` | Sì | Gestisci il formato immagine. |

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
