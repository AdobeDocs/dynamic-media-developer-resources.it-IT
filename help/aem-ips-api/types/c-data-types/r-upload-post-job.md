---
description: Utilizza getActiveJobs per tenere traccia dei caricamenti sul desktop.
solution: Experience Manager
title: UploadPostJob
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 60163016-fe96-4ac2-9208-da8192042d0f
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '471'
ht-degree: 5%

---

# [!DNL UploadPostJob]{#uploadpostjob}

Utilizza getActiveJobs per tenere traccia dei caricamenti sul desktop.

Vedi anche [Caricamento delle risorse tramite HTTP POST in Caricamento...](../../c-http-post.md#concept-457855c0cdc943339ca1f1bed356991d).

>[!NOTE]
>
>Tutte le richieste POST per un processo di caricamento devono provenire dallo stesso indirizzo IP.

## Parametri {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

<table id="table_04100BB8ABD84EF68B0A7CE3AD946414"> 
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
   <td colname="col1"> <span class="codeph"> <span class="varname"> autoColorCropOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> tipi:AutoColorCropOptions</span> </td> 
   <td colname="col3"> <p>No </p> </td> 
   <td colname="col4"> <p>Opzioni per ritaglio automatico delle immagini in base al colore. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> autoSetCreationOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> tipi:AutoSetCreateOptions</span> </td> 
   <td colname="col3"> <p>No </p> </td> 
   <td colname="col4"> <p>Array di script per la generazione automatica di set da applicare ai file caricati. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> autoTransparentCropOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> tipi:AutoTransparentCropOptions</span> </td> 
   <td colname="col3"> <p>No </p> </td> 
   <td colname="col4"> <p>Rimuove lo spazio vuoto dai bordi delle immagini, in base alla trasparenza. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> colorManagementOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> tipi:ColorManagementOptions</span> </td> 
   <td colname="col3"> <p>No </p> </td> 
   <td colname="col4"> <p>Opzioni che è possibile specificare durante un caricamento. Il set influisce sul modo in cui il colore viene gestito per il caricamento. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> createMask</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:booleano</span> </td> 
   <td colname="col3"> <p><b>Sì</b> </p> </td> 
   <td colname="col4"> <p>Specifica se creare una maschera. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> impostazione e-mail</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> <p><b>Sì</b> </p> </td> 
   <td colname="col4"> <p>Scelta delle impostazioni e-mail. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> inDesignOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> tipi:InDesignOptions</span> </td> 
   <td colname="col3"> <p>No </p> </td> 
   <td colname="col4"> <p>Opzioni per caricare i file InDesign sul server immagini. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> OpzioniIllustrator</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> tipi:IllustratorOptions</span> </td> 
   <td colname="col3"> <p>No </p> </td> 
   <td colname="col4"> <p>Opzioni per caricare i file Illustrator sul server immagini. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> knockoutBackground</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> tipi:KnockoutBackgroundOptions</span> </td> 
   <td colname="col3"> <p>No </p> </td> 
   <td colname="col4"> <p>Maschera lo sfondo per le immagini selezionate. Questo consente di sovrapporli ad altri livelli con una trasparenza al di fuori dell'immagine del soggetto. Facoltativo. </p> <p>Vedere<a href="../../types/c-data-types/r-knockout-background-options.md#reference-9196371848964d91842b337640791c9c" format="dita" scope="local"> KnockoutBackgroundOptions</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> manualCropOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> tipi:ManualCropOptions</span> </td> 
   <td colname="col3"> <p>No </p> </td> 
   <td colname="col4"> <p>Opzioni per ritagli manuali di immagini. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> opzioni multimediali</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> tipi:MediaOptions</span> </td> 
   <td colname="col3"> <p>No </p> </td> 
   <td colname="col4"> <p>Opzioni che consentono di impostare una miniatura dal video. </p> <p>Vedere <a href="../../types/c-data-types/r-media-options.md#reference-18618fc6803a4b6e994bbb48eba93b5b" format="dita" scope="local"> MediaOptions</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> sovrascrittura</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:booleano</span> </td> 
   <td colname="col3"> <p>Sì</p> </td> 
   <td colname="col4"> <p>Specifica se sovrascrivere i file durante il caricamento. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> pdfOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> tipi:PDFOptions</span> </td> 
   <td colname="col3"> <p>No</p> </td> 
   <td colname="col4"> <p>Opzioni per il caricamento di file PDF sul server immagini. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> photoshopOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> tipi:PhotoshopOptions</span> </td> 
   <td colname="col3"> <p>No </p> </td> 
   <td colname="col4"> <p>Opzioni per il caricamento di file Photoshop sul server immagini. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> postHttpUrl</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> <p>No </p> </td> 
   <td colname="col4"> <p>URL in cui vengono caricati i file. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> opzioni postScript</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> tipi:PostScriptOptions</span> </td> 
   <td colname="col3"> <p>No </p> </td> 
   <td colname="col4"> <p>Opzioni per il caricamento di file Post Script sul server immagini. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> preserveCrop</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:booleano</span> </td> 
   <td colname="col3"> <p>No </p> </td> 
   <td colname="col4"> <p>Controlla la conservazione di eventuali definizioni di ritaglio esistenti. Il valore predefinito è true.</p> <p>Se si specifica il parametro manualCropOptions e i valori corrispondenti, i nuovi valori (escluso 0,0,0,0) vengono applicati alla risorsa indipendentemente dal valore preserveCrop.</p><p>Se <i>non</i> fornisce il parametro manualCropOptions, il valore di preserveCrop viene mantenuto. E, in caso di true, i valori preserveCrop esistenti vengono mantenuti; in caso di false, i valori preserveCrop vengono rimossi.</p><p>Esempio:</p><p><p>&lt;preserveCrop&gt;false&lt;/preserveCrop&gt;<br />&lt;manualCropOptions&gt;<br />   &lt;left&gt;190&lt;/left&gt;<br />   &lt;right&gt;310&lt;/right&gt;<br />   &lt;top&gt;160&lt;/top&gt;<br />   &lt;bottom&gt;120&lt;/bottom&gt;<br />&lt;/manualCropOptions&gt;</p></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> preservePublishState</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:booleano</span> </td> 
   <td colname="col3"> <p><b>Sì</b> </p> </td> 
   <td colname="col4"> <p>Controlla se lo stato di pubblicazione di una risorsa esistente viene mantenuto durante la sovrascrittura. Se non viene impostata, viene utilizzata l’impostazione predefinita della società. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> projectHandleArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> tipi:HandleArray</span> </td> 
   <td colname="col3"> <p>No </p> </td> 
   <td colname="col4"> <p>Array di handle di progetto. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> readyForPublish</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:booleano</span> </td> 
   <td colname="col3"> <p><b>Sì</b> </p> </td> 
   <td colname="col4"> <p>Indica se i file sono contrassegnati come pronti per la pubblicazione. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> unCompressOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> tipi:UnCompressOptions</span> </td> 
   <td colname="col3"> <p>No </p> </td> 
   <td colname="col4"> <p>Estrai ed elabora il contenuto dei file TAR/ZIP caricati con queste impostazioni facoltative. </p> <p>Vedere <a href="../../types/c-data-types/r-uncompress-options.md#reference-510ec7028b1540bc9b58745f242d49d5" format="dita" scope="local"> UnCompressOptions</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> unsharpMaskOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> tipi:UnsharpMaskOptions</span> </td> 
   <td colname="col3"> <p>No </p> </td> 
   <td colname="col4"> <p>Opzioni che consentono di controllare le impostazioni della maschera di contrasto durante la creazione di un file TIF piramidale ottimizzato. Utilizza queste impostazioni per migliorare la nitidezza delle immagini. </p> <p>Vedere <a href="../../types/c-data-types/r-unsharp-mask-options.md#reference-b9a96244d7ee4424bc4ac3c23be3be3d" format="dita" scope="local"> UnsharpMaskOptions</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"><span class="codeph"><span class="varname"> xmpKeywords</span></span> </td> 
   <td colname="col2"><span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> <p>No </p> </td> 
   <td colname="col4"> <p>Opzione metadati aggiuntiva per tutto ciò che si trova nel processo di caricamento. </p> </td> 
  </tr> 
 </tbody> 
</table>
