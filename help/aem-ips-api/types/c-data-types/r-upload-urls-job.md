---
description: Carica gli URL dal percorso in cui desiderate ottenere i file.
seo-description: Carica gli URL dal percorso in cui desiderate ottenere i file.
seo-title: UploadUrlsJob
solution: Experience Manager
title: UploadUrlsJob
topic: Scene7 Image Production System API
uuid: 6140e969-bf61-4b62-9a60-29609626b0b4
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '453'
ht-degree: 1%

---


# UploadUrlsJob{#uploadurlsjob}

Carica gli URL dal percorso in cui desiderate ottenere i file.

Sintassi

## Parametri {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

<table id="table_04100BB8ABD84EF68B0A7CE3AD946414"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Nome </th> 
   <th colname="col2" class="entry"> Tipo </th> 
   <th colname="col3" class="entry"> Descrizione </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> autoColorCropOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> tipi:AutoColorCropOptions</span> </td> 
   <td colname="col3"> Opzioni per ritagli automatici di immagini in base al colore. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> autoSetCreationOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> tipi:AutoSetCreationOptions</span> </td> 
   <td colname="col3"> Array di script di generazione di set automatici da applicare ai file caricati. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> autoTransparentCropOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> tipi:AutoTransparentCropOptions</span> </td> 
   <td colname="col3"> Rimuove lo spazio bianco dai bordi delle immagini, in base alla trasparenza. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> createMask</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> Se creare una maschera. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> colorManagementOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> tipi:ColorManagementOptions</span> </td> 
   <td colname="col3"> Opzioni che potete specificare durante un caricamento. Il set influisce sulla modalità di gestione del colore per il caricamento. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> emailSetting</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Scelta delle impostazioni e-mail. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> IllustratorOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> tipi:IllustratorOptions</span> </td> 
   <td colname="col3"> Opzioni per caricare  file Illustrator sul server immagini. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> inDesignOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> tipi:InDesignOptions</span> </td> 
   <td colname="col3"> Opzioni per caricare  file InDesign sul server. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> knockoutBackground</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> tipi:KnockoutBackgroundOptions</span> </td> 
   <td colname="col3">Mascherare lo sfondo per le immagini selezionate. Questo consente di sovrapporle ad altri livelli con una trasparenza all’esterno dell’immagine oggetto. Facoltativo. Vedere<a href="../../types/c-data-types/r-knockout-background-options.md#reference-9196371848964d91842b337640791c9c" format="dita" scope="local"> KnockoutBackgroundOptions</a>. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> manualCropOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> tipi:ManualCropOptions</span> </td> 
   <td colname="col3"> Opzioni per ritagli manuali di immagini. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> mediaOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> tipi:MediaOptions</span> </td> 
   <td colname="col3">Opzioni che consentono di impostare una miniatura del video. Vedere <a href="../../types/c-data-types/r-media-options.md#reference-18618fc6803a4b6e994bbb48eba93b5b" format="dita" scope="local"> MediaOptions</a>. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> numUrls</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:int</span> </td> 
   <td colname="col3">Restituisce il numero di URL inviati in un processo. Utilizzata da <a href="../../operations/c-operations-intro/c-methods/r-get-active-jobs.md#reference-67483cbd71d04042b48434d886e8a7a0" format="dita" scope="local"> getActiveJobs</a> e <a href="../../operations/c-operations-intro/c-methods/r-get-scheduled-jobs.md#reference-2bab1861325f4bff84c879d1efa9146e" format="dita" scope="local"> getScheduledJobs</a>. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> overwrite</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> Se sovrascrivere o meno i file durante il caricamento. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> pdfOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> tipi:PDFOptions</span> </td> 
   <td colname="col3"> Opzioni per caricare i file PDF sul server immagini. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> photoshopOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> tipi:PhotoshopOptions</span> </td> 
   <td colname="col3"> Opzioni per caricare file Photoshop sul server immagini. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> postHttpUrl</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> L’URL in cui vengono caricati i file. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> postImageRenderingPublishJob</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> tipi:ImageRendingPublishJob</span> </td> 
   <td colname="col3"> Dettagli per un processo di pubblicazione di rendering immagine che viene eseguito al termine del caricamento. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> postImageServingPublishJob</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> tipi:ImageServingPublishJob</span> </td> 
   <td colname="col3"> Tutte le opzioni del supporto. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> postScriptOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> tipi:PostScriptOptions</span> </td> 
   <td colname="col3"> Opzioni per caricare i file PostScript sul server immagini. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> postVideoPublishJob</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> tipi:VideoPublishJob</span> </td> 
   <td colname="col3"> Dettagli per un processo di pubblicazione video eseguito al termine del caricamento. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> preserveCrop</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> Controlla la conservazione di eventuali definizioni di ritaglio esistenti. Il valore predefinito è true </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> preservePublishState</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> Controlla se lo stato di pubblicazione di una risorsa esistente viene mantenuto durante la sovrascrittura. Se non è impostato, viene utilizzata l'impostazione predefinita della società. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> projectHandleArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> tipi:HandleArray</span> </td> 
   <td colname="col3"> Array di handle di progetto. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> readyForPublish</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> Indica se i file sono contrassegnati come pronti per la pubblicazione. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> unCompressOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> tipi:AnnullaCompressOptions</span> </td> 
   <td colname="col3">Estrarre ed elaborare il contenuto dei file TAR/ZIP caricati con queste impostazioni facoltative. Vedere <a href="../../types/c-data-types/r-uncompress-options.md#reference-510ec7028b1540bc9b58745f242d49d5" format="dita" scope="local"> UnCompressOptions</a>. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> unsharpMaskOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> tipi:UnsharpMaskOptions</span> </td> 
   <td colname="col3">Opzioni che consentono di controllare le impostazioni di maschera di contrasto durante la creazione di un file TIF piramidale ottimizzato. Usate queste impostazioni per migliorare la nitidezza delle immagini. Vedere <a href="../../types/c-data-types/r-unsharp-mask-options.md#reference-b9a96244d7ee4424bc4ac3c23be3be3d" format="dita" scope="local"> UnsharpMaskOptions</a>. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> urlArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:UrlArray</span> </td> 
   <td colname="col3"> Un array di URL da caricare. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> xmpKeywords</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> <p>Un’ulteriore opzione di metadati per tutti gli elementi del processo di caricamento. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Note {#section-637405ff7e0b4a71b83fd359b92fa0c2}

Per `CropOptions`, potete scegliere solo una delle opzioni seguenti:

* `manualCropOptions`
* `autoColorCropOptions`
* `autoTransparentCropOptions`

Per `PublishJob`, potete scegliere solo una delle opzioni seguenti:

* `postImageServingPublishJob`
* `postImageRenderingPublishJob`
* `postvideoPublishJob`

