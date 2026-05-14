---
description: Imposta la mappa immagine per una risorsa.
solution: Experience Manager
title: setImageMaps
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 0c8e6536-0b9c-4fcc-b71f-511afc670089
TQID: 'https://experienceleague.adobe.com/sOGDO0ruTEK1DS5Sc-4nhLfViddEKCLDLJlpC-8H3g0'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 134
ht-degree: 8%

---

# setImageMaps{#setimagemaps}

Imposta la mappa immagine per una risorsa.

Le mappe immagine devono essere già state create. Le mappe immagine vengono applicate in ordine di recupero dall’array. Ciò significa che la seconda mappa immagine si sovrappone alla prima, la terza sovrappone la seconda e così via.

## Tipi di utenti autorizzati {#section-adb21c5b679249939dd83816e4a0ee97}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parametri {#section-2292ec1aead947ef8741dd0653a41f42}

**Input (setImageMapsParam)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| companyHandle | `xsd:string` | Sì | Gestore azienda. |
| assetHandle | `xsd:string` | Sì | Handle risorsa. |
| imageMapArray | `types:ImageMapDefinitionArray` | Sì | Array di mappe immagine predefinite. |

**Output (setImageMapsReturn)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| imageMapHandleArray | `types:HandleArray` | Sì | Array con handle di mappa immagine applicati alla risorsa. |

## Esempi {#section-fe2e35662a6a4ee29cf250c9fd180371}

Questo esempio di codice imposta 2 mappe immagine per una risorsa immagine. Il codice specifica il tipo di forma, l&#39;area e l&#39;azione eseguita quando vengono richiamate le mappe immagine. La risposta contiene un array con handle per le mappe immagine.

**Richiesta**

```java
<setImageMapsParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|6</companyHandle>
   <assetHandle>a|739|1|537</assetHandle>
   <imageMapArray>
      <items>
         <name>ImageMap2</name>
         <shapeType>Rectangle</shapeType>
         <region>40</region>
         <action>400</action>
         <enabled>true</enabled>
      </items>
      <items>
         <name>ImageMap3</name>
         <shapeType>Rectangle</shapeType>
         <region>40</region>
         <action>400</action>
         <enabled>false</enabled>
      </items>
   </imageMapArray>
</setImageMapsParam>
```
