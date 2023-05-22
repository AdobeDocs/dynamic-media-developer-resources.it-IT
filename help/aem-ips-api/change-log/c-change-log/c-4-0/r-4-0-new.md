---
title: Nuove aggiunte e modifiche
description: Vengono descritte le modifiche nuove e implementate per l'API IPS v4.0.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: f07562a8-71e9-4d98-9d0c-5bb32a7e0ef1
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '1195'
ht-degree: 1%

---

# Nuove aggiunte e modifiche{#new-additions-and-changes}

Vengono descritte le modifiche nuove e implementate per l&#39;API IPS v4.0.

Sono state implementate versioni API affiancate con WSDL e spazi dei nomi degli schemi separati.

* Versioni API precedenti: `IpsApi.wsdl, http://www.scene7.com/IpsApi/xsd`.
* Versione SPS 4.0: `IpsApi-2008-01-15.wsdl, http://www.scene7.com/IpsApi/xsd/2008-01-15`.

Aggiunto `PostScriptOptions/alpha` campo.

Aggiunto `VideoRootUrl` e `SwfRootUrl` proprietà per `getProperty` operazione.

Opzionale aggiunto `appName` e `appVersion` parametri a `authHeader` per tenere traccia dell&#39;applicazione chiamante. Registrazione aggiunta a `ipsApiService.log`.

È stata aggiunta un’opzione `serviceUrl` parametro per il servlet di generazione WSDL. Questo parametro è utile per i proxy di debug. Ad esempio: `http://<server>/scene7/webservice/IpsApi-2008-01-15.wsdl?serviceUrl=http://localhost:8081`

Implementato `getZipEntries` operazione.

Sono stati implementati intervalli di ricerca e valori di confronto digitati per le condizioni dei campi di sistema.

Aggiunto `'Asset'` costante stringa di tipo risorsa, principalmente per consentire campi di metadati tra risorse diverse.

Implementato `trashState` parametro per `searchAssets`.

Implementato `getAssetPublishHistory` operazione.

Opzionale aggiunto `faultHttpStatusCode` Intestazione SOAP per abilitare la gestione degli errori in Flex. Per Flex, utilizza `<faultHttpStatusCode>200</faultHttpStatusCode>`. Il codice di stato predefinito per le risposte di errore è `500 (Internal Server Error)`.

Sono state aggiunte operazioni per ripristinare le risorse dal cestino e svuotare le risorse dal cestino.

Implementazione delle operazioni CRUD.

È stato aggiunto il flag abilitato a `ImageMap` tipo e `saveImageMap` operazione.

È stato aggiunto il supporto per i processi di ottimizzazione dei file rimanenti.

Aggiunto `setAssetsPublishState` per aggiornamenti in blocco dello stato di pubblicazione.

Aggiunto `ImageServingPublishSettings`, `getImageServingPublishSettings`, `setImageServingPublishSettings`.

Obsoleto `saveMetadataField` operazione a favore di nuovi `createMetadataField` e `updateMetadataField` operazioni.

Implementato `deleteAssetsParam` operazione di eliminazione batch.

Implementato `moveAssetsParam` operazione di spostamento batch.

Implementato `deleteMetadataField` operazione.

Implementato `get/setImageRenderingPublishSettings`, `get/set/create/updateVignettePublishFormat` operazioni.

Implementato `getAssetCounts`.

Supporto aggiunto a `setImageSetMembers` per includere `RenderSet` membri in `ImageSet` risorse.

Aggiunto `replaceImage` operazione.

Aggiunto `copyImage` operazione.

Aggiunto `setUrlModifier` funzionamento e `urlModifier/urlPostApplyModifier` campi per `LayerViewInfo`, `TemplateInfo`, e `WatermarkInfo`.

Aggiunto `createDerivedAsset` operazione. Attualmente il `ownerHandle` deve fare riferimento a una risorsa Immagine e il tipo può essere `AdjustedView` o `LayerView`.

