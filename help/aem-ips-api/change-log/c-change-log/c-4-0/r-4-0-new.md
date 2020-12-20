---
description: Descrive le modifiche nuove e implementate per l'API IPS v4.0.
seo-description: Descrive le modifiche nuove e implementate per l'API IPS v4.0.
seo-title: Nuove aggiunte e modifiche
solution: Experience Manager
title: Nuove aggiunte e modifiche
topic: Scene7 Image Production System API
uuid: ca4bbe36-c1b7-471f-90a8-6b695d56ac7a
translation-type: tm+mt
source-git-commit: 55015831ed1971a305ddbd8085c95626507355e0
workflow-type: tm+mt
source-wordcount: '1234'
ht-degree: 1%

---


# Nuove aggiunte e modifiche{#new-additions-and-changes}

Descrive le modifiche nuove e implementate per l&#39;API IPS v4.0.

Sono state implementate versioni delle API affiancate con WSDL e spazi dei nomi degli schemi separati.

* Versioni API precedenti: `IpsApi.wsdl, http://www.scene7.com/IpsApi/xsd`.
* Versione SPS 4.0: `IpsApi-2008-01-15.wsdl, http://www.scene7.com/IpsApi/xsd/2008-01-15`.

Aggiunto il campo `PostScriptOptions/alpha`.

Sono state aggiunte le proprietà `VideoRootUrl` e `SwfRootUrl` per l&#39;operazione `getProperty`.

Sono stati aggiunti `appName` e `appVersion` params facoltativi a `authHeader` per tenere traccia dell&#39;applicazione di chiamata. È stata aggiunta la registrazione a `ipsApiService.log`.

È stato aggiunto un param opzionale `serviceUrl` al servlet di generazione WSDL. Questo è particolarmente utile per i proxy di debug. Ad esempio: `http://<server>/scene7/webservice/IpsApi-2008-01-15.wsdl?serviceUrl=http://localhost:8081`

Implementata l&#39;operazione `getZipEntries`.

Sono stati implementati intervalli di ricerca e valori di confronto digitati per le condizioni del campo di sistema.

È stata aggiunta la costante di stringa del tipo di risorsa `'Asset'`, principalmente per consentire i campi di metadati tra risorse.

È stato implementato `trashState` param per `searchAssets`.

Implementata l&#39;operazione `getAssetPublishHistory`.

È stata aggiunta l&#39;intestazione SOAP `faultHttpStatusCode` opzionale per abilitare la gestione degli errori in Flex. Per Flex, utilizzare `<faultHttpStatusCode>200</faultHttpStatusCode>`. Il codice di stato predefinito per le risposte di errore è `500 (Internal Server Error)`.

Sono state aggiunte operazioni per ripristinare le risorse dal cestino e quelle vuote dal cestino.

Implementazione delle operazioni CRUD.

Aggiunto flag enabled al tipo `ImageMap` e all&#39;operazione `saveImageMap`.

È stato aggiunto il supporto per ottimizzare i processi di file rimanenti.

Aggiunto `setAssetsPublishState` per gli aggiornamenti dello stato di pubblicazione in blocco.

Aggiunto `ImageServingPublishSettings`, `getImageServingPublishSettings`, `setImageServingPublishSettings`.

Operazione `saveMetadataField` obsoleta a favore di nuove operazioni `createMetadataField` e `updateMetadataField`.

Implementata `deleteAssetsParam` operazione di eliminazione batch.

Implementata `moveAssetsParam` operazione di spostamento batch.

Implementata l&#39;operazione `deleteMetadataField`.

Implementate le operazioni `get/setImageRenderingPublishSettings`, `get/set/create/updateVignettePublishFormat`.

Implementato `getAssetCounts`.

È stato aggiunto il supporto a `setImageSetMembers` per l&#39;inclusione di membri `RenderSet` nelle risorse `ImageSet`.

Aggiunta operazione `replaceImage`.

Aggiunta operazione `copyImage`.

Sono stati aggiunti i campi `setUrlModifier` e `urlModifier/urlPostApplyModifier` per `LayerViewInfo`, `TemplateInfo` e `WatermarkInfo`.

Aggiunta operazione `createDerivedAsset`. Attualmente `ownerHandle` deve fare riferimento a una risorsa immagine e il tipo può essere `AdjustedView` o `LayerView`.

Aggiunta operazione `createTemplate`. Attualmente questo può essere chiamato per creare risorse Modello o Filigrana.

Impostazioni società IPS, `CompanySettings`, portate nell&#39;API dei servizi Web.

Aggiunto flag di filtro `excludeByproducts` all&#39;operazione `searchAssets`. Impostando questo flag su true, vengono eseguite le immagini `PSDlayer` e le immagini PDF estratti.

Aggiunta operazione `getGenerationInfo`.

