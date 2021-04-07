---
description: Descrive le modifiche nuove e implementate per l’API IPS v4.0.
solution: Experience Manager
title: Nuove aggiunte e modifiche
feature: Dynamic Media Classic, SDK/API
role: Sviluppatore,Amministratore
exl-id: f07562a8-71e9-4d98-9d0c-5bb32a7e0ef1
translation-type: tm+mt
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '1227'
ht-degree: 1%

---

# Nuove aggiunte e modifiche{#new-additions-and-changes}

Descrive le modifiche nuove e implementate per l’API IPS v4.0.

Implementazione di versioni API affiancate con WSDL e namespace dello schema separati.

* Versioni API precedenti: `IpsApi.wsdl, http://www.scene7.com/IpsApi/xsd`.
* Versione SPS 4.0: `IpsApi-2008-01-15.wsdl, http://www.scene7.com/IpsApi/xsd/2008-01-15`.

È stato aggiunto il campo `PostScriptOptions/alpha` .

Sono state aggiunte le proprietà `VideoRootUrl` e `SwfRootUrl` per l’operazione `getProperty`.

Sono stati aggiunti parametri `appName` e `appVersion` facoltativi a `authHeader` per tenere traccia dell&#39;applicazione chiamante. È stata aggiunta la registrazione a `ipsApiService.log`.

È stato aggiunto un parametro opzionale `serviceUrl` al servlet di generazione WSDL. Questo è particolarmente utile per i proxy di debug. Ad esempio: `http://<server>/scene7/webservice/IpsApi-2008-01-15.wsdl?serviceUrl=http://localhost:8081`

Implementazione dell&#39;operazione `getZipEntries` .

Sono stati implementati intervalli di ricerca e valori di confronto tipizzati per le condizioni dei campi di sistema.

È stata aggiunta la costante di stringa del tipo di risorsa `'Asset'` , principalmente per consentire i campi di metadati tra risorse diverse.

È stato implementato il parametro `trashState` per `searchAssets`.

Implementazione dell&#39;operazione `getAssetPublishHistory` .

È stata aggiunta l’intestazione SOAP opzionale `faultHttpStatusCode` per abilitare la gestione degli errori in Flex. Per Flex, utilizza `<faultHttpStatusCode>200</faultHttpStatusCode>`. Il codice di stato predefinito per le risposte agli errori è `500 (Internal Server Error)`.

Sono state aggiunte operazioni per ripristinare le risorse dal cestino e le risorse vuote dal cestino.

Implementazione delle operazioni CRUD.

È stato aggiunto il flag abilitato al tipo `ImageMap` e all&#39;operazione `saveImageMap`.

È stato aggiunto il supporto per i lavori Ottimizza file rimanenti.

È stato aggiunto `setAssetsPublishState` per gli aggiornamenti dello stato di pubblicazione in blocco.

Sono stati aggiunti `ImageServingPublishSettings`, `getImageServingPublishSettings`, `setImageServingPublishSettings`.

Operazione `saveMetadataField` obsoleta a favore di nuove operazioni `createMetadataField` e `updateMetadataField`.

Implementazione dell’ `deleteAssetsParam` operazione di eliminazione batch.

Implementazione dell&#39;operazione di spostamento in batch `moveAssetsParam`.

Implementazione dell&#39;operazione `deleteMetadataField` .

Implementazione delle operazioni `get/setImageRenderingPublishSettings`, `get/set/create/updateVignettePublishFormat` .

Implementato `getAssetCounts`.

È stato aggiunto il supporto a `setImageSetMembers` per l’inclusione di membri `RenderSet` nelle risorse `ImageSet`.

È stata aggiunta l’operazione `replaceImage` .

È stata aggiunta l’operazione `copyImage` .

Sono stati aggiunti i campi `setUrlModifier` e `urlModifier/urlPostApplyModifier` per `LayerViewInfo`, `TemplateInfo` e `WatermarkInfo`.

È stata aggiunta l’operazione `createDerivedAsset` . Attualmente il `ownerHandle` deve fare riferimento a una risorsa immagine e il tipo può essere `AdjustedView` o `LayerView`.

È stata aggiunta l’operazione `createTemplate` . Attualmente è possibile chiamarlo per creare risorse Modello o Filigrana.

Impostazioni società IPS `CompanySettings` trasferite all&#39;API dei servizi Web.

Aggiunta del flag di filtro `excludeByproducts` all&#39;operazione `searchAssets`. L’impostazione di questo flag su true esegue le immagini `PSDlayer` e le immagini PDF strappate.

È stata aggiunta l’operazione `getGenerationInfo` .

Aggiunta del nome della proprietà `SystemMessage` all&#39;operazione `getProperty`.

