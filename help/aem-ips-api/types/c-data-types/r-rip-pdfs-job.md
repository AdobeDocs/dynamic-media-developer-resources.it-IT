---
description: Un processo che copia nuovamente una risorsa PDF esistente.
seo-description: Un processo che copia nuovamente una risorsa PDF esistente.
seo-title: RipPdfsJob
solution: Experience Manager
title: RipPdfsJob
topic: Scene7 Image Production System API
uuid: 95990d53-4baf-44a2-8d84-3cab2b5c9105
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# RipPdfsJob{#rippdfsjob}

Un processo che copia nuovamente una risorsa PDF esistente.

>[!NOTE]
>
>Questo tipo di processo è obsoleto. Transizione verso `ReprocessAssetsJob` per tutte le integrazioni future.

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
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> pdfHandleArray</span></span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> tipi:HandleArray</span> </p> </td> 
   <td colname="col3"> <p>Gestire l'array di file PDF da estrarre. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> create <span class="varname"> Mask</span></span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:boolean</span> </p> </td> 
   <td colname="col3"> <p>Determina se creare o meno una maschera. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> manual <span class="varname"> CropOptions</span></span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> tipi:ManualCropOptions</span> </p> </td> 
   <td colname="col3"> <p>Opzioni di ritaglio manuale. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> autoColorCropOptions</span></span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> tipi:AutoColorCropOptions</span> </p> </td> 
   <td colname="col3"> <p>Opzioni di ritaglio automatiche. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> autoTransparentCropOptions</span></span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> tipi:PostTransparentCropOptions</span> </p> </td> 
   <td colname="col3"> <p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> postScriptOptions <span class="varname"></span></span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> tipi:PostScriptOptions</span> </p> </td> 
   <td colname="col3"> <p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> pdfOptions</span></span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> tipi:PDFOptions</span> </p> </td> 
   <td colname="col3"> <p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> illustratorOptions <span class="varname"></span></span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> tipi:IllustratorOptions</span> </p> </td> 
   <td colname="col3"> <p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> colorManagementOptions <span class="varname"></span></span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> tipi:ColorManagementOptions</span> </p> </td> 
   <td colname="col3"> <p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> projectHandleArray</span></span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> tipi:HandleArray</span> </p> </td> 
   <td colname="col3"> <p>Un array di handle di progetto. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> emailSetting</span></span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:string</span> </p> </td> 
   <td colname="col3"> <p>Impostazioni e-mail. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> postHttpUrl</span></span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:string</span> </p> </td> 
   <td colname="col3"> <p>L’URL in cui vengono caricati i file. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> post <span class="varname"> ImageServingPublishJob</span></span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> tipi:ImageServingPublishJob</span> </p> </td> 
   <td colname="col3"> <p>Dettagli del processo per il processo di pubblicazione di un server di gestione immagini da eseguire al termine del caricamento. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> post <span class="varname"> ImageRenderingPublishJob</span></span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> tipi:ImageRenderingPublishJob</span> </p> </td> 
   <td colname="col3"> <p>Dettagli del processo per il processo di pubblicazione di un rendering immagine da eseguire al termine del caricamento. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> postVideoPublishJob <span class="varname"></span></span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> tipi:VideoPublishJob</span> </p> </td> 
   <td colname="col3"> <p>Dettagli del processo di pubblicazione di un video da eseguire al termine del caricamento. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> inDesignOptions</span></span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> tipi:InDesignOptions</span> </p> </td> 
   <td colname="col3"> <p>Opzioni per caricare i file Adobe InDesign nel server immagini. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> knockoutBackground</span></span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> tipi:KnockoutBackgroundOptions</span> </p> </td> 
   <td colname="col3"> <p>Mascherare lo sfondo per le immagini selezionate. Questo consente di sovrapporle ad altri livelli con una trasparenza all’esterno dell’immagine oggetto. </p> <p>Facoltativo. </p> <p>Vedere<a href="../../types/c-data-types/r-knockout-background-options.md#reference-9196371848964d91842b337640791c9c" format="dita" scope="local"> KnockoutBackgroundOptions</a> </p> </td> 
  </tr> 
 </tbody> 
</table>

## Note {#section-0822e70fa4784131baa5ad0ba8c0fb3b}

Le scelte per `*CropOptions` includere:

* `manualCropOptions`
* `autoColorCropOptions`
* `autoTransparentCropOptions`

Le scelte per `*PublishJob` includere:

* `postImageServingPublishJob`
* `postImageRenderingPublishJob`
* `postVideoPublishJob`