Aggiunto il nome della proprietà `SystemMessage` all&#39;operazione `getProperty`.

Sono state modificate delle costanti stringa di tipo risorsa in modo che corrispondano ai campi corrispondenti Informazioni risorsa.

* WordDoc: Word
* ExcelDoc: Excel
* PowerPointDoc: PowerPoint
* RTFDoc: Rtf

È stato modificato il formato dei risultati delle operazioni batch per riepilogare successo, avvisi ed errori.

Implementata `batchSetAssetMetadata` l&#39;operazione di metadati batch.

Supporto implementato per dati specifici per l&#39;app.

È stato implementato il supporto per i flag booleani per `createTemplate`, `extendLayers` e `extractText` per i processi di caricamento per controllare il processo di elaborazione Photoshop (simile alle modifiche per l&#39;aggiunta di caricamenti di file).

Implementate le operazioni `setImageMaps` e `setZoomTargets`.

Implementate le operazioni `ViewerPreset`. I tipi riconosciuti sono:

* `VideoPlayer` (i visualizzatori vengono pubblicati solo per i video).
* `Brochure`
* `BasicZoom`
* `AdvancedZoom`
* `Spin`
* `Custom types`

Le interfacce del visualizzatore supportano due parametri: `skinFg` e `skinBg`. Il codice back-end eseguirà tutte le elaborazioni necessarie per mantenere la compatibilità con le versioni precedenti.

Implementata l&#39;operazione `getAssociatedAssets`.

È stato aggiunto il tipo di processo `ReprocessAssets` per consentire la rielaborazione dei file sorgente primari caricati in precedenza, inclusi il ripristino dei PDF e il riottimizzazione delle immagini.

Il tipo di campo `PropertySetType` è stato rinominato in `propertyType`. Ciò influisce sul parametro `createPropertySetType` e sulla risposta `getPropertySetType/getPropertySetTypes`.

È stata implementata l&#39;operazione `batchSetImageFields` per supportare l&#39;impostazione di dati utente immagine e altri campi immagine modificabili.

47 È stato aggiunto il campo fileSize ai vari tipi di informazioni sulle risorse:

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

Implementata l&#39;operazione `getActivePublishContexts`. Questa operazione restituisce un array di nomi di contesto di pubblicazione con server di pubblicazione attivi per la società specificata. I nomi correnti del contesto di pubblicazione sono:

* `ImageServing`
* `ImageRendering`
* `Video`

Implementata l&#39;operazione `getSearchStrings`. Restituisce un array di stringhe di ricerca per la risorsa specificata.

Sono stati aggiunti i parametri delle impostazioni internazionali per i processi e un meccanismo per impostare le impostazioni internazionali per le operazioni API. La stringa delle impostazioni internazionali deve essere formattata come `<language_code>[-<country_code>]`. Il codice della lingua è un codice di due lettere minuscoli, come specificato dallo standard ISO-639, e il codice del paese opzionale è un codice di due lettere maiuscolo come specificato dallo standard ISO-3166.

È stato aggiunto il parametro internazionale facoltativo all&#39;intestazione SOAP `authHeader` per impostare le impostazioni internazionali per le operazioni API. Se questo parametro non è presente, verrà utilizzata l&#39;intestazione HTTP `Accept-Language`. Se questa intestazione non è presente, verranno utilizzate le impostazioni internazionali predefinite per il server IPS.

È stato aggiunto il supporto get/set per i campi metadati fortemente tipizzati.

È stato implementato il supporto SOAP e dell&#39;intestazione HTTP per il controllo della risposta gzip.

È stato aggiunto il flag `gzipResponse` a `authHeader`. Se non è presente, l&#39;API controllerà anche l&#39;intestazione HTTP `Accept-Encoding`.

È stato aggiunto il supporto a searchAssets per verificare le condizioni dei campi di metadati fortemente tipizzati.

* Per tutti i tipi di campo, il valore può essere passato con un operatore di confronto delle stringhe ( `Equals, NotEquals, Contains, NotContains, StartsWith, EndsWith`)
* Per i campi booleani, `boolVal` può essere passato con il comando `Equals` op.
* Per i campi Int, `longVal` può essere passato con un operatore di confronto numerico ( `Equals, NotEquals, LessThan, LessThanEquals, GreaterThan, GreaterThanEquals`) o `minLong/maxLong` può essere passato con operazioni di intervallo numerico ( `Between, NotBetween`).
* Per i campi mobili, `doubleVal` può essere passato con un operatore di confronto numerico ( `Equals, NotEquals, LessThan, LessThanEquals, GreaterThan, GreaterThanEquals`) o `minDouble/maxDouble` può essere passato con operazioni di intervallo numerico ( `Between, NotBetween`).
* Per i campi Data, è possibile passare `dateVal` con un operatore di confronto numerico ( `Equals, NotEquals, LessThan, LessThanEquals, GreaterThan, GreaterThanEquals`) oppure passare minDate/maxDate con operazioni di intervallo numerico ( `Between, NotBetween`).

Sono stati aggiunti i campi descrizione, `jobSubType` e `originalJobName` al tipo `JobLog`.

* `originalJobName` è il nome del processo a cui è stato inviato  `submitJob` (senza suffissi di univocità o nomi di processi successivi).
* `jobSubType` è attualmente utilizzato solo da  `ImageServingPublishJob` processi (dove è uno dei  `full`,  `increment, fullwithsearch,` o  `fulloverride`).
* `description` è attualmente una stringa vuota per tutti i tipi di processo, ma alla fine conterrà informazioni di riepilogo sul processo, come il percorso di caricamento.

Inoltre, i seguenti campi non sono inclusi sia con `getJobLogs` che con `getJobLogDetails`. Nelle versioni precedenti erano disponibili solo con `getJobLogDetails`.

* `endDate` (se il processo è stato completato).
* `fileDuplicateCount` (in precedenza era sempre  `0` con  `getJobLogs`)
* `fileUpdateCount` (in precedenza era sempre  `0` con  `getJobLogs` e incluso in  `fileSuccessCount`; ora è suddivisa in campi separati).

È stato aggiunto il campo assetHandle al tipo `JobLogDetail`.

Aggiunto parametro di descrizione opzionale a `submitJob`. Questo viene passato per il recupero in `getScheduledJobs`, `getActiveJobs` e `getJobLogs`.

Campo di sistema SKU obsoleto. Il campo viene ignorato se viene passato come `SystemFieldCondition` a `searchAssets`.

È stato aggiunto il filtro `excludeAssetTypeArray` a `searchAssets`.

È stato aggiunto il tipo `MaskInfo` a `Asset`.

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
   <td colname="col2"> <p> file Adobe Illustrator. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> PostScript </span> </p> </td> 
   <td colname="col2"> <p>File EPS e PostScript. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> WordDoc  </span> </p> </td> 
   <td colname="col2"> <p>Documento di Microsoft Word per i file con estensione doc. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ExcelDoc  </span> </p> </td> 
   <td colname="col2"> <p>Documento Microsoft Excel per i file con estensione xls. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> PowerPointDoc  </span> </p> </td> 
   <td colname="col2"> <p>Documento Microsoft PowerPoint per i file con estensione ppt. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> RTFDoc  </span> </p> </td> 
   <td colname="col2"> <p>File RTF per file caricati con estensione rtf. </p> </td> 
  </tr> 
 </tbody> 
</table>

Sono state aggiunte opzioni aggiuntive a `UploadDirectoryJob` e `UploadUrlsJob` per controllare l&#39;elaborazione dei file PostScript,  Illustrator e PDF in modo indipendente. Tutti i processi esistenti forniranno i parametri necessari a ciascuno dei 3 oleodotti di lavorazione in modo che funzionino esattamente come avviene oggi. Il blocco `PostScriptOptions` originale viene utilizzato per impostare l&#39;elaborazione per  file Illustrator ed EPS/PS. Facoltativamente, è possibile specificare blocchi di opzioni di file specifici per specificare l&#39;elaborazione. L’elenco delle modifiche comprende:

<table id="table_D4E5ACCB2D144D05A5FA0129AA5F9344"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Field </p> </th> 
   <th colname="col2" class="entry"> <p>Parametro </p> </th> 
   <th colname="col3" class="entry"> <p>Valore </p> </th> 
   <th colname="col4" class="entry"> <p>Descrizione </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1" morerows="1"> <p> <span class="codeph"> PostScriptOptions  </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> process  </span> </p> </td> 
   <td colname="col3"> <p> 
     <ul id="ul_6BBFF026010F4913BD632B3312E17C4B"> 
      <li id="li_AA1131A68FB242C9A1380DE6F8F318C7"> <p> <span class="codeph"> Nessuno </span> </p> </li> 
      <li id="li_141F4C3FC9D34C9AABECA91394A82969"> <p> <span class="codeph"> Rasterizza  </span>(predefinito) </p> </li> 
     </ul> </p> </td> 
   <td colname="col4"> <p> 
     <ul id="ul_14D0A696DF4E408DA50E102057EB7AC7"> 
      <li id="li_D8AA718D9F504B91AB557216D2D7DBCC"> <p>Gestite solo la risorsa e non create derivati al momento del caricamento. </p> </li> 
      <li id="li_3F56CEABAB3E43EAB157C83583A2F58D"> <p>Eseguire il rendering del file EPS e PostScript in un'immagine alla risoluzione e allo spazio colore richiesti. </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> alfa </span> </p> <p>Facoltativo. </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;boolean&gt; </span> </p> </td> 
   <td colname="col4"> <p>Ha effetto quando si rasterizza il file in un’immagine. Crea uno sfondo trasparente se il file originale viene definito in questo modo per sovrapporre i logo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" morerows="3"> <p> <span class="codeph"> IllustratorOptions  </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> process  </span> </p> </td> 
   <td colname="col3"> <p> 
     <ul id="ul_C2F1000A01DE41678A8E1DDE0C8A0E97"> 
      <li id="li_53749049B383441A81CB427A5B5F26A8"> <span class="codeph"> Nessuno </span> </li> 
      <li id="li_C5332FC35E5C4687B30D4C1081015BB0"> <span class="codeph"> Rasterizza  </span> (predefinito) </li> 
     </ul> </p> </td> 
   <td colname="col4"> <p> 
     <ul id="ul_41924574773542B7BFC4989667C14E97"> 
      <li id="li_3886554059AB4F7383619A9CB7292E0E"> <p>Gestite solo la risorsa e non create derivati al momento del caricamento. </p> </li> 
      <li id="li_BF3F5E54484C46D8887CA48D8646648E"> <p>Eseguire il rendering del file in un'immagine alla risoluzione e allo spazio colore richiesti. </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> resolution  </span> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;integer&gt; </span> </p> </td> 
   <td colname="col4"> <p>Rasterizzazione della risoluzione. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> colorspace </span> </p> </td> 
   <td colname="col3"> <p> </p> </td> 
   <td colname="col4"> <p>Spazio colore di destinazione per il rendering. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> alfa </span> </p> <p>Facoltativo. </p> </td> 
   <td colname="col3"> <p> </p> </td> 
   <td colname="col4"> <p>Interessa quando il file viene rasterizzato in un’immagine. Crea uno sfondo trasparente se il file originale è definito in questo modo per la creazione di logo sovrapposti. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" morerows="4"> <p> <span class="codeph"> PDFOptions  </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> process  </span> </p> </td> 
   <td colname="col3"> <p> 
     <ul id="ul_EF9C27EE7A154DA890CB9E6BA174D767"> 
      <li id="li_0BB0FC1BA43043EEA1EA257E5D603978"> <p> <span class="codeph"> Nessuno </span> </p> </li> 
      <li id="li_E3FA07129C2646C7B98854C22CDAC1F0"> <p> <span class="codeph"> Rasterizza  </span> (predefinito) </p> </li> 
     </ul> </p> </td> 
   <td colname="col4"> <p> 
     <ul id="ul_84EE74454FF5434087A895F915E68103"> 
      <li id="li_4312A1CD5F4B44589678311A59536FA7"> <p>Gestite solo la risorsa e non create derivati al momento del caricamento. </p> </li> 
      <li id="li_06FBA83EA3F248E288F4790255802DE6"> <p>Eseguire il rendering del file in un'immagine alla risoluzione e allo spazio colore richiesti. </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> resolution  </span> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;integer&gt; </span> </p> </td> 
   <td colname="col4"> <p>Rasterizzazione della risoluzione. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> colorspace  </span> </p> </td> 
   <td colname="col3"> <p> </p> </td> 
   <td colname="col4"> <p>Spazio colore di destinazione per il rendering. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> pdfCatalog  </span> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;boolean&gt; </span> </p> </td> 
   <td colname="col4"> <p>Definisce se combinare un PDF di più pagine in un eCatalog dopo il rendering (il valore predefinito è true). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> extractSearchWords  </span> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;boolean&gt; </span> </p> </td> 
   <td colname="col4"> <p>Definisce se le parole del PDF vengono estratte nel database per essere successivamente distribuite a un server di ricerca (impostazione predefinita: false). </p> </td> 
  </tr> 
 </tbody> 
</table>

È inoltre possibile eseguire query da `getScheduledJobs`.

Modificata la proprietà di configurazione `webservice.gzip.response` in modo da ottenere uno dei seguenti valori:

<table id="table_FCBBF1643DC84F5CBF81DCA6B552E0C4"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Valore </p> </th> 
   <th colname="col2" class="entry"> <p>Descrizione </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> never  </span> </p> </td> 
   <td colname="col2"> <p>Non comprimete la risposta. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> soap  </span> </p> </td> 
   <td colname="col2"> <p>La risposta Gzip è valida solo se authHeader/gzipResponse è true. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> accetto  </span> </p> </td> 
   <td colname="col2"> <p>Gzip se authHeader/gzipResponse è true o se non è presente alcuna intestazione gzipResponse e l’intestazione HTTP Accept-Encoding include gzip. (Predefinito). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> always  </span> </p> </td> 
   <td colname="col2"> <p>Gzip response Always, indipendentemente dai valori dell'intestazione. Utilizzate questo valore solo a scopo di debug. </p> </td> 
  </tr> 
 </tbody> 
</table>