Sono state modificate le costanti della stringa di alcuni tipi di risorsa in modo che corrispondano ai campi corrispondenti di Informazioni risorsa.

* WordDoc: Parola
* Documento Excel: Excel
* PowerPointDoc: PowerPoint
* RTFDoc: Rtf

Formato del risultato modificato delle operazioni batch per riepilogare il successo, gli avvisi e gli errori.

Implementazione dell&#39;operazione dei metadati batch `batchSetAssetMetadata`.

È stato implementato il supporto per dati specifici per l’app.

È stato implementato il supporto per i flag booleani per `createTemplate`, `extendLayers` e `extractText` per i processi di caricamento per controllare il processo di elaborazione di Photoshop (simile alle modifiche per l’aggiunta di file caricati).

Implementazione delle operazioni `setImageMaps` e `setZoomTargets` .

Implementazione delle operazioni `ViewerPreset` . I tipi riconosciuti sono:

* `VideoPlayer` (Il video pubblica solo questi visualizzatori.)
* `Brochure`
* `BasicZoom`
* `AdvancedZoom`
* `Spin`
* `Custom types`

Le interfacce del visualizzatore supportano due parametri: `skinFg` e `skinBg`. Il codice di backend eseguirà tutta l’elaborazione necessaria per mantenere la compatibilità con le versioni precedenti.

Implementazione dell&#39;operazione `getAssociatedAssets` .

È stato aggiunto il tipo di processo `ReprocessAssets` per consentire la rielaborazione dei file di origine primari caricati in precedenza, inclusi la cancellazione dei PDF e la riottimizzazione delle immagini.

Il tipo di campo `PropertySetType` è stato rinominato `propertyType`. Questo influisce sul parametro `createPropertySetType` e sulla risposta `getPropertySetType/getPropertySetTypes` .

È stata implementata l’operazione `batchSetImageFields` per supportare l’impostazione dei dati utente dell’immagine e di altri campi immagine modificabili.

47 Campo fileSize aggiunto a vari tipi di informazioni sulle risorse:

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

Implementazione dell&#39;operazione `getActivePublishContexts` . Questa operazione restituisce un array di nomi di contesto di pubblicazione con server di pubblicazione attivi per la società specificata. I nomi di contesto di pubblicazione correnti sono:

* `ImageServing`
* `ImageRendering`
* `Video`

Implementazione dell&#39;operazione `getSearchStrings` . Restituisce una matrice di stringhe di ricerca per la risorsa specificata.

Sono stati aggiunti i parametri internazionali per i processi e un meccanismo per impostare le impostazioni internazionali per le operazioni API. La stringa locale deve essere formattata come `<language_code>[-<country_code>]`. Il codice della lingua è un codice a due lettere minuscolo, come specificato dallo standard ISO-639, e il codice del paese opzionale è un codice a due lettere maiuscolo come specificato dallo standard ISO-3166.

Aggiunta del parametro locale opzionale all&#39;intestazione SOAP `authHeader` per impostare le impostazioni internazionali per le operazioni API. Se questo parametro non è presente, verrà utilizzata l’intestazione HTTP `Accept-Language`. Se questa intestazione non è presente, verranno utilizzate le impostazioni internazionali predefinite per il server IPS.

È stato aggiunto il supporto get/set per i campi metadati fortemente tipizzati.

Implementazione del supporto per l’intestazione SOAP e HTTP per il controllo della risposta gzip.

È stato aggiunto il flag `gzipResponse` a `authHeader`. Se non è presente, l’API controllerà anche l’intestazione HTTP `Accept-Encoding` .

È stato aggiunto il supporto a searchAssets per le condizioni dei campi di metadati fortemente tipizzati.

* Per tutti i tipi di campo, il valore può essere passato con un operatore di confronto stringa ( `Equals, NotEquals, Contains, NotContains, StartsWith, EndsWith`)
* Per i campi booleani, `boolVal` può essere passato con `Equals` op.
* Per i campi Int, è possibile trasmettere `longVal` con un operatore di confronto numerico ( `Equals, NotEquals, LessThan, LessThanEquals, GreaterThan, GreaterThanEquals`) o `minLong/maxLong` con operazioni di intervallo numerico ( `Between, NotBetween`).
* Per i campi Mobile, `doubleVal` può essere passato con un operatore di confronto numerico ( `Equals, NotEquals, LessThan, LessThanEquals, GreaterThan, GreaterThanEquals`) o `minDouble/maxDouble` può essere passato con operazioni di intervallo numerico ( `Between, NotBetween`).
* Per i campi Data, è possibile passare `dateVal` con un operatore di confronto numerico ( `Equals, NotEquals, LessThan, LessThanEquals, GreaterThan, GreaterThanEquals`) oppure passare minDate/maxDate con operazioni di intervallo numerico ( `Between, NotBetween`).

