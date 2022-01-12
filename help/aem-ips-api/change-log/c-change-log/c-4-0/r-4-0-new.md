---
title: Nuove aggiunte e modifiche
description: Descrive le modifiche nuove e implementate per l’API IPS v4.0.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: f07562a8-71e9-4d98-9d0c-5bb32a7e0ef1
source-git-commit: 50dddf148345d2ca5243d5d7108fefa56d23dad6
workflow-type: tm+mt
source-wordcount: '1206'
ht-degree: 1%

---

# Nuove aggiunte e modifiche{#new-additions-and-changes}

Descrive le modifiche nuove e implementate per l’API IPS v4.0.

Implementazione di versioni API affiancate con WSDL e namespace dello schema separati.

* Versioni API precedenti: `IpsApi.wsdl, http://www.scene7.com/IpsApi/xsd`.
* Versione SPS 4.0: `IpsApi-2008-01-15.wsdl, http://www.scene7.com/IpsApi/xsd/2008-01-15`.

Aggiunto `PostScriptOptions/alpha` campo .

Aggiunto `VideoRootUrl` e `SwfRootUrl` proprietà per `getProperty` funzionamento.

Aggiunto facoltativo `appName` e `appVersion` parametri a `authHeader` per tenere traccia dell&#39;applicazione chiamante. Accesso aggiunto a `ipsApiService.log`.

È stato aggiunto un facoltativo `serviceUrl` al servlet di generazione WSDL. Questo parametro è utile per i proxy di debug. Ad esempio: `http://<server>/scene7/webservice/IpsApi-2008-01-15.wsdl?serviceUrl=http://localhost:8081`

Implementato `getZipEntries` funzionamento.

Sono stati implementati intervalli di ricerca e valori di confronto tipizzati per le condizioni dei campi di sistema.

Aggiunto `'Asset'` costante della stringa del tipo di risorsa, principalmente per consentire campi di metadati tra risorse diverse.

Implementato `trashState` param for `searchAssets`.

Implementato `getAssetPublishHistory` funzionamento.

Aggiunto facoltativo `faultHttpStatusCode` Intestazione SOAP per abilitare la gestione degli errori in Flex. Per Flex, utilizza `<faultHttpStatusCode>200</faultHttpStatusCode>`. Il codice di stato predefinito per le risposte ai guasti è `500 (Internal Server Error)`.

Sono state aggiunte operazioni per ripristinare le risorse dal cestino e le risorse vuote dal cestino.

Implementazione delle operazioni CRUD.

È stato aggiunto il flag abilitato a `ImageMap` tipo e `saveImageMap` funzionamento.

È stato aggiunto il supporto per i lavori Ottimizza file rimanenti.

Aggiunto `setAssetsPublishState` per aggiornamenti di stato di pubblicazione in blocco.

Aggiunto `ImageServingPublishSettings`, `getImageServingPublishSettings`, `setImageServingPublishSettings`.

Obsoleto `saveMetadataField` operazione a favore di nuove `createMetadataField` e `updateMetadataField` operazioni.

Implementato `deleteAssetsParam` operazione di eliminazione batch.

Implementato `moveAssetsParam` operazione di spostamento in batch.

Implementato `deleteMetadataField` funzionamento.

Implementato `get/setImageRenderingPublishSettings`, `get/set/create/updateVignettePublishFormat` operazioni.

Implementato `getAssetCounts`.

È stato aggiunto il supporto a `setImageSetMembers` per includere `RenderSet` membri `ImageSet` risorse.

Aggiunto `replaceImage` funzionamento.

Aggiunto `copyImage` funzionamento.

Aggiunto `setUrlModifier` funzionamento e `urlModifier/urlPostApplyModifier` campi per `LayerViewInfo`, `TemplateInfo`e `WatermarkInfo`.

Aggiunto `createDerivedAsset` funzionamento. Attualmente `ownerHandle` deve fare riferimento a una risorsa Immagine e il tipo può essere `AdjustedView` o `LayerView`.

Aggiunto `createTemplate` funzionamento. Richiama per creare le risorse Modello o Filigrana.

impostazioni aziendali IPS, `CompanySettings`, è stato spostato nell’API dei servizi Web.

Aggiunto `excludeByproducts` flag di filtro a `searchAssets` funzionamento. Impostazione di questo flag su esecuzioni vere `PSDlayer` immagini e PDF strappate.

