---
description: Invia un processo al sistema.
seo-description: Invia un processo al sistema.
seo-title: submitJob
solution: Experience Manager
title: submitJob
topic: Scene7 Image Production System API
uuid: d3a83b59-bcd7-4ae9-b1ee-e515fc3c9261
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# submitJob{#submitjob}

Invia un processo al sistema.

Sintassi

## Tipi di utenti autorizzati {#section-eb7024277bec43c79e03f396205be16f}

* `IpsUser`
* `IpsAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parametri {#section-31a07dbccf964850883e817384499459}

**Input (submitJobParam)**

<table id="table_9CB1F668E036422E8CE4E0BBA42EC44C"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Nome </p> </th> 
   <th colname="col2" class="entry"> <p>Tipo </p> </th> 
   <th colname="col3" class="entry"> <p>Obbligatorio </p> </th> 
   <th colname="col4" class="entry"> <p>Descrizione </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> companyHandle</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Sì </td> 
   <td colname="col4"> <p>Maniglia aziendale. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> userHandle</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> No </td> 
   <td colname="col4"> <p>Gestite l’utente che ha inviato il processo. </p> <p> <p>Nota: Il sistema invia un messaggio e-mail all'utente specificato da <span class="codeph"> userHandle</span>. Se <span class="codeph"> userHandle</span> non viene fornito, la persona che ha inviato il processo riceve i messaggi e-mail. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> jobName</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Sì </td> 
   <td colname="col4"> <p>Nome processo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> locale</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> No </td> 
   <td colname="col4"> <p>Le impostazioni internazionali utilizzate per i dettagli del registro dei processi e la localizzazione delle e-mail. </p> <p>Le impostazioni internazionali sono specificate come <span class="codeph"> &lt;codice_lingua&gt;</span> e <span class="codeph"> [&lt;codice_paese&gt;]</span>, dove il codice della lingua è un codice di due lettere minuscoli, come specificato dallo standard ISO-639, e il codice del paese opzionale è un codice di due lettere maiuscole, come specificato dallo standard ISO-3166. Ad esempio, la stringa per l'inglese (Stati Uniti) è: it-IT. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> execTime</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:dateTime</span> </td> 
   <td colname="col3"> No </td> 
   <td colname="col4"> <p>Data e ora di esecuzione del processo. </p> <p>Nota:  Specifica il fuso orario con la richiesta. I fusi orari vengono regolati in base al fuso orario del server IPS di destinazione. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> execSchedule</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> No </td> 
   <td colname="col4"> <p>Determina quando eseguire il processo. </p> <p> Può essere una stringa <span class="codeph"> cron</span> che esegue il processo su base periodica. </p> <p>La pianificazione è sempre relativa al fuso orario locale del server. Consultate la documentazione IPS per il formato di pianificazione personalizzato. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> descrizione</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> No </td> 
   <td colname="col4"> <p>Descrizione del processo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> exportJob</span></span> </td> 
   <td colname="col2"> <span class="codeph"> tipi:ExportJob</span> </td> 
   <td colname="col3"> No </td> 
   <td colname="col4"> <p>Esportate i file caricati in precedenza. </p> <p>Consultate <a href="../../../types/c-data-types/r-exportjob.md#reference-1ce423f7b2d54507b90b67233c588665" format="dita" scope="local"> Processo</a>di esportazione. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> imageServingPublishJob <span class="varname"></span></span> </td> 
   <td colname="col2"> <span class="codeph"> tipi:ImageServingPublishJob</span> </td> 
   <td colname="col3"> No </td> 
   <td colname="col4"> <p>Dettagli per un processo di pubblicazione di Image Server. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> imageRenderingPublishJob <span class="varname"></span></span> </td> 
   <td colname="col2"> <span class="codeph"> tipi:ImageRenderingPublishJob</span> </td> 
   <td colname="col3"> No </td> 
   <td colname="col4"> <p>Dettagli per un processo di pubblicazione di rendering delle immagini. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> videoPublishJob</span></span> </td> 
   <td colname="col2"> <span class="codeph"> tipi:VideoPublishJob</span> </td> 
   <td colname="col3"> No </td> 
   <td colname="col4"> <p>Dettagli per un processo di pubblicazione video. </p> <p>Consultate <a href="../../../types/c-data-types/r-video-publish-job.md#reference-e99e60d38fe94a07914eefcd7beef2e0" format="dita" scope="local"> VideoPublishJob</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> serverDirectoryPublishJob <span class="varname"></span></span> </td> 
   <td colname="col2"> <span class="codeph"> tipi:ServerDirectoryPublishJob</span> </td> 
   <td colname="col3"> No </td> 
   <td colname="col4"> <p>Dettagli per un processo di pubblicazione di una directory server. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> uploadDirectoryJob</span></span> </td> 
   <td colname="col2"> <span class="codeph"> tipi:UploadDirectoryJob</span> </td> 
   <td colname="col3"> No </td> 
   <td colname="col4"> <p>Dettagli per un processo della directory di caricamento. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> uploadUrlsJob</span></span> </td> 
   <td colname="col2"> <span class="codeph"> tipi:UploadUrlsJob</span> </td> 
   <td colname="col3"> No </td> 
   <td colname="col4"> <p>Dettagli per un processo URL di caricamento. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> optimizeImagesJob</span></span> </td> 
   <td colname="col2"> <span class="codeph"> tipi:OptimizeImagesJob</span> </td> 
   <td colname="col3"> No </td> 
   <td colname="col4"> <p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> ripPdfsJob</span></span> </td> 
   <td colname="col2"> <span class="codeph"> tipi:RipPdfsJob</span> </td> 
   <td colname="col3"> No </td> 
   <td colname="col4"> <p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> reprocessAssetsJob</span></span> </td> 
   <td colname="col2"> <span class="codeph"> tipi:ReprocessAssetsJob</span> </td> 
   <td colname="col3"> No </td> 
   <td colname="col4"> <p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> automatizzatoSetGenerationJob</span></span> </td> 
   <td colname="col2"> <span class="codeph"> tipi:AutomatedSetGenerationJob</span> </td> 
   <td colname="col3"> No </td> 
   <td colname="col4"> <p>Elabora un elenco di risorse in set utilizzando gli script di set automatizzati. </p> <p>Vedere <a href="../../../types/c-data-types/r-automated-set-generation-job.md#reference-ab0b3c5408eb41b98c49898b2197cf5a" format="dita" scope="local"> AutomatedSetGenerationJob</a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Output (submitJobReturn)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| ` *`jobHandle`*` | `xsd:string` | Sì | Handle processo. |

## Esempi {#section-40ac77d14adf4588ba2575be6879b2d2}

Questo esempio di codice invia un processo di pubblicazione di immagini in IPS e restituisce un handle di processo. Scegliete solo un tipo di processo nella richiesta. Poiché `userHandle` è stato omesso, le notifiche e-mail vengono inviate all’utente che ha inviato il processo. Questo processo di esempio viene eseguito immediatamente perché `execTime` e `execSchedule` sono stati omessi.

**Request Contents (Richiesta contenuto)**

```java
<submitJobParam xmlns="http://www.scene7.com/IpsApi/xsd">
   <companyHandle>47</companyHandle>
   <jobName>My Test Job</jobName>
   <imageServingPublishJob>
      <publishType>Full</publishType>
      <emailSetting>Error</emailSetting>
   </imageServingPublishJob>
</submitJobParam>
```

**Risposta**

```java
<submitJobReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <jobHandle>47|My Test Job|</jobHandle>
</submitJobReturn>
```

## Note {#section-0f3078e503a249aeb6f3d662a51f036a}

Potete specificare al massimo uno di `execTime` e `execSchedule`. Se nessuna delle due operazioni viene superata, il processo viene eseguito immediatamente. Potete utilizzare solo una delle seguenti opzioni:

* `imageServingPublishJob`
* `imageRenderingPublishJob`
* `videoPublishJob`
* `serverDirectoryPublishJob`
* `uploadDirectoryJob`
* `uploadUrlsJob`