Sono stati aggiunti campi descrizione, `jobSubType` e `originalJobName` al tipo `JobLog`.

* `originalJobName` è il nome del processo inviato a  `submitJob` (senza suffissi di univocità o nomi di lavoro successivi).
* `jobSubType` è attualmente utilizzato solo dai  `ImageServingPublishJob` lavori (dove è uno dei  `full`,  `increment, fullwithsearch,` o  `fulloverride`).
* `description` è attualmente una stringa vuota per tutti i tipi di processo, ma alla fine conterrà informazioni sul processo di riepilogo, come il percorso di caricamento.

Inoltre, i campi seguenti non sono inclusi sia con `getJobLogs` che con `getJobLogDetails`. Nelle versioni precedenti erano disponibili solo con `getJobLogDetails`.

* `endDate` (se il processo è stato completato).
* `fileDuplicateCount` (in precedenza era sempre  `0` con  `getJobLogs`)
* `fileUpdateCount` (in precedenza era sempre  `0` con  `getJobLogs` e incluso in  `fileSuccessCount`; ora è suddiviso in campi separati).

È stato aggiunto il campo assetHandle al tipo `JobLogDetail` .

È stato aggiunto il parametro di descrizione opzionale a `submitJob`. Questo viene trasmesso per il recupero in `getScheduledJobs`, `getActiveJobs` e `getJobLogs`.

Il campo del sistema SKU è stato dichiarato obsoleto. Il campo viene ignorato se viene passato come `SystemFieldCondition` a `searchAssets`.

È stato aggiunto il filtro `excludeAssetTypeArray` a `searchAssets`.

È stato aggiunto il tipo `MaskInfo` a `Asset`.

Sono stati aggiunti nuovi tipi di risorse per la gestione da parte di IPS:

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
   <td colname="col2"> <p>File Adobe Illustrator. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> PostScript </span> </p> </td> 
   <td colname="col2"> <p>File EPS e PostScript. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> WordDoc  </span> </p> </td> 
   <td colname="col2"> <p>Documento di Microsoft Word per i file che terminano con .doc. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ExcelDoc  </span> </p> </td> 
   <td colname="col2"> <p>Documento di Microsoft Excel per i file che terminano con .xls. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> PowerPointDoc  </span> </p> </td> 
   <td colname="col2"> <p>Documento di Microsoft PowerPoint per i file che terminano con .ppt. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> RTFDoc  </span> </p> </td> 
   <td colname="col2"> <p>File RTF per file caricati che terminano con .rtf. </p> </td> 
  </tr> 
 </tbody> 
</table>

