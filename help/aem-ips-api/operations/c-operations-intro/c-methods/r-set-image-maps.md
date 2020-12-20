---
description: Imposta la mappa immagine per una risorsa.
seo-description: Imposta la mappa immagine per una risorsa.
seo-title: setImageMaps
solution: Experience Manager
title: setImageMaps
topic: Scene7 Image Production System API
uuid: 1dd7e032-34b4-464d-8ec6-7ad282d12891
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '141'
ht-degree: 9%

---


# setImageMaps{#setimagemaps}

Imposta la mappa immagine per una risorsa.

Dovete aver già creato le mappe immagine. Le mappe immagine vengono applicate in ordine di recupero dall&#39;array. Questo significa che la seconda mappa immagine si sovrappone alla prima, la terza alla seconda e così via.

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
| ` *`companyHandle`*` | `xsd:string` | Sì | Maniglia aziendale. |
| ` *`assetHandle`*` | `xsd:string` | Sì | Handle risorsa. |
| ` *`imageMapArray`*` | `types:ImageMapDefinitionArray` | Sì | Matrice di mappe immagine predefinite. |

**Output (setImageMapsReturn)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| ` *`imageMapHandleArray`*` | `types:HandleArray` | Sì | Un array con le maniglie della mappa immagine applicate alla risorsa. |

## Esempi {#section-fe2e35662a6a4ee29cf250c9fd180371}

Questo esempio di codice imposta 2 mappe immagine per una risorsa immagine. Il codice specifica il tipo di forma, la regione e l’azione eseguite quando vengono richiamate le mappe immagine. La risposta contiene un array con le maniglie delle mappe immagine.

**Request Contents (Richiesta contenuto)**

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

