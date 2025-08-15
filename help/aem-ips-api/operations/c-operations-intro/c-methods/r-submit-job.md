---
description: Invia un processo al sistema.
solution: Experience Manager
title: submitJob
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: b1dc7a0e-da9a-4086-822b-5274bd62eadf
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '407'
ht-degree: 6%

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
   <td colname="col1"> <span class="codeph"> <span class="varname"> companyHandle</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Sì </td> 
   <td colname="col4"> <p>Gestore azienda. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> userHandle</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> No </td> 
   <td colname="col4"> <p>Gestisci per l’utente che ha inviato il processo. </p> <p> <p>Nota: il sistema invia un'e-mail all'utente specificato da <span class="codeph"> userHandle</span>. Se <span class="codeph"> userHandle</span> non viene fornito, la persona che ha inviato il processo riceve le e-mail. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> jobName</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Sì </td> 
   <td colname="col4"> <p>Nome processo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> impostazioni locali</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> No </td> 
   <td colname="col4"> <p>La lingua utilizzata per i dettagli del registro di processo e la localizzazione delle e-mail. </p> <p>Le impostazioni internazionali sono specificate come <span class="codeph"> &lt;codice_lingua&gt;</span> e <span class="codeph"> [&lt;codice_paese&gt;]</span>, dove il codice della lingua è un codice a due lettere minuscole come specificato dallo standard ISO-639 e il codice paese facoltativo è un codice a due lettere maiuscole come specificato dallo standard ISO-3166. Ad esempio, la stringa della lingua inglese (Stati Uniti) sarà: en-US. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> execTime</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:dateTime</span> </td> 
   <td colname="col3"> No </td> 
   <td colname="col4"> <p>Data e ora di esecuzione del processo. </p> <p>Nota: specifica il fuso orario con la richiesta. I fusi orari vengono regolati in base al fuso orario del server IPS di destinazione. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> execSchedule</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> No </td> 
   <td colname="col4"> <p>Determina quando eseguire il processo. </p> <p> Può essere una stringa cron<span class="codeph"> </span> che esegue il processo su base periodica. </p> <p>La pianificazione è sempre relativa al fuso orario locale del server. Consulta la documentazione IPS per il formato di pianificazione personalizzato. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> descrizione</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> No </td> 
   <td colname="col4"> <p>Descrizione del processo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> processo di esportazione</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> tipi:ExportJob</span> </td> 
   <td colname="col3"> No </td> 
   <td colname="col4"> <p>Esporta i file caricati in precedenza. </p> <p>Vedere <a href="../../../types/c-data-types/r-exportjob.md#reference-1ce423f7b2d54507b90b67233c588665" format="dita" scope="local"> ExportJob</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> imageServingPublishJob</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> tipi:ImageServingPublishJob</span> </td> 
   <td colname="col3"> No </td> 
   <td colname="col4"> <p>Dettagli di un processo di pubblicazione di server immagini. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> imageRenderingPublishJob</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> tipi:ImageRenderingPublishJob</span> </td> 
   <td colname="col3"> No </td> 
   <td colname="col4"> <p>Dettagli per un processo di pubblicazione di rendering immagini. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> videoPublishJob</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> tipi:VideoPublishJob</span> </td> 
   <td colname="col3"> No </td> 
   <td colname="col4"> <p>Dettagli di un processo di pubblicazione video. </p> <p>Vedi <a href="../../../types/c-data-types/r-video-publish-job.md#reference-e99e60d38fe94a07914eefcd7beef2e0" format="dita" scope="local"> VideoPublishJob</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> serverDirectoryPublishJob</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> tipi:ServerDirectoryPublishJob</span> </td> 
   <td colname="col3"> No </td> 
   <td colname="col4"> <p>Dettagli di un processo di pubblicazione di directory server. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> uploadDirectoryJob</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> tipi:UploadDirectoryJob</span> </td> 
   <td colname="col3"> No </td> 
   <td colname="col4"> <p>Dettagli di un processo di caricamento directory. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> uploadUrlsJob</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> tipi:UploadUrlsJob</span> </td> 
   <td colname="col3"> No </td> 
   <td colname="col4"> <p>Dettagli di un processo URL di caricamento. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> optimizeImagesJob</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> tipi:OptimizeImagesJob</span> </td> 
   <td colname="col3"> No </td> 
   <td colname="col4"> <p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> ripPdfsJob</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> tipi:RipPdfsJob</span> </td> 
   <td colname="col3"> No </td> 
   <td colname="col4"> <p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> rielabora AssetsJob</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> tipi:ReprocessAssetsJob</span> </td> 
   <td colname="col3"> No </td> 
   <td colname="col4"> <p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> processo di generazione automatizzato</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> tipi:AutomatedSetGenerationJob</span> </td> 
   <td colname="col3"> No </td> 
   <td colname="col4"> <p>Elabora un elenco di risorse in set utilizzando gli script per set automatizzati. </p> <p>Vedere <a href="../../../types/c-data-types/r-automated-set-generation-job.md#reference-ab0b3c5408eb41b98c49898b2197cf5a" format="dita" scope="local"> AutomatedSetGenerationJob</a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Output (submitJobReturn)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| jobHandle | `xsd:string` | Sì | Handle di processo. |

## Esempi {#section-40ac77d14adf4588ba2575be6879b2d2}

In questo esempio di codice viene inviato un processo di pubblicazione da server immagini a IPS e viene restituito un handle di processo. Scegliere un solo tipo di job nella richiesta. Poiché `userHandle` è stato omesso, le notifiche e-mail vengono inviate all&#39;utente che ha inviato il processo. Il processo di esempio viene eseguito immediatamente perché `execTime` e `execSchedule` sono stati omessi.

**Richiesta**

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

È possibile specificare al massimo uno di `execTime` e `execSchedule`. Se nessuno dei due viene passato, il processo viene eseguito immediatamente. È possibile utilizzare solo una delle seguenti opzioni:

* `imageServingPublishJob`
* `imageRenderingPublishJob`
* `videoPublishJob`
* `serverDirectoryPublishJob`
* `uploadDirectoryJob`
* `uploadUrlsJob`
