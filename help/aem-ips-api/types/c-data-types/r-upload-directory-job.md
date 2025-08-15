---
description: Carica i file dalle directory server specificate su base periodica.
solution: Experience Manager
title: UploadDirectoryJob
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: a23f1bc2-aa6a-4c1d-aab5-7f6dbd08682c
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '461'
ht-degree: 1%

---

# [!DNL UploadDirectoryJob]{#uploaddirectoryjob}

Carica i file dalle directory server specificate su base periodica.

Sintassi

## Parametri {#section-69c07f4e7b2e4a0fba143ffaa9f4d48f}

<table id="table_6E40A78846F444BDB8E437413B90CFCE"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Nome </p> </th> 
   <th colname="col2" class="entry"> <p>Tipo </p> </th> 
   <th colname="col3" class="entry"> <p>Descrizione </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> opzioni colore automatico</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> tipi:OpzioniColoreAutomatico</span> </td> 
   <td colname="col3"> <p>Opzioni di ritaglio automatico dell’immagine (in base al colore). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> autoSetCreationOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> tipi:AutoSetCreateOptions</span> </td> 
   <td colname="col3"> <p>Array di script per la generazione automatica di set da applicare ai file caricati. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> autoTransparentCropOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> tipi:AutoTransparentCropOptions</span> </td> 
   <td colname="col3"> <p>Rimuove lo spazio vuoto dai bordi delle immagini, in base alla trasparenza. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> colorManagementOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> tipi:ColorManagementOptions</span> </td> 
   <td colname="col3"> <p>Opzioni che è possibile specificare durante un caricamento. Il set influisce sul modo in cui il colore viene gestito per il caricamento. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> createMask</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:booleano</span> </td> 
   <td colname="col3"> <p>Specifica se creare una maschera durante il caricamento. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> destFolder</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> <p>cartella IPS per i file. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> impostazione e-mail</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> <p>Scelta delle impostazioni e-mail. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> illustratorOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> tipi:IllustratorOptions</span> </td> 
   <td colname="col3"> <p>Opzioni per caricare i file Illustrator sul server immagini. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> includeSubfolders</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> <p>Indica se includere le sottocartelle durante il caricamento. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> inDesignOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> tipi:InDesignOptions</span> </td> 
   <td colname="col3"> <p>Opzioni per caricare i file InDesign sul server. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> knockoutBackground</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> tipi:KnockoutBackgroundOptions</span> </td> 
   <td colname="col3"> <p>Maschera lo sfondo per le immagini selezionate. Questo consente di sovrapporli ad altri livelli con una trasparenza al di fuori dell'immagine del soggetto. </p> <p>Facoltativo. </p> <p>Vedere <a href="../../types/c-data-types/r-knockout-background-options.md#reference-9196371848964d91842b337640791c9c" format="dita" scope="local"> KnockoutBackgroundOptions</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> manualCropOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> tipi:ManualCropOptions</span> </td> 
   <td colname="col3"> <p>Opzioni di ritaglio immagine manuale. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> opzioni multimediali</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> tipi:MediaOptions</span> </td> 
   <td colname="col3"> <p>Opzioni che consentono di impostare una miniatura dal video. </p> <p>Vedere <a href="../../types/c-data-types/r-media-options.md#reference-18618fc6803a4b6e994bbb48eba93b5b" format="dita" scope="local"> MediaOptions</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> sovrascrittura</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> <p>Opzioni di sovrascrittura caricamento file. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> pdfOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> tipi:PDFOptions</span> </td> 
   <td colname="col3"> <p>Opzioni per il caricamento di file PDF sul server immagini. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> photoshopOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> tipi:PhotoshopOptions</span> </td> 
   <td colname="col3"> <p>Opzioni per il caricamento di file Photoshop sul server immagini. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> postHttpUrl</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> <p>URL della destinazione di caricamento file. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> postImageRenderingPublish</span> </span>Processo </td> 
   <td colname="col2"> <span class="codeph"> tipi:ImageRendingPublishJob</span> </td> 
   <td colname="col3"> <p>Dettagli di un processo di pubblicazione di rendering di immagini eseguito dopo il completamento del caricamento. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> postImageServingPublishJob</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> tipi:ImageServingPublishJob</span> </td> 
   <td colname="col3"> <p>Dettagli di un processo di pubblicazione di server immagini eseguito dopo il completamento del caricamento. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> postJobOnlyIfFiles</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:booleano</span> </td> 
   <td colname="col3"> <p>Specifica se caricare solo i file. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> opzioni postScript</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> tipi:PostScriptOptions</span> </td> 
   <td colname="col3"> <p>Opzioni per il caricamento di file Post Script sul server immagini. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> postVideoPublishJob</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> tipi:VideoPublishJob</span> </td> 
   <td colname="col3"> <p>Dettagli di un processo di pubblicazione video eseguito al termine del caricamento. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> preserveCrop</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:booleano</span> </td> 
   <td colname="col3"> <p>Controlla la conservazione di eventuali definizioni di ritaglio esistenti. Impostazione predefinita: true. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> preservePublishState</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:booleano</span> </td> 
   <td colname="col3"> <p>Controlla se lo stato di pubblicazione di una risorsa esistente viene mantenuto durante la sovrascrittura. Se non viene impostata, viene utilizzata l’impostazione predefinita della società. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> processMetadataFiles</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> <p>Indica se elaborare file XML di metadati separati per questo processo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> projectHandleArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> tipi:HandleArray</span> </td> 
   <td colname="col3"> <p>Array di handle di progetto. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> readyForPublish</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:booleano</span> </td> 
   <td colname="col3"> <p>Determina se i file sono contrassegnati per la pubblicazione. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> serverDir</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> <p>Directory di caricamento Source. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> unCompressOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> tipi:UnCompressOptions</span> </td> 
   <td colname="col3"> <p>Estrai ed elabora il contenuto dei file TAR/ZIP caricati con queste impostazioni facoltative. </p> <p>Vedere <a href="../../types/c-data-types/r-uncompress-options.md#reference-510ec7028b1540bc9b58745f242d49d5" format="dita" scope="local"> UnCompressOptions</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> unsharpMaskOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> tipi:UnsharpMaskOptions</span> </td> 
   <td colname="col3"> <p>Opzioni che consentono di controllare le impostazioni della maschera di contrasto durante la creazione di un file TIF piramidale ottimizzato. Utilizza queste impostazioni per migliorare la nitidezza delle immagini. </p> <p>Vedere <a href="https://experienceleague.adobe.com/docs/dynamic-media-developer-resources/image-production-api/data-types/r-unsharp-mask-options.html"> UnsharpMaskOptions</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> xmpKeywords</span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> xsd:string</span> </p> </td> 
   <td colname="col3"> <p>Opzione metadati aggiuntiva per tutto il contenuto del processo di caricamento </p> </td> 
  </tr> 
 </tbody> 
</table>

## Note {#section-637405ff7e0b4a71b83fd359b92fa0c2}

Per `CropOptions`, è possibile scegliere solo una delle seguenti opzioni:

* `manualCropOptions`
* `autoColorCropOptions`
* `autoTransparentCropOptions`

Per `PublishJob`, è possibile scegliere solo una delle seguenti opzioni:

* `postImageServingPublishJob`
* `postImageRenderingPublishJob`
* `postvideoPublishJob`
