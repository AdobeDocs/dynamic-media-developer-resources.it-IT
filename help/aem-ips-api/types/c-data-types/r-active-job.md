---
title: Processo attivo
description: Processo eseguito su un server. Inoltre, è un’istanza di un processo pianificato.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 3d878207-99e4-4c75-ab12-b38a37c82fb7
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '375'
ht-degree: 1%

---

# [!DNL ActiveJob]{#activejob}

Processo eseguito su un server. Inoltre, è un’istanza di un processo pianificato.

I processi sono disponibili in tre stati:

* Esecuzione pianificata.
* Attualmente in esecuzione.
* Esecuzione completata (e sono già state scritte informazioni in un registro di processo).

Per restituire il tipo di processo, specificare un valore per il tipo di processo. È possibile restituire i seguenti processi:

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
   <td colname="col1"> <span class="codeph"> <span class="varname"> companyHandle</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:stringa</span> </td> 
   <td colname="col3"> Gestire l'azienda. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> jobHandle</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:stringa</span> </td> 
   <td colname="col3"> Gestire il processo. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> nome</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:stringa</span> </td> 
   <td colname="col3"> Nome univoco del processo. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> originalName</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:stringa</span> </td> 
   <td colname="col3">Nome originale del <span class="codeph"> Processo attivo</span> tipo inviato con il processo. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> tipo</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:stringa</span> </td> 
   <td colname="col3"> Scelta dei tipi di processo restituiti dal sistema. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> stato</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:stringa</span> </td> 
   <td colname="col3"> Scelta degli stati di processo attivi restituiti dal sistema. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> submitUserEmail</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:stringa</span> </td> 
   <td colname="col3"> indirizzo e-mail dell’utente che ha pianificato il processo. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> locale</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:stringa</span> </td> 
   <td colname="col3">Impostazioni locali per i dettagli del registro processo e la localizzazione e-mail. <p>Specifica impostazioni internazionali come <span class="codeph"> &lt;language_code&gt;[-&lt;country_code&gt;]</span>, dove il codice della lingua è un codice a due lettere minuscole come specificato dallo standard ISO-639 e il codice facoltativo del paese è un codice a due lettere maiuscole come specificato dallo standard ISO-3166. Ad esempio, la stringa delle impostazioni internazionali per l'inglese (Stati Uniti) sarà: <span class="codeph"> en-US</span>. </p></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> descrizione</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:stringa</span> </td> 
   <td colname="col3">Descrizione del processo specificata originariamente in <span class="codeph"> submitJob</span>. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> serverName</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:stringa</span> </td> 
   <td colname="col3"> Nome del server che esegue il processo. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> startDate</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:dateTime</span> </td> 
   <td colname="col3"> Data, ora e fuso orario del processo attivo. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> totalSize</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:stringa</span> </td> 
   <td colname="col3"> Dimensione totale del processo attivo. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> avanzamento</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:int</span> </td> 
   <td colname="col3"> Avanzamento del processo (ovvero quanto è vicino il completamento del processo). </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> progressMessage</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:int</span> </td> 
   <td colname="col3"> Un messaggio di testo che descrive l’avanzamento del processo. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> lastProgressUpdate</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:dateTime</span> </td> 
   <td colname="col3"> Data, ora e fuso orario dell’ultimo aggiornamento di avanzamento. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> taskProgressArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> tipi:TaskProgressArray</span> </td> 
   <td colname="col3"> Informazioni sull'avanzamento delle attività asincrone. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> imageServingPublishJob</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> tipi:ImageServingPublishJob</span> </td> 
   <td colname="col3"> Dettagli di un processo di pubblicazione di image server. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> imageServingRenderJob</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> tipi:ImageServingRenderJob</span> </td> 
   <td colname="col3"> Dettagli di un processo di pubblicazione di rendering immagini. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> videoPublishJob</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> tipi:VideoPublishJob</span> </td> 
   <td colname="col3"> Dettagli di un processo di pubblicazione video. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> serverDirectoryPublishJob</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> tipi:ImageServingPublishJob</span> </td> 
   <td colname="col3"> Dettagli del processo per un processo di pubblicazione della directory del server. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> uploadUrlsJob</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> tipi:UploadUrlsJob</span> </td> 
   <td colname="col3"> Dettagli di un processo di caricamento URL. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> ripPdfsJob</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> tipi:RipPdfsJob</span> </td> 
   <td colname="col3"></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> optimizeImagesJob</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> tipi:OptimizeImagesJob</span> </td> 
   <td colname="col3"></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> reprocessAssetsJob</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> tipi:RielaboraProcessoRisorse</span> </td> 
   <td colname="col3"></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> uploadPostJob</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> tipi:UploadPostJob</span> </td> 
   <td colname="col3"> Dettagli del processo, tracciamento del caricamento del desktop. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> exportJob</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> tipi:ExportJob</span> </td> 
   <td colname="col3">Consente l’esportazione autorizzata di file caricati in precedenza. Consulta <a href="https://experienceleague.adobe.com/docs/dynamic-media-developer-resources/image-production-api/data-types/r-exportjob.html" format="http" scope="external"> Processo di esportazione</a>. </td> 
  </tr> 
 </tbody> 
</table>
