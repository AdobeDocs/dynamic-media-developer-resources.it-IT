---
description: Crea un nuovo formato di pubblicazione per una vignettatura.
solution: Experience Manager
title: createVignettePublishFormat
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: d58e1290-8a79-4129-99ce-776b919dea13
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '520'
ht-degree: 4%

---

# createVignettePublishFormat{#createvignettepublishformat}

Crea un nuovo formato di pubblicazione per una vignettatura.

I formati di vignettatura specificano le dimensioni delle vignettature pubblicate e delle relative miniature, nonché i livelli di zoom, i parametri di nitidezza e la versione del formato di file per le vignettature prodotte da vignettature primarie pubblicate su un server Image Rendering da IPS.

Le versioni più recenti del server Image Rendering supportano le vignettature piramidali, eliminando la necessità di definire formati di vignettatura specifici per la pubblicazione.

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
   <td colname="col4"> Gestisci l’azienda a cui appartiene la vignettatura. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> nome</span> </span> </td> 
   <td colname="col2"> Frase codice <span class="codeph"> di </span> </td> 
   <td colname="col3"> Sì </td> 
   <td colname="col4"> Nome per identificare il formato di pubblicazione vignettatura. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> targetWidth</span> </span> </td> 
   <td colname="col2"> Frase codice <span class="codeph"> di </span> </td> 
   <td colname="col3"> Sì </td> 
   <td colname="col4"> <p>Specifica la larghezza di destinazione della visualizzazione vignettatura risultante, in pixel. </p> <p>Utilizzare zero in modo che la vignettatura di output abbia le stesse dimensioni della vignettatura principale. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> targetHeight</span> </span> </td> 
   <td colname="col2"> Frase codice <span class="codeph"> di </span> </td> 
   <td colname="col3"> Sì </td> 
   <td colname="col4"> Crea una vignettatura piramidale ottimizzata per lo zoom sul server Image Rendering. Partendo dalla dimensione massima, impostata dai campi Dimensione vignettatura di destinazione, vengono create visualizzazioni con più dimensioni in un singolo file di output vignettatura. Ogni dimensione di visualizzazione successiva viene dimezzata fino a raggiungere valori di larghezza e altezza compresi tra 128x128 pixel. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> createPyramid</span> </span> </td> 
   <td colname="col2"> Frase codice <span class="codeph"> di </span> </td> 
   <td colname="col3"> Sì </td> 
   <td colname="col4"> Specifica la larghezza in pixel di ciascuna miniatura risultante. Questa impostazione è facoltativa. Lascia zero per non creare alcun file di miniatura. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> larghezza miniature</span> </span> </td> 
   <td colname="col2"> Frase codice <span class="codeph"> di </span> </td> 
   <td colname="col3"> Sì </td> 
   <td colname="col4"> Specifica il formato di file per le vignettature pubblicate. Considerata una nuova versione di Image Authoring e una precedente versione di Image Rendering Server, è necessario specificare una versione di vignettatura che il server ImageRendering possa leggere. Se specificate una versione successiva, il server Image Rendering non sarà in grado di leggere le vignettature pubblicate. Impostate questo valore su zero per pubblicare le vignettature all'ultima versione. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> saveAsVersion</span> </span> </td> 
   <td colname="col2"> Frase codice <span class="codeph"> di </span> </td> 
   <td colname="col3"> Sì </td> 
   <td colname="col4"> Specifica il carattere che separa il nome della vignettatura e il suffisso che ne indica la larghezza. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> sizeSuffixSeparator</span> </span> </td> 
   <td colname="col2"> Frase codice <span class="codeph"> di </span> </td> 
   <td colname="col3"> Sì </td> 
   <td colname="col4"> Specifica il carattere che separa il nome della vignettatura e il suffisso che ne indica la larghezza. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> nitidezza</span> </span> </td> 
   <td colname="col2"> Frase codice <span class="codeph"> di </span> </td> 
   <td colname="col3"> No </td> 
   <td colname="col4"> Aumenta la nitidezza dell'immagine di visualizzazione principale per ogni dimensione di vignettatura con effetto di contrasto in grado di compensare l'effetto sfuocato quando i vignettatori vengono ridimensionati. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> usmAmount</span> </span> </td> 
   <td colname="col2"> Frase codice <span class="codeph"> di </span> </td> 
   <td colname="col3"> Sì </td> 
   <td colname="col4"> Il mascheramento digitale è un modo flessibile e potente per aumentare la nitidezza, soprattutto nelle immagini digitalizzate. Questa opzione consente di controllare la grandezza di ciascuna sovrascrittura (la quantità di luce e di oscurità che i bordi diventano). </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> usmRadius</span> </span> </td> 
   <td colname="col2"> Frase codice <span class="codeph"> di </span> </td> 
   <td colname="col3"> Sì </td> 
   <td colname="col4"> Influisce sulla dimensione degli spigoli da aumentare o sulla larghezza dei bordi, quindi un raggio più piccolo migliora i dettagli di scala più piccola. Valori di raggio più alti possono causare aloni sui bordi. I dettagli fini richiedono un raggio più piccolo, in quanto vengono persi piccoli dettagli della stessa dimensione o più piccoli del raggio. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> usmThreshold</span> </span> </td> 
   <td colname="col2"> Frase codice <span class="codeph"> di </span> </td> 
   <td colname="col3"> Sì </td> 
   <td colname="col4"> Controlla la variazione minima della luminosità da rendere più nitida o la distanza tra i valori tonali adiacenti prima che il filtro funzioni. Questa impostazione consente di rendere più nitidi i bordi pronunciati lasciando invariati quelli più sottili. L'intervallo consentito di soglia compreso tra 0 e 255. </td> 
  </tr> 
 </tbody> 
</table>

**Output (createVignettePublishFormatReturn)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| vignetteFormatHandle | `xsd:string` | Sì | Handle del formato di vignettatura creato. |

## Esempi {#section-0564752d439642b9bb8de2903db6de1e}

Questo codice crea il formato di pubblicazione vignettatura. La richiesta di creazione specifica un nome, una larghezza e un&#39;altezza di destinazione e altri valori richiesti.

**Richiesta**

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
