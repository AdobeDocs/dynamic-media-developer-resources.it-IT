---
description: Imposta la mappa immagine per una risorsa.
solution: Experience Manager
title: setImageMaps
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '140'
ht-degree: 10%

---


# setImageMaps{#setimagemaps}

Imposta la mappa immagine per una risorsa.

Devi aver già creato le mappe immagine. Le mappe immagine vengono applicate in ordine di recupero dalla matrice. Questo significa che la seconda mappa immagine si sovrappone alla prima, la terza alla seconda e così via.

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
| `*`companyHandle`*` | `xsd:string` | Sì | Tratta l&#39;azienda. |
| `*`assetHandle`*` | `xsd:string` | Sì | Gestione risorse. |
| `*`imageMapArray`*` | `types:ImageMapDefinitionArray` | Sì | Array di mappe immagine predefinite. |

**Output (setImageMapsReturn)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| `*`imageMapHandleArray`*` | `types:HandleArray` | Sì | Matrice con handle di mappa immagine applicati alla risorsa. |

## Esempi {#section-fe2e35662a6a4ee29cf250c9fd180371}

Questo esempio di codice imposta 2 mappe immagine per una risorsa immagine. Il codice specifica il tipo di forma, la regione e l&#39;azione eseguita quando vengono richiamate le mappe immagine. La risposta contiene un array con maniglie per le mappe immagine.

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

