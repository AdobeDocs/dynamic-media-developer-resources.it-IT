---
description: Utilizza getActiveJobs per tenere traccia dei caricamenti del desktop.
seo-description: Utilizza getActiveJobs per tenere traccia dei caricamenti del desktop.
seo-title: UploadPostJob
solution: Experience Manager
title: UploadPostJob
topic: Scene7 Image Production System API
uuid: 172f47c7-685a-4014-9c30-dacd78733655
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# UploadPostJob{#uploadpostjob}

Utilizza getActiveJobs per tenere traccia dei caricamenti del desktop.

Consultate anche [Caricamento delle risorse tramite POST HTTP in corso...](../../c-http-post.md#concept-457855c0cdc943339ca1f1bed356991d).

>[!NOTE]
>
>Tutte le richieste POST per un processo di caricamento devono provenire dallo stesso indirizzo IP.

## Parametri {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

<table id="table_04100BB8ABD84EF68B0A7CE3AD946414"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Nome </p> </th> 
   <th colname="col2" class="entry"> <p>Tipo </p> </th> 
   <th colname="col03" class="entry"> <p>Obbligatorio? </p> </th> 
   <th colname="col3" class="entry"> <p>Descrizione </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> autoColorCropOptions</span></span> </td> 
   <td colname="col2"> <span class="codeph"> tipi:AutoColorCropOptions</span> </td> 
   <td colname="col03"> <p>No </p> </td> 
   <td colname="col3"> <p>Opzioni per ritagli automatici di immagini in base al colore. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> autoSetCreationOptions</span></span> </td> 
   <td colname="col2"> <span class="codeph"> tipi:AutoSetCreateOptions</span> </td> 
   <td colname="col03"> <p>No </p> </td> 
   <td colname="col3"> <p>Array di script di generazione di set automatici da applicare ai file caricati. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> autoTransparentCropOptions</span></span> </td> 
   <td colname="col2"> <span class="codeph"> tipi:AutoTransparentCropOptions</span> </td> 
   <td colname="col03"> <p>No </p> </td> 
   <td colname="col3"> <p>Rimuove lo spazio bianco dai bordi delle immagini, in base alla trasparenza. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> colorManagementOptions <span class="varname"></span></span> </td> 
   <td colname="col2"> <span class="codeph"> tipi:ColorManagementOptions</span> </td> 
   <td colname="col03"> <p>No </p> </td> 
   <td colname="col3"> <p>Opzioni che potete specificare durante un caricamento. Il set influisce sulla modalità di gestione del colore per il caricamento. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> create <span class="varname"> Mask</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col03"> <p><b>Sì</b> </p> </td> 
   <td colname="col3"> <p>Se creare una maschera. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> emailSetting</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col03"> <p><b>Sì</b> </p> </td> 
   <td colname="col3"> <p>Scelta delle impostazioni e-mail. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> inDesignOptions</span></span> </td> 
   <td colname="col2"> <span class="codeph"> tipi:InDesignOptions</span> </td> 
   <td colname="col03"> <p>No </p> </td> 
   <td colname="col3"> <p>Opzioni per caricare i file InDesign sul server immagini. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> IllustratorOptions</span></span> </td> 
   <td colname="col2"> <span class="codeph"> tipi:IllustratorOptions</span> </td> 
   <td colname="col03"> <p>No </p> </td> 
   <td colname="col3"> <p>Opzioni per caricare i file Illustrator sul server immagini. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> knockoutBackground</span></span> </td> 
   <td colname="col2"> <span class="codeph"> tipi:KnockoutBackgroundOptions</span> </td> 
   <td colname="col03"> <p>No </p> </td> 
   <td colname="col3"> <p>Mascherare lo sfondo per le immagini selezionate. Questo consente di sovrapporle ad altri livelli con una trasparenza all’esterno dell’immagine oggetto. Facoltativo. </p> <p>Vedere<a href="../../types/c-data-types/r-knockout-background-options.md#reference-9196371848964d91842b337640791c9c" format="dita" scope="local"> KnockoutBackgroundOptions</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> manual <span class="varname"> CropOptions</span></span> </td> 
   <td colname="col2"> <span class="codeph"> tipi:ManualCropOptions</span> </td> 
   <td colname="col03"> <p>No </p> </td> 
   <td colname="col3"> <p>Opzioni per ritagli manuali di immagini. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> mediaOptions</span></span> </td> 
   <td colname="col2"> <span class="codeph"> tipi:MediaOptions</span> </td> 
   <td colname="col03"> <p>No </p> </td> 
   <td colname="col3"> <p>Opzioni che consentono di impostare una miniatura del video. </p> <p>Consultate <a href="../../types/c-data-types/r-media-options.md#reference-18618fc6803a4b6e994bbb48eba93b5b" format="dita" scope="local"> MediaOptions</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> sovrascrittura</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col03"> <p><b>Sì</b> </p> </td> 
   <td colname="col3"> <p>Se sovrascrivere o meno i file durante il caricamento. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> pdfOptions</span></span> </td> 
   <td colname="col2"> <span class="codeph"> tipi:PDFOptions</span> </td> 
   <td colname="col03"> <p>No </p> </td> 
   <td colname="col3"> <p>Opzioni per caricare file PDF sul server immagini. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> photoshopOptions</span></span> </td> 
   <td colname="col2"> <span class="codeph"> tipi:PhotoshopOptions</span> </td> 
   <td colname="col03"> <p>No </p> </td> 
   <td colname="col3"> <p>Opzioni per caricare i file Photoshop sul server immagini. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> postHttpUrl</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col03"> <p>No </p> </td> 
   <td colname="col3"> <p>L’URL in cui vengono caricati i file. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> postScriptOptions <span class="varname"></span></span> </td> 
   <td colname="col2"> <span class="codeph"> tipi:PostScriptOptions</span> </td> 
   <td colname="col03"> <p>No </p> </td> 
   <td colname="col3"> <p>Opzioni per caricare i file PostScript sul server immagini. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> preserveCrop</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col03"> <p>No </p> </td> 
   <td colname="col3"> <p>Controlla la conservazione di eventuali definizioni di ritaglio esistenti. I valori predefiniti sono veri. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> preservePublishState <span class="varname"></span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col03"> <p><b>Sì</b> </p> </td> 
   <td colname="col3"> <p>Controlla se lo stato di pubblicazione di una risorsa esistente viene mantenuto durante la sovrascrittura. Se non è impostato, viene utilizzata l'impostazione predefinita della società. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> projectHandleArray</span></span> </td> 
   <td colname="col2"> <span class="codeph"> tipi:HandleArray</span> </td> 
   <td colname="col03"> <p>No </p> </td> 
   <td colname="col3"> <p>Array di handle di progetto. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> readyForPublish</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col03"> <p><b>Sì</b> </p> </td> 
   <td colname="col3"> <p>Indica se i file sono contrassegnati come pronti per la pubblicazione. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> unCompressOptions</span></span> </td> 
   <td colname="col2"> <span class="codeph"> tipi:AnnullaCompressOptions</span> </td> 
   <td colname="col03"> <p>No </p> </td> 
   <td colname="col3"> <p>Estrarre ed elaborare il contenuto dei file TAR/ZIP caricati con queste impostazioni facoltative. </p> <p>Vedere <a href="../../types/c-data-types/r-uncompress-options.md#reference-510ec7028b1540bc9b58745f242d49d5" format="dita" scope="local"> AnnullaCompressOptions</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> unsharpMaskOptions</span></span> </td> 
   <td colname="col2"> <span class="codeph"> tipi:UnsharpMaskOptions</span> </td> 
   <td colname="col03"> <p>No </p> </td> 
   <td colname="col3"> <p>Opzioni che consentono di controllare le impostazioni di maschera di contrasto durante la creazione di un file TIF piramidale ottimizzato. Usate queste impostazioni per migliorare la nitidezza delle immagini. </p> <p>Consultate <a href="../../types/c-data-types/r-unsharp-mask-options.md#reference-b9a96244d7ee4424bc4ac3c23be3be3d" format="dita" scope="local"> UnsharpMaskOptions</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"><span class="codeph"><span class="varname"> xmpKeywords</span></span> </td> 
   <td colname="col2"><span class="codeph"> xsd:string</span> </td> 
   <td colname="col03"> <p>No </p> </td> 
   <td colname="col3"> <p>Un’ulteriore opzione di metadati per tutti gli elementi del processo di caricamento. </p> </td> 
  </tr> 
 </tbody> 
</table>