Aggiunto `getGenerationInfo` funzionamento.

Aggiunto `SystemMessage` nome della proprietà in `getProperty` funzionamento.

Sono state modificate le costanti della stringa di alcuni tipi di risorsa in modo che corrispondano ai campi corrispondenti di Informazioni risorsa.

* WordDoc: Parola
* Documento Excel: Excel
* PowerPointDoc: PowerPoint
* RTFDoc: Rtf

Formato del risultato modificato delle operazioni batch per riepilogare il successo, gli avvisi e gli errori.

Implementato `batchSetAssetMetadata` funzionamento dei metadati batch.

È stato implementato il supporto per dati specifici per l’app.

È stato implementato il supporto per i flag booleani per `createTemplate`, `extendLayers`e `extractText` per i processi di caricamento per controllare il processo di elaborazione di Photoshop (simile alle modifiche per l’aggiunta di caricamenti di file).

Implementato `setImageMaps` e `setZoomTargets` operazioni.

Implementato `ViewerPreset` operazioni. I tipi riconosciuti sono:

* `VideoPlayer` (Il video pubblica solo questi visualizzatori.)
* `Brochure`
* `BasicZoom`
* `AdvancedZoom`
* `Spin`
* `Custom types`

Le interfacce del visualizzatore supportano due parametri: `skinFg` e `skinBg`. Il codice di backend esegue tutte le elaborazioni necessarie per mantenere la compatibilità con le versioni precedenti.

Implementato `getAssociatedAssets` funzionamento.

Aggiunto `ReprocessAssets` tipo di processo per consentire la rielaborazione dei file di origine primari caricati in precedenza, inclusi il recupero dei PDF e la riottimizzazione delle immagini.

Rinominato `PropertySetType` tipo di campo a `propertyType`. Questa ridenominazione influisce sul `createPropertySetType` e `getPropertySetType/getPropertySetTypes` risposta.

Implementato `batchSetImageFields` per supportare l’impostazione dei dati utente dell’immagine e di altri campi immagine modificabili.

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

Implementato `getActivePublishContexts` funzionamento. Questa operazione restituisce un array di nomi di contesto di pubblicazione con server di pubblicazione attivi per la società specificata. I nomi di contesto di pubblicazione correnti sono:

* `ImageServing`
* `ImageRendering`
* `Video`

Implementato `getSearchStrings` funzionamento. Restituisce una matrice di stringhe di ricerca per la risorsa specificata.

Sono stati aggiunti i parametri internazionali per i processi e un meccanismo per impostare le impostazioni internazionali per le operazioni API. La stringa delle impostazioni internazionali deve essere formattata come `<language_code>[-<country_code>]`. Il codice della lingua è un codice a due lettere minuscolo, come specificato dallo standard ISO-639, e il codice del paese opzionale è un codice a due lettere maiuscolo come specificato dallo standard ISO-3166.

È stato aggiunto il parametro di impostazione internazionale opzionale al `authHeader` Intestazione SOAP per impostare le impostazioni internazionali per le operazioni API. Se questo parametro non è presente, l&#39;intestazione HTTP `Accept-Language` viene utilizzato. Se questa intestazione non è presente, verranno utilizzate le impostazioni internazionali predefinite per il server IPS.

È stato aggiunto il supporto get/set per i campi metadati fortemente tipizzati.

Implementazione del supporto per l’intestazione SOAP e HTTP per il controllo della risposta gzip.

Aggiunto `gzipResponse` flag to `authHeader`. Se non è presente, l’API controlla il codice HTTP `Accept-Encoding` intestazione.

È stato aggiunto il supporto a searchAssets per le condizioni dei campi di metadati fortemente tipizzati.

