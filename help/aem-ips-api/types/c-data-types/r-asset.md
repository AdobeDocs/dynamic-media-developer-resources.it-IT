---
description: Un oggetto o un contenitore nella gerarchia delle cartelle.
solution: Experience Manager
title: Risorsa
feature: Dynamic Media Classic,SDK/API,Gestione risorse
role: Developer,Administrator
exl-id: 943e653a-ed30-4c75-9bad-6ef5b72f5219
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '443'
ht-degree: 1%

---

# Risorsa{#asset}

Un oggetto o un contenitore nella gerarchia delle cartelle.

Sintassi

## Parametri {#section-0f2abb29deaf4d73bbbd0a5a2dc9ca3b}

<table id="table_C58EF9963CB34179A9D6C9F0F6FF24F2"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Nome </th> 
   <th colname="col2" class="entry"> Tipo </th> 
   <th colname="col3" class="entry"> Descrizione </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> acoInfo</span> </span> </td> 
   <td colname="col2"> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> animatedGifInfo</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> tipi:AnimatedGifInfo</span> </td> 
   <td colname="col3"> Dettagli su un file GIF animato. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> assetHandle</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Gestione risorse. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> assetSetInfo</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> Frase di codice  </span> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> cabinetInfo</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> tipi:CabinetInfo</span> </td> 
   <td colname="col3"> Proprietà per un tipo di risorsa archivio. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> creato</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:dateTime</span> </td> 
   <td colname="col3"> Data e ora del caricamento della risorsa. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> createUser</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Indirizzo e-mail dell’utente che ha creato la risorsa. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> cssInfo</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> tipi:CssInfo</span> </td> 
   <td colname="col3"> Dettagli su un file CSS. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> cuePointInfo</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> Frase di codice  </span> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> excelInfo</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> Frase di codice  </span> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> fileName</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3">Restituisce il nome del file virtuale. Il percorso completo del file virtuale è <span class="codeph"> folder</span>+<span class="codeph"> fileName</span>. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> flashInfo</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> Frase di codice  </span> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> cartella</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Cartella contenente una risorsa. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> folderHandle</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Gestisci la cartella principale della risorsa. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> fontInfo</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> tipo:fontInfo</span> </td> 
   <td colname="col3"> Proprietà per una risorsa di font. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> iccProfileInfo</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> tipi:IccProfileInfo</span> </td> 
   <td colname="col3"> Proprietà per una risorsa profilo ICC. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> illustratorInfo</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> Frase di codice  </span> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> imageInfo</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> tipi:ImageInfo</span> </td> 
   <td colname="col3"> Proprietà per una risorsa immagine. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> inDesignInfo</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> Frase di codice  </span> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> ipsImageUrl</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> URL relativo che rappresenta una visualizzazione in miniatura della risorsa. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> javascriptInfo</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> tipi:JavascriptInfo</span> </td> 
   <td colname="col3"> Dettagli su un file JavaScript. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> lastModified</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:dateTime</span> </td> 
   <td colname="col3"> Data e ora dell’ultima modifica della risorsa. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> lastModifyUser</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Indirizzo e-mail dell’utente che ha modificato la risorsa per l’ultima volta. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> layerViewInfo</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> tipi:LayerViewInfo</span> </td> 
   <td colname="col3"> Proprietà per una risorsa di visualizzazione livello. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> maskInfo</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> Frase di codice  </span> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> masterVideoInfo</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> Frase di codice  </span> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> metadataArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> tipi:MetadataArray</span> </td> 
   <td colname="col3"> Array di valori di metadati associati alla risorsa. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> name</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Nome risorsa. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> pdfInfo</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> Frase di codice  </span> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> pdfSettingsInfo</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> tipi:PdfSettingsInfo</span> </td> 
   <td colname="col3"> Proprietà di una risorsa delle impostazioni PDF. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> permissions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> Frase di codice  </span> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> postScriptInfo</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> Frase di codice  </span> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> PowerPointInfo</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> Frase di codice  </span> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> premiereExpressInfo</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> Frase di codice  </span> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> progetti</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Elenco dei nomi dei progetti. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> psdInfo</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> Frase di codice  </span> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> readyForPublish</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> Imposta un flag per indicare se una risorsa deve essere pubblicata o meno. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> renderSceneInfo</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> tipi:RenderSceneInfo</span> </td> 
   <td colname="col3"> Proprietà di una risorsa scena di rendering. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> rtfInfo</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> Frase di codice  </span> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> subType</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3">Sottotipo di risorsa generico che supporta i valori dei sottotipi (ad esempio, <span class="codeph"> AssetSet</span>). </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> svgInfo</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> tipi:SvgInfo</span> </td> 
   <td colname="col3"> Proprietà di una risorsa SVG. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> swcInfo</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> tipi:SwcInfo</span> </td> 
   <td colname="col3"> Proprietà di una risorsa SWC. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> templateInfo</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> tipi:TemplateInfo</span> </td> 
   <td colname="col3"> Proprietà di una risorsa modello. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> trashState</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Indica se una risorsa è nel cestino o live (consulta "Stato del cestino" per i valori). </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> type</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3">Tipo di risorsa. Per i valori, consulta <a href="../../string-constants/c-string-constants/r-asset-types.md#reference-2fe75d230663419d88632d30f1144a10" format="dita" scope="local"> Tipi di risorse</a> . </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> videoCaptionInfo</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> tipi:VideoCaptionInfo</span> </td> 
   <td colname="col3"> <p>Proprietà di una risorsa di sottotitoli video. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> videoInfo</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> Frase di codice  </span> </td> 
   <td colname="col3"> <p>Proprietà di una risorsa video. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> viewerPresetInfo</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> tipi:ViewerPresetInfo</span> </td> 
   <td colname="col3"> Proprietà di una risorsa predefinita visualizzatore. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> viewerSwfInfo</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> tipi:ViewerSwfInfo</span> </td> 
   <td colname="col3"> Proprietà di una risorsa SWf visualizzatore. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> vignetteInfo</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> tipi:VignetteInfo</span> </td> 
   <td colname="col3"> Proprietà di una risorsa vignetta. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> watermarkInfo</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> tipi:InformazioniFiligrana</span> </td> 
   <td colname="col3"> Proprietà di una risorsa filigrana. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> windowCoveringInfo</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> tipi:WindowCoveringInfo</span> </td> 
   <td colname="col3"> Proprietà di una finestra che copre la risorsa. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> wordInfo</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> Frase di codice  </span> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> xmlInfo</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> tipi:XmlInfo</span> </td> 
   <td colname="col3"> Proprietà di una risorsa XML. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> xslInfo</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> tipi:XslInfo</span> </td> 
   <td colname="col3"> Proprietà di una risorsa XSL. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> zipInfo</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> Frase di codice  </span> </td> 
   <td colname="col3"> </td> 
  </tr> 
 </tbody> 
</table>
