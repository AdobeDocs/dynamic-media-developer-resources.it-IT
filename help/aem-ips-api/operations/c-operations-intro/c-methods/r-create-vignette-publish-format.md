---
description: Crea un nuovo formato di pubblicazione per una vignettatura.
seo-description: Crea un nuovo formato di pubblicazione per una vignettatura.
seo-title: createVignettePublishFormat
solution: Experience Manager
title: createVignettePublishFormat
topic: Scene7 Image Production System API
uuid: 834ebe6a-e105-4075-8004-172237980933
translation-type: tm+mt
source-git-commit: 55015831ed1971a305ddbd8085c95626507355e0
workflow-type: tm+mt
source-wordcount: '527'
ht-degree: 14%

---


# createVignettePublishFormat{#createvignettepublishformat}

Crea un nuovo formato di pubblicazione per una vignettatura.

I formati delle vignettature specificano le dimensioni delle vignettature pubblicate e le relative miniature, nonché i livelli di zoom, i parametri di nitidezza e la versione del formato file per le vignettature prodotte dalle vignettature primarie pubblicate su un server di rendering immagini da IPS.

Le versioni più recenti del server di rendering delle immagini supportano le vignettature a piramide, eliminando la necessità di definire formati di vignettatura specifici per la pubblicazione.

## Tipi di utenti autorizzati {#section-f5c563e3695c4dba8df41e2a965aace7}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## Parametri {#section-3a368186ec1d4005bca056fc9d9bacc7}

**Input (createVignettePublishFormatParam)**

<table id="table_4D5B2913FA784EC09190F25223C1A680"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Nome </th> 
   <th colname="col2" class="entry"> Tipo </th> 
   <th colname="col3" class="entry"> Obbligatorio </th> 
   <th colname="col4" class="entry"> Descrizione </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> companyHandle</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Sì </td> 
   <td colname="col4"> Gestire la società a cui appartiene la vignettatura. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> name</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> Frase codice </span> </td> 
   <td colname="col3"> Sì </td> 
   <td colname="col4"> Nome per identificare il formato di pubblicazione della vignettatura. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> targetWidth</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> Frase codice </span> </td> 
   <td colname="col3"> Sì </td> 
   <td colname="col4"> <p>Specifica la larghezza di destinazione della visualizzazione della vignettatura risultante, in pixel. </p> <p>Utilizzate zero in modo che la vignettatura di output abbia le stesse dimensioni della vignettatura principale. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> targetHeight</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> Frase codice </span> </td> 
   <td colname="col3"> Sì </td> 
   <td colname="col4"> Crea una vignettatura piramidale ottimizzata per lo zoom sul server Image Rendering. Partendo dalla dimensione massima impostata mediante i campi Dimensione vignettatura destinazione, vengono create visualizzazioni con diverse dimensioni in un singolo file di output vignettatura. Ciascuna dimensione di visualizzazione successiva è dimezzata fino ad arrivare a valori di larghezza e altezza che rientrano in 128x128 pixel. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> createPyramid</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> Frase codice </span> </td> 
   <td colname="col3"> Sì </td> 
   <td colname="col4"> Specifica la larghezza di ciascuna miniatura risultante, in pixel. Questa impostazione è facoltativa. Lasciate zero per nessun file di miniatura. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> thumbWidth</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> Frase codice </span> </td> 
   <td colname="col3"> Sì </td> 
   <td colname="col4"> Specifica il formato di file per le vignettature pubblicate. Data una nuova versione di Image Authoring e una versione precedente del Image Rendering Server, dovete specificare una versione di vignettatura che può essere letta dal server ImageRendering. Se specificate una versione superiore, il server di rendering immagini non sarà in grado di leggere le vignettature pubblicate. Impostate su zero per pubblicare le vignettature nella versione più recente. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> saveAsVersion</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> Frase codice </span> </td> 
   <td colname="col3"> Sì </td> 
   <td colname="col4"> Specifica il carattere che separa il nome della vignettatura e il suffisso che ne indica la larghezza. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> sizeSuffixSeparator</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> Frase codice </span> </td> 
   <td colname="col3"> Sì </td> 
   <td colname="col4"> Specifica il carattere che separa il nome della vignettatura e il suffisso che ne indica la larghezza. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> rendere più nitido</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> Frase codice </span> </td> 
   <td colname="col3"> No </td> 
   <td colname="col4"> Applica la nitidezza all’immagine di visualizzazione principale per ogni dimensione di vignettatura di colore di colore automatico. La nitidezza può compensare la sfocatura quando i vignettatori vengono ridimensionati. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> usmAmount</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> Frase codice </span> </td> 
   <td colname="col3"> Sì </td> 
   <td colname="col4"> Il mascheramento digitale di contrasto è un metodo flessibile e potente per aumentare la nitidezza, soprattutto nelle immagini scansionate. Questo controlla la grandezza di ogni overshot (quanto più scuri e leggeri diventano i bordi dei bordi). </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> usmRadius</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> Frase codice </span> </td> 
   <td colname="col3"> Sì </td> 
   <td colname="col4"> Influisce sulle dimensioni dei bordi da migliorare o sulla larghezza dei cerchi dei bordi che diventano, in modo che un raggio più piccolo esalti i dettagli di scala minore. Valori di raggio più elevati possono causare aloni ai bordi. I dettagli fini necessitano di un raggio più piccolo, poiché i minimi dettagli delle stesse dimensioni o inferiori al raggio vengono persi. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> usmThreshold</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> Frase codice </span> </td> 
   <td colname="col3"> Sì </td> 
   <td colname="col4"> Controlla la variazione minima di luminosità da rendere più nitida o la distanza tra i valori tonali adiacenti prima del funzionamento del filtro. Questa impostazione consente di rendere più nitidi i bordi mentre altri bordi più sottili non vengono toccati. L'intervallo di soglia consentito da 0 a 255. </td> 
  </tr> 
 </tbody> 
</table>

**Output (createVignettePublishFormatReturn)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| ` *`vignetteFormatHandle`*` | `xsd:string` | Sì | L&#39;handle del formato di vignettatura creato. |

## Esempi {#section-0564752d439642b9bb8de2903db6de1e}

Questo codice crea il formato di pubblicazione della vignettatura. La richiesta di creazione specifica un nome, una larghezza e un&#39;altezza di destinazione e altri valori richiesti.

**Request Contents (Richiesta contenuto)**

```java
<createVignettePublishFormatParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|21</companyHandle>
   <name>APIcreateVignettePublishFormat1</name>
   <targetWidth>1200</<targetWidth>
   <targetHeight>800</targetHeight>
   <createPyramid>true</createPyramid>
   <thumbWidth>400</thumbWidth>
   <saveAsVersion>0</saveAsVersion>
   <sizeSuffixSeparator>-</sizeSuffixSeparator>
   <sharpen>50</sharpen>
   <usmAmount>230.0</usmAmount>
   <usmRadius>1.1</usmRadius>
   <usmThreshold>130</usmThreshold>
</createVignettePublishFormatParam>
```

**Risposta**

```java
<createVignettePublishFormatReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <vignetteFormatHandle>v|21|282</vignetteFormatHandle>
</createVignettePublishFormatReturn>
```

