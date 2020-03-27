---
description: Aggiorna le impostazioni del formato di pubblicazione della vignettatura.
seo-description: Aggiorna le impostazioni del formato di pubblicazione della vignettatura.
seo-title: updateVignettePublishFormat
solution: Experience Manager
title: updateVignettePublishFormat
topic: Scene7 Image Production System API
uuid: ef8ae609-56e8-4ed6-906b-0668c5873946
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# updateVignettePublishFormat{#updatevignettepublishformat}

Aggiorna le impostazioni del formato di pubblicazione della vignettatura.

## Tipi di utenti autorizzati {#section-2f2ad136d2884dc9bfef6da008196ed0}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## Parametri {#section-8c7ba8d2bce14071b21fccb11f44749f}

**Input (updateVignettePublishFormatParam)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | Sì | Maniglia aziendale. |
| ` *`vignetteFormatHandle`*` | `xsd:string` | Sì | handle di formato di pubblicazione. |
| ` *`name`*` | `xsd:string` | No | Nome del formato di pubblicazione. |
| ` *`targetWidth`*` | `xsd:int` | Sì | Specifica la larghezza di destinazione della visualizzazione della vignettatura risultante, in pixel. Utilizzate zero in modo che la vignettatura di output abbia le stesse dimensioni della vignettatura principale. |
| ` *`targetHeight`*` | `xsd:int` | Sì | Specifica l&#39;altezza di destinazione della visualizzazione della vignettatura risultante, in pixel. Utilizzate zero in modo che la vignettatura di output abbia le stesse dimensioni della vignettatura principale. |
| ` *`createPyramid`*` | `xsd:boolean` | Sì | Crea una vignettatura piramidale ottimizzata per lo zoom sul server Image Rendering. Partendo dalla dimensione massima impostata mediante i campi Dimensione vignettatura destinazione, vengono create visualizzazioni con diverse dimensioni in un singolo file di output vignettatura. Ciascuna dimensione di visualizzazione successiva è dimezzata fino ad arrivare a valori di larghezza e altezza che rientrano in 128x128 pixel. |
| ` *`thumbWidth`*` | `xsd:int` | Sì | Specifica la larghezza di ciascuna miniatura risultante, in pixel. Questa impostazione è facoltativa. Lasciate zero per nessun file di miniatura. |
| ` *`saveAsVersion`*` | `xsd:int` | Sì | Specifica il formato di file per le vignettature pubblicate. Data una nuova versione di Image Authoring e una precedente versione del Image Rendering Server, è necessario specificare una versione di vignettatura leggibile dal server ImageRendering. Se specificate una versione superiore, il server di rendering immagini non sarà in grado di leggere le vignettature pubblicate. Impostate su zero per pubblicare le vignettature nella versione più recente. |
| ` *`sizeSuffixSeparator`*` | `xsd:string` | Sì | Specifica il carattere che separa il nome della vignettatura e il suffisso che ne indica la larghezza. |
| ` *`rendere più nitido`*` | `xsd:int` | No | Applica la nitidezza all’immagine della vista principale per ciascuna dimensione di vignettatura di pubblicazione. La nitidezza può compensare la sfocatura quando le vignettature vengono ridimensionate. |
| ` *`usmAmount`*` | `xsd:double` | Sì | Il mascheramento digitale di contrasto è un metodo flessibile e potente per aumentare la nitidezza, soprattutto nelle immagini scansionate. Questo controlla la grandezza di ogni overshot (quanto più scuri e leggeri diventano i bordi dei bordi). |
| ` *`usmRadius`*` | `xsd:double` | Sì | Influisce sulle dimensioni dei bordi da migliorare o sulla larghezza dei cerchi dei bordi che diventano, in modo che un raggio più piccolo esalti i dettagli di scala più piccola. Valori di raggio più elevati possono causare aloni ai bordi. I dettagli fini necessitano di un raggio più piccolo, poiché i minimi dettagli delle stesse dimensioni o inferiori al raggio vengono persi. |
| ` *`usmThreshold`*` | `xsd:int` | Sì | Controlla la variazione minima di luminosità da rendere più nitida o la distanza tra i valori tonali adiacenti prima del funzionamento del filtro. Questa impostazione consente di rendere più nitidi i bordi mentre altri bordi più sottili non vengono toccati. L&#39;intervallo di soglia consentito è compreso tra 0 e 255. |

**Output (updateVignettePublishFormatReturn)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| ` *`vignetteFormatHandle`*` | `xsd:string` | Sì | Gestite il formato di pubblicazione della vignettatura aggiornato. |

## Esempio {#section-fcba4bf2b7264786a676e315a35dbe43}

Questo esempio di codice aggiorna il formato di pubblicazione di una vignettatura e restituisce l’handle al formato aggiornato.

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

