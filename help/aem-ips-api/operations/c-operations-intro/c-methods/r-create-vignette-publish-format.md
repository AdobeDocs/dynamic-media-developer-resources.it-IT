---
description: Crea un nuovo formato di pubblicazione per una vignetta.
solution: Experience Manager
title: createVignettePublishFormat
feature: Dynamic Media Classic, SDK/API
role: Sviluppatore,Amministratore
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '525'
ht-degree: 14%

---


# createVignettePublishFormat{#createvignettepublishformat}

Crea un nuovo formato di pubblicazione per una vignetta.

I formati delle vignette specificano le dimensioni delle vignette pubblicate e le relative miniature, nonché i livelli di zoom, i parametri di nitidezza e la versione del formato del file per le vignette prodotte da vignette primarie pubblicate su un server Image Rendering da IPS.

Le nuove versioni del server Image Rendering supportano le vignette piramidali, eliminando la necessità di definire formati di vignetta specifici per la pubblicazione.

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
   <td colname="col4"> Gestisci l'azienda a cui appartiene la vignetta. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> name</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> Frase di codice  </span> </td> 
   <td colname="col3"> Sì </td> 
   <td colname="col4"> Nome per identificare il formato di pubblicazione della vignetta. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> targetWidth</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> Frase di codice  </span> </td> 
   <td colname="col3"> Sì </td> 
   <td colname="col4"> <p>Specifica la larghezza di destinazione della visualizzazione della vignetta risultante in pixel. </p> <p>Usa zero in modo che la vignetta di output abbia le stesse dimensioni della vignetta primaria. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> targetHeight</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> Frase di codice  </span> </td> 
   <td colname="col3"> Sì </td> 
   <td colname="col4"> Crea una vignettatura piramidale ottimizzata per lo zoom sul server Image Rendering. Partendo dalla dimensione massima impostata mediante i campi Dimensione vignettatura destinazione, vengono create visualizzazioni con diverse dimensioni in un singolo file di output vignettatura. Ciascuna dimensione di visualizzazione successiva è dimezzata fino ad arrivare a valori di larghezza e altezza che rientrano in 128x128 pixel. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> createPyramid</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> Frase di codice  </span> </td> 
   <td colname="col3"> Sì </td> 
   <td colname="col4"> Specifica la larghezza di ogni miniatura risultante in pixel. Questa impostazione è facoltativa. Lascia come zero per nessun file di miniatura. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> thumbWidth</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> Frase di codice  </span> </td> 
   <td colname="col3"> Sì </td> 
   <td colname="col4"> Specifica il formato di file per le vignette pubblicate. Data una nuova versione di Image Authoring e una versione precedente di Image Rendering Server, è necessario specificare una versione di vignetta leggibile dal server ImageRendering. Se si specifica una versione successiva, il server Image Rendering non è in grado di leggere le vignette pubblicate. Imposta su zero per pubblicare le vignette nella versione più recente. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> saveAsVersion</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> Frase di codice  </span> </td> 
   <td colname="col3"> Sì </td> 
   <td colname="col4"> Specifica il carattere che separa il nome della vignetta e il suffisso che ne indica la larghezza. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> sizeSuffixSeparator</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> Frase di codice  </span> </td> 
   <td colname="col3"> Sì </td> 
   <td colname="col4"> Specifica il carattere che separa il nome della vignetta e il suffisso che ne indica la larghezza. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> affilare</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> Frase di codice  </span> </td> 
   <td colname="col3"> No </td> 
   <td colname="col4"> Applica la nitidezza all'immagine della vista principale per ogni dimensione della vignetta puvlish La nitidezza può compensare la sfocatura quando i vignettatori sono scalati. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> usmAmount</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> Frase di codice  </span> </td> 
   <td colname="col3"> Sì </td> 
   <td colname="col4"> La funzione di mascheramento intelligente digitale è un modo flessibile e potente per aumentare la nitidezza, specialmente nelle immagini scansionate. Questo controlla la grandezza di ogni sovrimpressione (quanto più scura e leggera diventano i bordi dei bordi). </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> usmRadius</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> Frase di codice  </span> </td> 
   <td colname="col3"> Sì </td> 
   <td colname="col4"> Influisce sulle dimensioni dei bordi da migliorare o sulla larghezza dei bordi, in modo che un raggio più piccolo migliori i dettagli di scala più piccola. Valori di raggio più elevati possono causare alone ai bordi. La precisione dei dettagli ha bisogno di un raggio più piccolo, dato che i minimi dettagli delle stesse dimensioni o minori del raggio vengono persi. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> usmThreshold</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> Frase di codice  </span> </td> 
   <td colname="col3"> Sì </td> 
   <td colname="col4"> Controlla la variazione minima di luminosità da rendere più nitida o la distanza di separazione dei valori tonali adiacenti prima che il filtro funzioni. Questa impostazione può rendere più nitidi i bordi più pronunciati lasciando intatti i bordi più sottili. L'intervallo di soglia consentito da 0 a 255. </td> 
  </tr> 
 </tbody> 
</table>

**Output (createVignettePublishFormatReturn)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| `*`vignetteFormatHandle`*` | `xsd:string` | Sì | Il punto di manipolazione del formato di vignetta creato. |

## Esempi {#section-0564752d439642b9bb8de2903db6de1e}

Questo codice crea il formato di pubblicazione della vignetta. La richiesta di creazione specifica un nome, una larghezza e un&#39;altezza della destinazione e altri valori richiesti.

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