Aggiunto `createTemplate` operazione. Richiama per creare risorse modello o filigrana.

impostazioni aziendali IPS, `CompanySettings`, portato all’API dei servizi Web.

Aggiunto `excludeByproducts` filtra flag per `searchAssets` operazione. Impostazione di questo flag su esecuzioni vere `PSDlayer` immagini e immagini copiate da PDF.

Aggiunto `getGenerationInfo` operazione.

Aggiunto `SystemMessage` nome proprietà a `getProperty` operazione.

Sono state modificate alcune costanti stringa di tipo risorsa per farle corrispondere ai campi Informazioni risorsa corrispondenti.

* WordDoc: Word
* ExcelDoc: Excel
* PowerPointDoc: PowerPoint
* RTFDoc: Rtf

Formato risultato modificato delle operazioni batch per riepilogare le operazioni riuscite, gli avvisi e gli errori.

Implementato `batchSetAssetMetadata` operazione batch di metadati.

È stato implementato il supporto per i dati specifici dell’app.

È stato implementato il supporto dei flag booleani per `createTemplate`, `extendLayers`, e `extractText` processi di caricamento per controllare il processo di elaborazione Photoshop (simile alle modifiche per gli upload di file di aggiunta).

Implementato `setImageMaps` e `setZoomTargets` operazioni.

Implementato `ViewerPreset` operazioni. I tipi riconosciuti sono:

* `VideoPlayer` (Il video pubblica solo questi visualizzatori).
* `Brochure`
* `BasicZoom`
* `AdvancedZoom`
* `Spin`
* `Custom types`

Gli skin del visualizzatore supportano due parametri: `skinFg` e `skinBg`. Il codice back-end esegue tutte le operazioni di elaborazione necessarie per mantenere la compatibilità con le versioni precedenti.

Implementato `getAssociatedAssets` operazione.

Aggiunto `ReprocessAssets` tipo di processo per consentire la rielaborazione dei file di origine primari caricati in precedenza, inclusa la copia dei PDF e la riottimizzazione delle immagini.

Rinominato `PropertySetType` tipo di campo a `propertyType`. Questa ridenominazione influisce sul `createPropertySetType` Parametro e `getPropertySetType/getPropertySetTypes` risposta.

Implementato `batchSetImageFields` operazione per supportare l&#39;impostazione di dati utente immagine e di altri campi immagine modificabili.

47 È stato aggiunto il campo fileSize a vari tipi di informazioni sulle risorse:

* `VignetteInfo`
* `CabinetInfo`
* `WindowCoveringInfo`
* `IccProfileInfo`
* `FontInfo`
* `XslInfo`
* `ViewerSwfInfo`
* `XmlInfo`
* `SvgInfo`
* `ZipInfo`
* `VideoInfo`
* `AcoInfo`
* `PdfInfo`
* `PsdInfo`
* `FlashInfo`
* `InDesignInfo`
* `PostScriptInfo`
* `IllustratorInfo`
* `WordInfo`
* `ExcelInfo`
* `PowerPointInfo`
* `IllustratorInfo`
* `WordInfo`
* `ExcelInfo`
* `PowerPointInfo`
* `RTFInfo`

Implementato `getActivePublishContexts` operazione. Questa operazione restituisce un array di nomi di contesto di pubblicazione con server di pubblicazione attivi per la società specificata. I nomi di contesto di pubblicazione correnti sono:

* `ImageServing`
* `ImageRendering`
* `Video`

Implementato `getSearchStrings` operazione. Restituisce un array di stringhe di ricerca per la risorsa specificata.

Sono stati aggiunti i parametri delle impostazioni locali per i processi e un meccanismo per impostare le impostazioni locali per le operazioni API. La stringa delle impostazioni locali deve essere formattata come `<language_code>[-<country_code>]`. Il codice della lingua è un codice a due lettere minuscole come specificato dallo standard ISO-639 e il codice facoltativo del paese è un codice a due lettere maiuscole come specificato dallo standard ISO-3166.