* Per tutti i tipi di campo, il valore può essere passato con un operatore di confronto stringa ( `Equals, NotEquals, Contains, NotContains, StartsWith, EndsWith`)
* Per i campi booleani, `boolVal` possono essere trasmessi con `Equals` op.
* Per i campi Int, `longVal` può essere passato con un operatore di confronto numerico ( `Equals, NotEquals, LessThan, LessThanEquals, GreaterThan, GreaterThanEquals`) o `minLong/maxLong` può essere passato con operazioni di intervallo numerico ( `Between, NotBetween`).
* Per i campi mobili, `doubleVal` può essere passato con un operatore di confronto numerico ( `Equals, NotEquals, LessThan, LessThanEquals, GreaterThan, GreaterThanEquals`) o `minDouble/maxDouble` può essere passato con operazioni di intervallo numerico ( `Between, NotBetween`).
* Per i campi Data è possibile trasmettere `dateVal` con un operatore di confronto numerico ( `Equals, NotEquals, LessThan, LessThanEquals, GreaterThan, GreaterThanEquals`) oppure puoi passare minDate/maxDate con operazioni di intervallo numerico ( `Between, NotBetween`).

È stata aggiunta la descrizione, `jobSubType`e `originalJobName` campi `JobLog` digitare.

* `originalJobName` è il nome del processo inviato a `submitJob` (senza suffissi univoci o nomi di lavoro successivi).
* `jobSubType` viene utilizzato solo da `ImageServingPublishJob` posti di lavoro `full`, `increment, fullwithsearch,` o `fulloverride`).
* `description` è una stringa vuota per tutti i tipi di processo, ma alla fine contiene informazioni sul processo di riepilogo, come il percorso di caricamento.

Inoltre, i campi seguenti non sono inclusi in entrambi `getJobLogs` e `getJobLogDetails`. Nelle versioni precedenti, erano disponibili solo con `getJobLogDetails`.

* `endDate` (se il processo è stato completato).
* `fileDuplicateCount` (in precedenza era sempre `0` con `getJobLogs`)
* `fileUpdateCount` (in precedenza era sempre `0` con `getJobLogs` e incluso in `fileSuccessCount`; ora è suddiviso in campi separati).

È stato aggiunto il campo assetHandle a `JobLogDetail` digitare.

È stato aggiunto il parametro di descrizione opzionale a `submitJob`. Questo parametro viene trasmesso per il recupero in `getScheduledJobs`, `getActiveJobs`e `getJobLogs`.

Il campo del sistema SKU è stato dichiarato obsoleto. Il campo viene ignorato se viene passato come `SystemFieldCondition` a `searchAssets`.

Aggiunto `excludeAssetTypeArray` filtrare `searchAssets`.

Aggiunto `MaskInfo` digitare `Asset`.

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
   <td colname="col2"> <p>File RTF per file caricati che terminano con .rtf. </p> </td> 
  </tr> 
 </tbody> 
</table>

