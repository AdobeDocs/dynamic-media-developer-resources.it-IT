---
description: Aggiorna le impostazioni del formato di pubblicazione della vignetta.
solution: Experience Manager
title: updateVignettePublishFormat
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '441'
ht-degree: 20%

---


# updateVignettePublishFormat{#updatevignettepublishformat}

Aggiorna le impostazioni del formato di pubblicazione della vignetta.

## Tipi di utenti autorizzati {#section-2f2ad136d2884dc9bfef6da008196ed0}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## Parametri {#section-8c7ba8d2bce14071b21fccb11f44749f}

**Input (updateVignettePublishFormatParam)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Sì | Tratta l&#39;azienda. |
| `*`vignetteFormatHandle`*` | `xsd:string` | Sì | Maniglia del formato di pubblicazione. |
| `*`name`*` | `xsd:string` | No | Nome del formato di pubblicazione. |
| `*`targetWidth`*` | `xsd:int` | Sì | Specifica la larghezza di destinazione della visualizzazione della vignetta risultante in pixel. Usa zero in modo che la vignetta di output abbia le stesse dimensioni della vignetta primaria. |
| `*`targetHeight`*` | `xsd:int` | Sì | Specifica l&#39;altezza di destinazione della visualizzazione della vignetta risultante in pixel. Usa zero in modo che la vignetta di output abbia le stesse dimensioni della vignetta primaria. |
| `*`createPyramid`*` | `xsd:boolean` | Sì | Crea una vignettatura piramidale ottimizzata per lo zoom sul server Image Rendering. Partendo dalla dimensione massima impostata mediante i campi Dimensione vignettatura destinazione, vengono create visualizzazioni con diverse dimensioni in un singolo file di output vignettatura. Ciascuna dimensione di visualizzazione successiva è dimezzata fino ad arrivare a valori di larghezza e altezza che rientrano in 128x128 pixel. |
| `*`thumbWidth`*` | `xsd:int` | Sì | Specifica la larghezza di ogni miniatura risultante in pixel. Questa impostazione è facoltativa. Lascia come zero per nessun file di miniatura. |
| `*`saveAsVersion`*` | `xsd:int` | Sì | Specifica il formato di file per le vignette pubblicate. Data una nuova versione di Image Authoring e una versione precedente di Image Rendering Server, è necessario specificare una versione di vignetta leggibile dal server ImageRendering. Se si specifica una versione successiva, il server Image Rendering non è in grado di leggere le vignette pubblicate. Imposta su zero per pubblicare le vignette nella versione più recente. |
| `*`sizeSuffixSeparator`*` | `xsd:string` | Sì | Specifica il carattere che separa il nome della vignettatura e il suffisso che ne indica la larghezza. |
| `*`affilare`*` | `xsd:int` | No | Applica la nitidezza all&#39;immagine della visualizzazione principale per ogni dimensione della vignetta di pubblicazione. La nitidezza può compensare la sfocatura quando le vignette vengono ridimensionate. |
| `*`usmAmount`*` | `xsd:double` | Sì | La funzione di mascheramento intelligente digitale è un modo flessibile e potente per aumentare la nitidezza, specialmente nelle immagini scansionate. Questo controlla la grandezza di ogni sovrimpressione (quanto più scuro e leggero diventano i bordi dei bordi). |
| `*`usmRadius`*` | `xsd:double` | Sì | Influisce sulle dimensioni dei bordi da migliorare o sulla larghezza dei bordi che diventano, in modo che un raggio più piccolo migliori i dettagli più piccoli. Valori di raggio più elevati possono causare alone ai bordi. La precisione dei dettagli ha bisogno di un raggio più piccolo, dato che i minimi dettagli delle stesse dimensioni o minori del raggio vengono persi. |
| `*`usmThreshold`*` | `xsd:int` | Sì | Controlla la variazione minima di luminosità da rendere più nitida o la distanza di separazione dei valori tonali adiacenti prima che il filtro funzioni. Questa impostazione può rendere più nitidi i bordi più pronunciati lasciando intatti i bordi più sottili. L’intervallo di soglia consentito è compreso tra 0 e 255. |

**Output (updateVignettePublishFormatReturn)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| `*`vignetteFormatHandle`*` | `xsd:string` | Sì | Gestisci il formato di pubblicazione della vignetta aggiornato. |

## Esempio {#section-fcba4bf2b7264786a676e315a35dbe43}

Questo esempio di codice aggiorna un formato di pubblicazione della vignetta e restituisce l&#39;handle al formato aggiornato.

**Request Contents (Richiesta contenuto)**

```java
<updateVignettePublishFormatParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|21</companyHandle>
   <vignetteFormatHandle>v|21|283</vignetteFormatHandle>
   <name>APIcreateVignettePublishFormat2</name>
   <targetWidth>1000</targetWidth>
   <targetHeight>800</targetHeight>
   <createPyramid>false</createPyramid>
   <thumbWidth>100</thumbWidth>
   <saveAsVersion>0</saveAsVersion>
   <sizeSuffixSeparator>-</sizeSuffixSeparator>
   <sharpen>50</sharpen>
   <usmAmount>240.0</usmAmount>
   <usmRadius>3.1</usmRadius>
   <usmThreshold>150</usmThreshold>
</updateVignettePublishFormatParam>
```

**Risposta**

```java
<updateVignettePublishFormatReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <vignetteFormatHandle>v|21|283</vignetteFormatHandle>
</updateVignettePublishFormatReturn>
```

