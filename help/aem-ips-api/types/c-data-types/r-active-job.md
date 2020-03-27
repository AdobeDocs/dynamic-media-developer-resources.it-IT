---
description: Un processo che viene eseguito su un server. Inoltre, si tratta di un'istanza di un processo pianificato.
seo-description: Un processo che viene eseguito su un server. Inoltre, si tratta di un'istanza di un processo pianificato.
seo-title: ActiveJob
solution: Experience Manager
title: ActiveJob
topic: Scene7 Image Production System API
uuid: d7120a88-6f3e-4844-aafa-83d419470fad
translation-type: tm+mt
source-git-commit: 26fb6212c3106deb7b088020d9f2993e40dec20b

---


# ActiveJob{#activejob}

Un processo che viene eseguito su un server. Inoltre, si tratta di un&#39;istanza di un processo pianificato.

I posti di lavoro esistono in 3 stati:

* Pianificazione dell&#39;esecuzione.
* Attualmente in esecuzione.
* Esecuzione completata (con informazioni già scritte in un registro processi).

Specificate un valore per il tipo di processo da restituire. È possibile restituire i seguenti processi:

* `imageServingPublishJob`
* `imageRenderingPublishJob`
* `videoPublishJob`
* `serverDirectoryPublish`
* `JobUploadDirectoryJob`
* `uploadUrlsJob`

## Parametri {#section-6590fe864a434000822b9ec384784512}

<table id="table_1C4DDAB4EB1341FDA92B6F14E0132F75"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Nome </th> 
   <th colname="col2" class="entry"> Tipo </th> 
   <th colname="col3" class="entry"> Descrizione </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> companyHandle</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Gestite l'azienda. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> jobHandle</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Gestite il lavoro. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> name</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Nome univoco per il processo. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> OriginalName</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3">Nome originale del tipo <span class="codeph"> ActiveJob</span> inviato con il processo. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> type</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Scelta dei tipi di processo restituiti dal sistema. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> state</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Scelta degli stati di processo attivi restituiti dal sistema. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> submitUserEmail <span class="varname"></span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> indirizzo e-mail dell’utente che ha pianificato il processo. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> locale</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3">Le impostazioni internazionali per i dettagli del registro dei processi e la localizzazione delle e-mail. <p>Specificate le impostazioni internazionali come <span class="codeph"> &lt;codice_lingua&gt;[-&lt;codice_paese&gt;]</span>, dove il codice della lingua è un codice di due lettere minuscoli, come specificato dallo standard ISO-639, e il codice del paese facoltativo è un codice di due lettere maiuscole, come specificato dallo standard ISO-3166. Ad esempio, la stringa per l'inglese (Stati Uniti) è: <span class="codeph"> en-US</span>. </p></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> descrizione</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3">Descrizione del processo specificata originariamente in <span class="codeph"> submitJob</span>. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> serverName</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Nome del server che esegue il processo. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> startDate</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:dateTime</span> </td> 
   <td colname="col3"> Data, ora e fuso orario per il processo attivo. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> totalSize</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Dimensione totale del processo attivo. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> progress</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:int</span> </td> 
   <td colname="col3"> Avanzamento del processo (ovvero, la vicinanza del processo al completamento). </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> progressMessage</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:int</span> </td> 
   <td colname="col3"> Un messaggio di testo che descrive l’avanzamento del processo. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> lastProgressUpdate <span class="varname"></span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:dateTime</span> </td> 
   <td colname="col3"> Data, ora e fuso orario dell’ultimo aggiornamento in corso. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> taskProgressArray</span></span> </td> 
   <td colname="col2"> <span class="codeph"> tipi:TaskProgressArray</span> </td> 
   <td colname="col3"> Informazioni di avanzamento asincrone dell'attività. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> imageServingPublishJob <span class="varname"></span></span> </td> 
   <td colname="col2"> <span class="codeph"> tipi:ImageServingPublishJob</span> </td> 
   <td colname="col3"> Dettagli del processo per un processo di pubblicazione di Image Server. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> imageServingRenderJob <span class="varname"></span></span> </td> 
   <td colname="col2"> <span class="codeph"> tipi:ImageServingRenderJob</span> </td> 
   <td colname="col3"> Dettagli del processo per un processo di pubblicazione di rendering di immagini. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> videoPublishJob</span></span> </td> 
   <td colname="col2"> <span class="codeph"> tipi:VideoPublishJob</span> </td> 
   <td colname="col3"> Dettagli del processo per un processo di pubblicazione video. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> serverDirectoryPublishJob <span class="varname"></span></span> </td> 
   <td colname="col2"> <span class="codeph"> tipi:ImageServingPublishJob</span> </td> 
   <td colname="col3"> Dettagli del processo per un processo di pubblicazione della directory del server. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> uploadUrlsJob</span></span> </td> 
   <td colname="col2"> <span class="codeph"> tipi:UploadUrlsJob</span> </td> 
   <td colname="col3"> Dettagli processo per un processo URL di caricamento. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> ripPdfsJob</span></span> </td> 
   <td colname="col2"> <span class="codeph"> tipi:RipPdfsJob</span> </td> 
   <td colname="col3"></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> optimizeImagesJob</span></span> </td> 
   <td colname="col2"> <span class="codeph"> tipi:OptimizeImagesJob</span> </td> 
   <td colname="col3"></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> reprocessAssetsJob</span></span> </td> 
   <td colname="col2"> <span class="codeph"> tipi:ReprocessAssetsJob</span> </td> 
   <td colname="col3"></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> uploadPostJob</span></span> </td> 
   <td colname="col2"> <span class="codeph"> tipi:UploadPostJob</span> </td> 
   <td colname="col3"> Dettagli processo per tracciamento del caricamento del desktop. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> exportJob</span></span> </td> 
   <td colname="col2"> <span class="codeph"> tipi:ExportJob</span> </td> 
   <td colname="col3">Consenti esportazione autorizzata di file caricati in precedenza. Consultate Processo <a href="https://marketing.adobe.com/resources/help/en_US/s7/ips_api/types/r_exportjob.html" format="http" scope="external"></a>di esportazione. </td> 
  </tr> 
 </tbody> 
</table>

