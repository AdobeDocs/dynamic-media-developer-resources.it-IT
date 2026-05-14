---
description: Crea un formato immagine.
solution: Experience Manager
title: saveImageFormat
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: cafbd715-237b-4454-920e-643f0c84e208
TQID: 'https://experienceleague.adobe.com/kP25DoK-SIRIYh69I8tE07KH4dI-GFZf9JjUZjG-lFw'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 146
ht-degree: 8%

---

# saveImageFormat{#saveimageformat}

Crea un formato immagine.

>[!NOTE]
>
>Il valore del campo `urlModifier` deve essere costituito da un XML valido. Modificare ad esempio `&` in `&`. Ottiene il valore `urlModfier` dall&#39;interfaccia utente IPS.

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

**Richiesta**

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