Sono state aggiunte opzioni aggiuntive a `UploadDirectoryJob` e `UploadUrlsJob` per controllare l’elaborazione di file Postscript, Illustrator e PDF in modo indipendente. Tutti i lavori esistenti forniranno i parametri necessari a ciascuna delle tre pipeline di elaborazione in modo che funzionino esattamente come avviene oggi. Il blocco originale `PostScriptOptions` viene utilizzato per impostare l&#39;elaborazione per i file Illustrator ed EPS/PS. Facoltativamente, è possibile fornire blocchi di opzioni di file specifici per specificare l’elaborazione. L’elenco delle modifiche include:

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
   <td colname="col1" morerows="1"> <p> <span class="codeph"> OpzioniPostScript  </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> processo  </span> </p> </td> 
   <td colname="col3"> <p> 
     <ul id="ul_6BBFF026010F4913BD632B3312E17C4B"> 
      <li id="li_AA1131A68FB242C9A1380DE6F8F318C7"> <p> <span class="codeph"> Nessuno </span> </p> </li> 
      <li id="li_141F4C3FC9D34C9AABECA91394A82969"> <p> <span class="codeph"> Rasterize  </span>(predefinito) </p> </li> 
     </ul> </p> </td> 
   <td colname="col4"> <p> 
     <ul id="ul_14D0A696DF4E408DA50E102057EB7AC7"> 
      <li id="li_D8AA718D9F504B91AB557216D2D7DBCC"> <p>Gestisci solo la risorsa e non creare derivati al momento del caricamento. </p> </li> 
      <li id="li_3F56CEABAB3E43EAB157C83583A2F58D"> <p>Esegui il rendering del file EPS e PostScript in un'immagine alla risoluzione e allo spazio colore prescritti. </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> alfa </span> </p> <p>Facoltativo. </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;boolean&gt; </span> </p> </td> 
   <td colname="col4"> <p>Ha effetto quando il file viene rasterizzato in un’immagine. Crea uno sfondo trasparente se il file originale è definito in questo modo per sovrapporre i loghi. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" morerows="3"> <p> <span class="codeph"> IllustratorOptions  </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> processo  </span> </p> </td> 
   <td colname="col3"> <p> 
     <ul id="ul_C2F1000A01DE41678A8E1DDE0C8A0E97"> 
      <li id="li_53749049B383441A81CB427A5B5F26A8"> <span class="codeph"> Nessuno </span> </li> 
      <li id="li_C5332FC35E5C4687B30D4C1081015BB0"> <span class="codeph"> Rasterize  </span> (predefinito) </li> 
     </ul> </p> </td> 
   <td colname="col4"> <p> 
     <ul id="ul_41924574773542B7BFC4989667C14E97"> 
      <li id="li_3886554059AB4F7383619A9CB7292E0E"> <p>Gestisci solo la risorsa e non creare derivati al momento del caricamento. </p> </li> 
      <li id="li_BF3F5E54484C46D8887CA48D8646648E"> <p>Esegui il rendering del file in un'immagine alla risoluzione e allo spazio colore prescritti. </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> resolution  </span> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;integer&gt; </span> </p> </td> 
   <td colname="col4"> <p>Risoluzione raster. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> colorspace </span> </p> </td> 
   <td colname="col3"> <p> </p> </td> 
   <td colname="col4"> <p>Spazio colore di destinazione per il rendering. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> alfa </span> </p> <p>Facoltativo. </p> </td> 
   <td colname="col3"> <p> </p> </td> 
   <td colname="col4"> <p>Interessa quando rasterizza il file in un’immagine. Crea uno sfondo trasparente se il file originale è definito in questo modo per creare loghi sovrapposti. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" morerows="4"> <p> <span class="codeph"> PDFOptions  </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> processo  </span> </p> </td> 
   <td colname="col3"> <p> 
     <ul id="ul_EF9C27EE7A154DA890CB9E6BA174D767"> 
      <li id="li_0BB0FC1BA43043EEA1EA257E5D603978"> <p> <span class="codeph"> Nessuno </span> </p> </li> 
      <li id="li_E3FA07129C2646C7B98854C22CDAC1F0"> <p> <span class="codeph"> Rasterize  </span> (predefinito) </p> </li> 
     </ul> </p> </td> 
   <td colname="col4"> <p> 
     <ul id="ul_84EE74454FF5434087A895F915E68103"> 
      <li id="li_4312A1CD5F4B44589678311A59536FA7"> <p>Gestisci solo la risorsa e non creare derivati al momento del caricamento. </p> </li> 
      <li id="li_06FBA83EA3F248E288F4790255802DE6"> <p>Esegui il rendering del file in un'immagine alla risoluzione e allo spazio colore prescritti. </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> resolution  </span> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;integer&gt; </span> </p> </td> 
   <td colname="col4"> <p>Risoluzione raster. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> colorspace  </span> </p> </td> 
   <td colname="col3"> <p> </p> </td> 
   <td colname="col4"> <p>Spazio colore di destinazione per il rendering. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> pdfCatalog  </span> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;boolean&gt; </span> </p> </td> 
   <td colname="col4"> <p>Definisce se combinare un PDF a più pagine in un eCatalog dopo il rendering (l’impostazione predefinita è true). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> extractSearchWords  </span> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;boolean&gt; </span> </p> </td> 
   <td colname="col4"> <p>Definisce se le parole del PDF vengono estratte nel database per un successivo invio a un server di ricerca (l'impostazione predefinita è false). </p> </td> 
  </tr> 
 </tbody> 
</table>

Puoi anche eseguire query da `getScheduledJobs`.

È stata modificata la proprietà di configurazione `webservice.gzip.response` in modo che prenda uno dei seguenti valori:

<table id="table_FCBBF1643DC84F5CBF81DCA6B552E0C4"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Valore </p> </th> 
   <th colname="col2" class="entry"> <p>Descrizione </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> mai  </span> </p> </td> 
   <td colname="col2"> <p>Non comprimere la risposta. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> sapone  </span> </p> </td> 
   <td colname="col2"> <p>Risposta Gzip solo se authHeader/gzipResponse è true. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> accettare  </span> </p> </td> 
   <td colname="col2"> <p>Gzip se authHeader/gzipResponse è true o se non è presente alcuna intestazione gzipResponse e l'intestazione HTTP Accept-Encoding include gzip. (Predefinito). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> sempre  </span> </p> </td> 
   <td colname="col2"> <p>Gzip sempre la risposta, indipendentemente dai valori dell'intestazione. Utilizzare questo valore solo a scopo di debug. </p> </td> 
  </tr> 
 </tbody> 
</table>