Sono state aggiunte opzioni aggiuntive a `UploadDirectoryJob` e `UploadUrlsJob` per controllare l’elaborazione dei file Postscript, Illustrator e PDF in modo indipendente. Tutti i processi esistenti forniscono i parametri necessari a ciascuna delle tre pipeline di elaborazione in modo che funzionino esattamente come avviene oggi. L&#39;originale `PostScriptOptions` block viene utilizzato per impostare l&#39;elaborazione per i file Illustrator e EPS/PS. Facoltativamente, è possibile fornire blocchi di opzioni di file specifici per specificare l’elaborazione. L’elenco delle modifiche include:

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
   <td colname="col1" morerows="1"> <p> <span class="codeph"> OpzioniPostScript </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> processo </span> </p> </td> 
   <td colname="col3"> <p> 
     <ul id="ul_6BBFF026010F4913BD632B3312E17C4B"> 
      <li id="li_AA1131A68FB242C9A1380DE6F8F318C7"> <p> <span class="codeph"> Nessuno </span> </p> </li> 
      <li id="li_141F4C3FC9D34C9AABECA91394A82969"> <p> <span class="codeph"> Rasterizza </span>(predefinito) </p> </li> 
     </ul> </p> </td> 
   <td colname="col4"> <p> 
     <ul id="ul_14D0A696DF4E408DA50E102057EB7AC7"> 
      <li id="li_D8AA718D9F504B91AB557216D2D7DBCC"> <p>Gestisci solo la risorsa e non creare derivati al momento del caricamento. </p> </li> 
      <li id="li_3F56CEABAB3E43EAB157C83583A2F58D"> <p>Esegui il rendering del file EPS e PostScript in un'immagine con la risoluzione e lo spazio colore richiesti. </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> alfa </span> </p> <p>Facoltativo. </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;boolean&gt; </span> </p> </td> 
   <td colname="col4"> <p>Ha effetto quando il file viene rasterizzato in un’immagine. Crea uno sfondo trasparente se il file originale è definito in questo modo per sovrapporre i loghi. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" morerows="3"> <p> <span class="codeph"> IllustratorOptions </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> processo </span> </p> </td> 
   <td colname="col3"> <p> 
     <ul id="ul_C2F1000A01DE41678A8E1DDE0C8A0E97"> 
      <li id="li_53749049B383441A81CB427A5B5F26A8"> <span class="codeph"> Nessuno </span> </li> 
      <li id="li_C5332FC35E5C4687B30D4C1081015BB0"> <span class="codeph"> Rasterizza </span> (predefinito) </li> 
     </ul> </p> </td> 
   <td colname="col4"> <p> 
     <ul id="ul_41924574773542B7BFC4989667C14E97"> 
      <li id="li_3886554059AB4F7383619A9CB7292E0E"> <p>Gestisci solo la risorsa e non creare derivati al momento del caricamento. </p> </li> 
      <li id="li_BF3F5E54484C46D8887CA48D8646648E"> <p>Esegui il rendering del file in un'immagine alla risoluzione e allo spazio colore prescritti. </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> resolution </span> </p> </td> 
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
   <td colname="col4"> <p>Ha effetto quando il file viene rasterizzato in un’immagine. Crea uno sfondo trasparente se il file originale è definito in questo modo per creare loghi sovrapposti. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" morerows="4"> <p> <span class="codeph"> PDFOptions </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> processo </span> </p> </td> 
   <td colname="col3"> <p> 
     <ul id="ul_EF9C27EE7A154DA890CB9E6BA174D767"> 
      <li id="li_0BB0FC1BA43043EEA1EA257E5D603978"> <p> <span class="codeph"> Nessuno </span> </p> </li> 
      <li id="li_E3FA07129C2646C7B98854C22CDAC1F0"> <p> <span class="codeph"> Rasterizza </span> (predefinito) </p> </li> 
     </ul> </p> </td> 
   <td colname="col4"> <p> 
     <ul id="ul_84EE74454FF5434087A895F915E68103"> 
      <li id="li_4312A1CD5F4B44589678311A59536FA7"> <p>Gestisci solo la risorsa e non creare derivati al momento del caricamento. </p> </li> 
      <li id="li_06FBA83EA3F248E288F4790255802DE6"> <p>Esegui il rendering del file in un'immagine alla risoluzione e allo spazio colore prescritti. </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> resolution </span> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;integer&gt; </span> </p> </td> 
   <td colname="col4"> <p>Risoluzione raster. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> colorspace </span> </p> </td> 
   <td colname="col3"> <p> </p> </td> 
   <td colname="col4"> <p>Spazio colore di destinazione per il rendering. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> pdfCatalog </span> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;boolean&gt; </span> </p> </td> 
   <td colname="col4"> <p>Definisce se combinare un PDF di pagina multiplo in un eCatalog dopo il rendering (l’impostazione predefinita è true). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> extractSearchWords </span> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;boolean&gt; </span> </p> </td> 
   <td colname="col4"> <p>Definisce se le parole di PDF vengono estratte nel database per essere successivamente fornite a un server di ricerca (l'impostazione predefinita è false). </p> </td> 
  </tr> 
 </tbody> 
</table>

Puoi anche eseguire query da `getScheduledJobs`.

Modificato il `webservice.gzip.response` proprietà di configurazione per ottenere uno dei seguenti valori:

<table id="table_FCBBF1643DC84F5CBF81DCA6B552E0C4"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Valore </p> </th> 
   <th colname="col2" class="entry"> <p>Descrizione </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> mai </span> </p> </td> 
   <td colname="col2"> <p>Non comprimere la risposta. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> sapone </span> </p> </td> 
   <td colname="col2"> <p>Risposta Gzip solo se authHeader/gzipResponse è true. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> accettare </span> </p> </td> 
   <td colname="col2"> <p>Gzip se authHeader/gzipResponse è true o se non è presente alcuna intestazione gzipResponse e l'intestazione HTTP Accept-Encoding include gzip. (Predefinito). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> sempre </span> </p> </td> 
   <td colname="col2"> <p>Gzip sempre la risposta, indipendentemente dai valori dell'intestazione. Utilizzare questo valore solo a scopo di debug. </p> </td> 
  </tr> 
 </tbody> 
</table>