È stato aggiunto un parametro locale opzionale al `authHeader` Intestazione SOAP per impostare le impostazioni locali per le operazioni API. Se questo parametro non è presente, l’intestazione HTTP `Accept-Language` viene utilizzato. Se anche questa intestazione non è presente, viene utilizzata la lingua predefinita per il server IPS.

È stato aggiunto il supporto per get/set per campi di metadati fortemente tipizzati.

È stato implementato il supporto SOAP e HTTP header per il controllo della risposta gzip.

Aggiunto `gzipResponse` contrassegna per `authHeader`. Se non è presente, l’API controlla il `Accept-Encoding` intestazione.

È stato aggiunto il supporto a searchAssets per le condizioni dei campi di metadati fortemente tipizzati.

* Per tutti i tipi di campo, il valore può essere passato con un operatore di confronto delle stringhe ( `Equals, NotEquals, Contains, NotContains, StartsWith, EndsWith`)
* Per i campi booleani: `boolVal` può essere trasmesso con `Equals` Op.
* Per i campi Int: `longVal` può essere trasmesso con un operatore di confronto numerico ( `Equals, NotEquals, LessThan, LessThanEquals, GreaterThan, GreaterThanEquals`) o `minLong/maxLong` può essere trasmesso con operazioni di intervallo numerico ( `Between, NotBetween`).
* Per i campi Mobile: `doubleVal` può essere trasmesso con un operatore di confronto numerico ( `Equals, NotEquals, LessThan, LessThanEquals, GreaterThan, GreaterThanEquals`) o `minDouble/maxDouble` può essere trasmesso con operazioni di intervallo numerico ( `Between, NotBetween`).
* Per i campi Data, è possibile trasmettere `dateVal` con operatore di confronto numerico ( `Equals, NotEquals, LessThan, LessThanEquals, GreaterThan, GreaterThanEquals`) oppure è possibile passare minDate/maxDate con operazioni di intervallo numerico ( `Between, NotBetween`).

È stata aggiunta la descrizione `jobSubType`, e `originalJobName` campi per `JobLog` tipo.

* `originalJobName` è il nome del processo inviato a `submitJob` (senza suffissi di univocità o nomi di processo successivi).
* `jobSubType` viene utilizzato solo da `ImageServingPublishJob` lavori (dove è uno dei `full`, `increment, fullwithsearch,` o `fulloverride`).
* `description` è una stringa vuota per tutti i tipi di processo, ma alla fine contiene informazioni di riepilogo sul processo, ad esempio il percorso di caricamento.

Inoltre, i seguenti campi non sono inclusi in entrambi `getJobLogs` e `getJobLogDetails`. Nelle versioni precedenti, erano disponibili solo con `getJobLogDetails`.

* `endDate` (se il processo è stato completato).
* `fileDuplicateCount` (prima era sempre `0` con `getJobLogs`)
* `fileUpdateCount` (in precedenza era sempre `0` con `getJobLogs` e inclusi in `fileSuccessCount`; ora è suddiviso in campi separati).

È stato aggiunto il campo assetHandle a `JobLogDetail` tipo.

È stato aggiunto un parametro descrittivo opzionale a `submitJob`. Questo parametro viene trasmesso per il recupero in `getScheduledJobs`, `getActiveJobs`, e `getJobLogs`.

Campo di sistema SKU obsoleto. Il campo viene ignorato se viene passato come `SystemFieldCondition` a `searchAssets`.

Aggiunto `excludeAssetTypeArray` filtra per `searchAssets`.

Aggiunto `MaskInfo` digita in `Asset`.

Sono stati aggiunti nuovi tipi di risorse per la gestione tramite IPS:

<table id="table_DCCE936B797A448598C30E3B344525A5"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Tipo di risorsa </p> </th> 
   <th colname="col2" class="entry"> <p>Descrizione </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Illustrator </span> </p> </td> 
   <td colname="col2"> <p>file Adobe Illustrator. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> PostScript </span> </p> </td> 
   <td colname="col2"> <p>File EPS e PostScript. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> WordDoc </span> </p> </td> 
   <td colname="col2"> <p>Documento Microsoft® Word per file che terminano con .doc. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ExcelDoc </span> </p> </td> 
   <td colname="col2"> <p>Documento Microsoft® Excel per file che terminano con .xls. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> PowerPointDoc </span> </p> </td> 
   <td colname="col2"> <p>Documento Microsoft® PowerPoint per file che terminano con .ppt. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> RTFDoc </span> </p> </td> 
   <td colname="col2"> <p>File RTF per i file caricati che terminano con .rtf. </p> </td> 
  </tr> 
 </tbody> 
</table>

Sono state aggiunte opzioni aggiuntive a `UploadDirectoryJob` e `UploadUrlsJob` per controllare l&#39;elaborazione dei file Postscript, Illustrator e PDF in modo indipendente. Tutti i processi esistenti forniscono i parametri necessari a ciascuna delle tre pipeline di elaborazione in modo che funzionino esattamente come oggi. L&#39;originale `PostScriptOptions` Questo blocco viene utilizzato per impostare l’elaborazione dei file Illustrator e EPS/PS. In alternativa, è possibile fornire blocchi di opzioni di file specifici per specificare l’elaborazione. L’elenco delle modifiche include:

