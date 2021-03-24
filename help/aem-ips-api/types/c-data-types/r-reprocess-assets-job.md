---
description: Tipo di processo per consentire la rielaborazione dei file principali caricati in precedenza, inclusi la cancellazione dei PDF e la riottimizzazione delle immagini.
solution: Experience Manager
title: ReprocessAssetsJob
feature: Dynamic Media Classic,SDK/API,Gestione risorse
role: Sviluppatore,Amministratore
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '474'
ht-degree: 2%

---


# ReprocessAssetsJob{#reprocessassetsjob}

Tipo di processo per consentire la rielaborazione dei file principali caricati in precedenza, inclusi la cancellazione dei PDF e la riottimizzazione delle immagini.

Sintassi

## Parametri {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

<table id="table_04100BB8ABD84EF68B0A7CE3AD946414"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Nome </p> </th> 
   <th colname="col2" class="entry"> <p>Tipo </p> </th> 
   <th colname="col3" class="entry"> <p>Descrizione </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> assetHandleArray</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> tipi:HandleArray</span> </p> </td> 
   <td colname="col3"> <p>Gestione risorse. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> readyForPublish</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:boolean</span> </p> </td> 
   <td colname="col3"> <p>Se i file sono contrassegnati come pronti per la pubblicazione. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> preservePublishState</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:boolean</span> </p> </td> 
   <td colname="col3"> <p>Controlla se lo stato di pubblicazione di una risorsa esistente viene mantenuto durante la sovrascrittura. Se non è impostato, viene utilizzata l'impostazione predefinita della società. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> createMask</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:boolean</span> </p> </td> 
   <td colname="col3"> <p>Se creare una maschera. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> preserveCrop</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:boolean</span> </p> </td> 
   <td colname="col3"> <p>Controlla la conservazione di qualsiasi definizione di coltura esistente. Il valore predefinito è true.</p> <p>Se fornisci il parametro manualCropOptions e i valori corrispondenti, i nuovi valori (escluso 0,0,0,0) vengono applicati alla risorsa indipendentemente dal valore preserveCrop.</p><p>Se <i>non</i> fornisci il parametro manualCropOptions, il valore di preserveCrop viene mantenuto. E, in caso di true, i valori preserveCrop esistenti vengono mantenuti; in caso di false, i valori preserveCrop vengono rimossi.</p><p>Esempio:</p><p><p>&lt;preservecrop&gt;false&lt;/preservecrop&gt;<br />&lt;manualcropoptions&gt;<br />    &lt;left&gt;190&lt;/left&gt;<br />    &lt;right&gt;310&lt;/right&gt;<br />    &lt;top&gt;160&lt;/top&gt;<br />    &lt;bottom&gt;120&lt;/bottom&gt;<br />&lt;/manualcropoptions&gt;</p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> manualCropOptions</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> tipi:ManualCropOptions</span> </p> </td> 
   <td colname="col3"> <p>Opzioni di ritaglio manuali. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> autoColorCropOptions</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> tipi:OpzioniRitaglioColoreAutomatico</span> </p> </td> 
   <td colname="col3"> <p>Opzioni per ritagli automatici di immagini in base al colore. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> autoTransparentCropOptions</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> tipi:AutoTransparentCropOptions</span> </p> </td> 
   <td colname="col3"> <p>Rimuove lo spazio bianco dai bordi delle immagini, in base alla trasparenza. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> photoshopOptions</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> tipi:PhotoshopOptions</span> </p> </td> 
   <td colname="col3"> <p>Opzioni per il caricamento di file Photoshop sul server di immagini. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> postScriptOptions</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> tipi:PostScriptOptions</span> </p> </td> 
   <td colname="col3"> <p>Opzioni per il caricamento di file PostScript sul server di immagini. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> pdfOptions</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> tipi:PDFOptions</span> </p> </td> 
   <td colname="col3"> <p>Opzioni per il caricamento di file PDF sul server di immagini. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> mediaOptions</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> tipi:MediaOptions</span> </p> </td> 
   <td colname="col3"> <p>Opzioni del file multimediale A/V. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> illustratorOptions</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> tipi:IllustratorOptions</span> </p> </td> 
   <td colname="col3"> <p>Opzioni per il caricamento di file Illustrator sul server di immagini. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> colorManagementOptions</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> tipi:ColorManagementOptions</span> </p> </td> 
   <td colname="col3"> <p>Opzioni che puoi specificare durante un caricamento. Il set influisce sulla modalità di gestione del colore per il caricamento. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> autoSetCreationOptions</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> tipi:AutoSetCreationOptions</span> </p> </td> 
   <td colname="col3"> <p>Array di script di generazione di set automatici da applicare ai file caricati. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> projectHandleArray</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> tipi:HandleArray</span> </p> </td> 
   <td colname="col3"> <p>Matrice di handle di progetto. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> emailSetting</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:string</span> </p> </td> 
   <td colname="col3"> <p>Opzioni per le impostazioni e-mail. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> postJobOnlyIfFiles</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:boolean</span> </p> </td> 
   <td colname="col3"> <p>Se caricare solo i file. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> postHttpUrl</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:string</span> </p> </td> 
   <td colname="col3"> <p>URL della posizione di caricamento del file. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> postImageServingPublishJob</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> tipi:ImageServingPublishJob</span> </p> </td> 
   <td colname="col3"> <p>Dettagli del processo per un processo di pubblicazione di image serving da eseguire dopo il completamento del caricamento. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> postImageRenderingPublishJob</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> tipi:ImageRenderingPublishJob</span> </p> </td> 
   <td colname="col3"> <p>Dettagli del processo per un processo di pubblicazione di rendering di immagini da eseguire al termine del caricamento. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> postVideoPublishJob</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> tipi:VideoPublishJob</span> </p> </td> 
   <td colname="col3"> <p>Dettagli del processo per un processo di pubblicazione video da eseguire al termine del caricamento. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> inDesignOptions</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> tipi:InDesignOptions</span> </p> </td> 
   <td colname="col3"> <p>Opzioni per il caricamento di file InDesign nel server di immagini. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> knockoutBackground</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> tipi:KnockoutBackgroundOptions</span> </p> </td> 
   <td colname="col3"> <p>Maschera lo sfondo per le immagini selezionate. Questo consente di sovrapporle ad altri livelli con una trasparenza al di fuori dell'immagine del soggetto. </p> <p>Facoltativo. </p> <p>Vedere<a href="../../types/c-data-types/r-knockout-background-options.md#reference-9196371848964d91842b337640791c9c" format="dita" scope="local"> KnockoutBackgroundOptions</a> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> unSharpMaskOptions</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> tipi:UnSharpMaskOptions</span> </p> </td> 
   <td colname="col3"> <p>Opzioni che consentono di controllare le impostazioni della maschera di contrasto durante la creazione di un file TIF piramidale ottimizzato. Utilizza queste impostazioni per migliorare la nitidezza delle immagini. </p> <p>Consulta <a href="https://experienceleague.adobe.com/docs/dynamic-media-developer-resources/image-production-api/data-types/r-unsharp-mask-options.html"> UnSharpMaskOptions</a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Note**

Le scelte per `*CropOptions` includono:

* `manualCropOptions`
* `autoColorCropOptions`
* `autoTransparentCropOptions`

Le scelte per `*PublishJob` includono:

* `postImageServingPublishJob`
* `postImageRenderingPublishJob`
* `postVideoPublishJob`