<table id="table_D4E5ACCB2D144D05A5FA0129AA5F9344"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Campo </p> </th> 
   <th colname="col2" class="entry"> <p>Parametro </p> </th> 
   <th colname="col3" class="entry"> <p>Valore </p> </th> 
   <th colname="col4" class="entry"> <p>Descrizione </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1" morerows="1"> <p> <span class="codeph"> [!DNL PostScriptOptions] </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> [!DNL process] </span> </p> </td> 
   <td colname="col3"> <p> 
     <ul id="ul_6BBFF026010F4913BD632B3312E17C4B"> 
      <li id="li_AA1131A68FB242C9A1380DE6F8F318C7"> <p> <span class="codeph"> Nessuno </span> </p> </li> 
      <li id="li_141F4C3FC9D34C9AABECA91394A82969"> <p> <span class="codeph"> Rasterizza </span>(impostazione predefinita) </p> </li> 
     </ul> </p> </td> 
   <td colname="col4"> <p> 
     <ul id="ul_14D0A696DF4E408DA50E102057EB7AC7"> 
      <li id="li_D8AA718D9F504B91AB557216D2D7DBCC"> <p>Gestisci solo la risorsa e non creare derivati al caricamento. </p> </li> 
      <li id="li_3F56CEABAB3E43EAB157C83583A2F58D"> <p>Eseguire il rendering dei file EPS e PostScript in un'immagine alla risoluzione e allo spazio colore prescritti. </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> alfa </span> </p> <p>Facoltativo. </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;boolean&gt; </span> </p> </td> 
   <td colname="col4"> <p>Esegue la rasterizzazione del file in un'immagine. Crea uno sfondo trasparente se il file originale è definito in questo modo per sovrapporre i logo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" morerows="3"> <p> <span class="codeph"> [!DNL IllustratorOptions] </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> processo </span> </p> </td> 
   <td colname="col3"> <p> 
     <ul id="ul_C2F1000A01DE41678A8E1DDE0C8A0E97"> 
      <li id="li_53749049B383441A81CB427A5B5F26A8"> <span class="codeph"> Nessuno </span> </li> 
      <li id="li_C5332FC35E5C4687B30D4C1081015BB0"> <span class="codeph"> Rasterizza </span> (impostazione predefinita) </li> 
     </ul> </p> </td> 
   <td colname="col4"> <p> 
     <ul id="ul_41924574773542B7BFC4989667C14E97"> 
      <li id="li_3886554059AB4F7383619A9CB7292E0E"> <p>Gestisci solo la risorsa e non creare derivati al caricamento. </p> </li> 
      <li id="li_BF3F5E54484C46D8887CA48D8646648E"> <p>Rendering del file in un'immagine alla risoluzione e allo spazio colore prescritti. </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> [!DNL resolution] </span> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;integer&gt; </span> </p> </td> 
   <td colname="col4"> <p>Risoluzione di rasterizzazione. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> [!DNL colorspace] </span> </p> </td> 
   <td colname="col3"> <p> </p> </td> 
   <td colname="col4"> <p>Spazio colore di destinazione per il rendering. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> alfa </span> </p> <p>Facoltativo. </p> </td> 
   <td colname="col3"> <p> </p> </td> 
   <td colname="col4"> <p>Esegue la rasterizzazione del file in un'immagine. Crea uno sfondo trasparente se il file originale è definito in questo modo per la creazione di logo sovrapposti. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" morerows="4"> <p> <span class="codeph"> PDFOptions </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> processo </span> </p> </td> 
   <td colname="col3"> <p> 
     <ul id="ul_EF9C27EE7A154DA890CB9E6BA174D767"> 
      <li id="li_0BB0FC1BA43043EEA1EA257E5D603978"> <p> <span class="codeph"> Nessuno </span> </p> </li> 
      <li id="li_E3FA07129C2646C7B98854C22CDAC1F0"> <p> <span class="codeph"> Rasterizza </span> (impostazione predefinita) </p> </li> 
     </ul> </p> </td> 
   <td colname="col4"> <p> 
     <ul id="ul_84EE74454FF5434087A895F915E68103"> 
      <li id="li_4312A1CD5F4B44589678311A59536FA7"> <p>Gestisci solo la risorsa e non creare derivati al caricamento. </p> </li> 
      <li id="li_06FBA83EA3F248E288F4790255802DE6"> <p>Rendering del file in un'immagine alla risoluzione e allo spazio colore prescritti. </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> [!DNL resolution] </span> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;integer&gt; </span> </p> </td> 
   <td colname="col4"> <p>Risoluzione di rasterizzazione. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> [!DNL colorspace] </span> </p> </td> 
   <td colname="col3"> <p> </p> </td> 
   <td colname="col4"> <p>Spazio colore di destinazione per il rendering. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> pdfCatalog </span> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;boolean&gt; </span> </p> </td> 
   <td colname="col4"> <p>Definisce se combinare un PDF di più pagine in un eCatalog dopo il rendering (il valore predefinito è true). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> extractSearchWords </span> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;boolean&gt; </span> </p> </td> 
   <td colname="col4"> <p>Definisce se le parole del PDF vengono estratte nel database per essere successivamente fornite a un server di ricerca (il valore predefinito è false). </p> </td> 
  </tr> 
 </tbody> 
</table>

Puoi anche eseguire query da `getScheduledJobs`.

Modificato il `webservice.gzip.response` proprietà di configurazione per accettare uno dei seguenti valori:

<table id="table_FCBBF1643DC84F5CBF81DCA6B552E0C4"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Valore </p> </th> 
   <th colname="col2" class="entry"> <p>Descrizione </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> [!DNL never] </span> </p> </td> 
   <td colname="col2"> <p>Non ricevere risposta Gzip. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> [!DNL soap] </span> </p> </td> 
   <td colname="col2"> <p>Risposta Gzip solo se authHeader/gzipResponse è true. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> [!DNL accept] </span> </p> </td> 
   <td colname="col2"> <p>Gzip se authHeader/gzipResponse è true oppure se non è presente alcuna intestazione gzipResponse e l'intestazione HTTP Accept-Encoding include gzip. (Predefinito). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> [!DNL always] </span> </p> </td> 
   <td colname="col2"> <p>Risposta gzip sempre, indipendentemente dai valori di intestazione. Utilizza questo valore solo a scopo di debug. </p> </td> 
  </tr> 
 </tbody> 
</table>
