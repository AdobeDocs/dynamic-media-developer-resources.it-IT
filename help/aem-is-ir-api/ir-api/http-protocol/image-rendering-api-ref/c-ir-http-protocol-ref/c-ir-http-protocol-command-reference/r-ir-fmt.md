---
description: Formato immagine di risposta. Specifica il formato di codifica dell’immagine per i dati immagine inviati al client e il tipo MIME di risposta corrispondente per l’intestazione di risposta HTTP.
solution: Experience Manager
title: fmt
feature: Dynamic Media Classic, SDK/API
role: Developer,Business Practitioner
exl-id: 691c5421-0754-45ce-b454-dd0ceff47a58
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '582'
ht-degree: 3%

---

# fmt{#fmt}

Formato immagine di risposta. Specifica il formato di codifica dell’immagine per i dati immagine inviati al client e il tipo MIME di risposta corrispondente per l’intestazione di risposta HTTP.

` fmt= *``*[,[ *``*][, *`formatpixelTypetiffCompression`*]]`

<table id="simpletable_200779AA8D8D49A089A295AED5C98C8F"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> format  </span> </p> </td> 
  <td class="stentry"> <p>jpeg </p> </td> 
  <td class="stentry"> <p>JPEG. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> </p> </td> 
  <td class="stentry"> <p>jpg </p> </td> 
  <td class="stentry"> <p>JPG Perdita. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> </p> </td> 
  <td class="stentry"> <p>png </p> </td> 
  <td class="stentry"> <p>PNG senza perdita. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> </p> </td> 
  <td class="stentry"> <p>png-alpha </p> </td> 
  <td class="stentry"> <p>PNG senza perdita con canale alfa. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> </p> </td> 
  <td class="stentry"> <p>tif </p> </td> 
  <td class="stentry"> <p>TIFF. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> </p> </td> 
  <td class="stentry"> <p>tif-alfa </p> </td> 
  <td class="stentry"> <p>TIFF con canale alfa. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> </p> </td> 
  <td class="stentry"> <p>swf </p> </td> 
  <td class="stentry"> <p>File JPEG con perdita incorporato in un file swf Macromedia. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> </p> </td> 
  <td class="stentry"> <p>swf-alpha </p> </td> 
  <td class="stentry"> <p>File JPEG con perdita e maschera con compressione deflata incorporati in un file swf Macromedia. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> </p> </td> 
  <td class="stentry"> <p>pdf </p> </td> 
  <td class="stentry"> <p>Immagine incorporata in PDF. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> </p> </td> 
  <td class="stentry"> <p>eps </p> </td> 
  <td class="stentry"> <p>PostScript incapsulato binario non compresso. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> </p> </td> 
  <td class="stentry"> <p>gif </p> </td> 
  <td class="stentry"> <p>GIF con 256 colori. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> </p> </td> 
  <td class="stentry"> <p>gif-alpha </p> </td> 
  <td class="stentry"> <p>GIF con 255 colori più trasparenza a colori chiave. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> pixelType  </span> </p> </td> 
  <td class="stentry"> <p>rgb </p> </td> 
  <td class="stentry"> <p>Restituire i dati immagine RGB. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> </p> </td> 
  <td class="stentry"> <p>grigio </p> </td> 
  <td class="stentry"> <p>Restituisce i dati immagine in scala di grigi. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> </p> </td> 
  <td class="stentry"> <p>cmyk </p> </td> 
  <td class="stentry"> <p>Restituisci i dati immagine CMYK. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <span class="varname"> tiffCompression  </span> </td> 
  <td class="stentry"> <p>none </p> </td> 
  <td class="stentry"> <p>Non compresso. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> </p> </td> 
  <td class="stentry"> <p>lzw </p> </td> 
  <td class="stentry"> <p>Compressione LZW (Lempel-Ziv-Welch) (senza perdita). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> </p> </td> 
  <td class="stentry"> <p>zip </p> </td> 
  <td class="stentry"> <p>Compressione "Deflate" (senza perdita). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> </p> </td> 
  <td class="stentry"> <p>jpeg </p> </td> 
  <td class="stentry"> <p>Compressione JPEG (con perdita). </p> </td> 
 </tr> 
</table>

*`pixelType`* applica la conversione dello spazio colore in uscita quando non  `icc=` è specificato; viene  *`pixelType`* applicato il profilo colore predefinito corrispondente a . Se la gestione del colore è disabilitata, viene applicata una conversione ingenua. *`pixelType`* viene ignorato quando  `icc=` viene specificato, che determina il tipo di pixel di output.

*`compression`* è consentito solo se tif, tif-alpha o PDF è specificato come  *`format`*. Per le opzioni di compressione supportate per questi formati immagine, fare riferimento alla tabella seguente.

`qlt-` imposta le opzioni di codifica JPEG per i seguenti formati: JPEG, TIFF con compressione JPEG, PDF con compressione JPEG e file SWF. Utilizzare `quantize=` se `fmt=gif` o `fmt=gif-alpha`. Per ulteriori informazioni, fare riferimento alle descrizioni dei comandi. Gli altri formati non dispongono di opzioni impostabili.

Vengono restituiti otto bit per componente pixel per tutti i formati e i tipi di pixel.

Nella tabella seguente sono elencate le combinazioni valide di *`format`* e *`pixelType`*, i tipi MIME di risposta HTTP corrispondenti, se i profili ICC possono essere incorporati (vedi [iccEmbed=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-iccembed.md#reference-47a433138c7c4b29b9b29871b2491a7f)) e quali comandi di opzione specifici per il formato possono essere applicati.

<table id="table_3461A367632E4B5A8AB578850A439024"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> <span class="varname"> format  </span> </p> </th> 
   <th colname="col2" class="entry"> <p> <span class="varname"> pixelType  </span> </p> </th> 
   <th colname="col3" class="entry"> <p>Tipo MIME di risposta </p> </th> 
   <th colname="col4" class="entry"> <p>Incorpora profilo ICC </p> </th> 
   <th colname="col5" class="entry"> <p>Opzioni </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>jpeg, jpg </p> </td> 
   <td colname="col2"> <p>rgb, grigio, cmyk </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;image&gt; </span> </p> </td> 
   <td colname="col4"> <p>Sì </p> </td> 
   <td colname="col5"> <span class="codeph"> qlt=  </span> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>png, png-alpha </p> </td> 
   <td colname="col2"> <p>rgb, grigio </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;image&gt; </span> </p> </td> 
   <td colname="col4"> <p>Sì </p> </td> 
   <td colname="col5"> <p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>png8, png8-alpha </p> </td> 
   <td colname="col2"> <p>rgb </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;image&gt; </span> </p> </td> 
   <td colname="col4"> <p>sì </p> </td> 
   <td colname="col5"> <p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>tif, tif-alfa </p> </td> 
   <td colname="col2"> <p>rgb, grigio, cmyk </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;image&gt; </span> </p> </td> 
   <td colname="col4"> <p>Sì </p> </td> 
   <td colname="col5"> <p> <span class="varname"> tiffCompression  </span> </p> <p> <span class="codeph"> (none|lzw|zip|jpeg), pathEmbed=, qlt  </span> </p> <p>( <span class="codeph"> qlt= </span> viene ignorato a meno che <span class="varname"> tiffCompression </span> non sia impostato su 'jpeg'). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>swf, alfa-swf </p> </td> 
   <td colname="col2"> <p>rgb, grigio </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;application&gt; </span> </p> </td> 
   <td colname="col4"> <p>No </p> <p>(Il Flash Player ignora i profili ICC incorporati.) </p> </td> 
   <td colname="col5"> <p> <span class="codeph"> qlt=  </span>,  <span class="codeph"> attributo::TrustedDomains  </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>pdf </p> </td> 
   <td colname="col2"> <p>rgb, grigio, cmyk </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;application&gt; </span> </p> </td> 
   <td colname="col4"> <p>Sì </p> </td> 
   <td colname="col5"> <p> <span class="varname"> tiffCompression  </span> </p> <p> <span class="codeph"> (none|zip|jpeg),qlt=  </span> </p> <p> ( <span class="codeph"> qlt= </span> viene ignorato a meno che <span class="varname"> tiffCompression </span> non sia impostato su 'jpeg'). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>eps </p> </td> 
   <td colname="col2"> <p>rgb, grigio, cmyk </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;image&gt; </span> </p> </td> 
   <td colname="col4"> <p>Sì </p> </td> 
   <td colname="col5"> <p> <span class="codeph"> pathEmbed=  </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>gif, gif-alpha </p> </td> 
   <td colname="col2"> <p>rgb, grigio </p> <p>I dati vengono convertiti in palette dopo la conversione in grigio o rgb. </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;image&gt; </span> </p> </td> 
   <td colname="col4"> <p>No </p> </td> 
   <td colname="col5"> <p> </p> </td> 
  </tr> 
 </tbody> 
</table>

Specifica il formato di codifica per i dati dell’immagine di risposta inviati al client e il tipo MIME di risposta corrispondente per l’intestazione di risposta HTTP.

`png-alpha` restituisce alfa non associato (ovvero, alfa non premoltiplica i valori dei pixel), mentre  `tif-alpha`, e  `swf-alpha` restituisce alfa associato (ovvero, i valori alfa sono pre-moltiplicati con i valori alfa). Il canale alfa corrisponde all&#39;inverso della maschera di sfondo della vignetta per `req=img` e al gruppo o alla maschera oggetto se è presente `req=object`. Per applicare alfa quando si utilizza una richiesta IR nidificata, aggiungi `fmt=` con il formato di file alfa appropriato alla richiesta IR incorporata e alla richiesta principale. Se con `icc=` è specificato un profilo ICC CMYK o in scala di grigi, non viene restituito alcun dato alfa.

## Proprietà {#section-eb12a82c69d84622bcea153dd84d95b3}

Può verificarsi in qualsiasi punto della richiesta.

## Predefinito {#section-d2c2af11fa974e1a84e0c6cb7fb646fe}

*`format`* viene impostata su  `attribute::Format`e  *`tiffCompression`* viene impostata su  `attribute::TiffEncoding`. *`pixelType`* viene impostato automaticamente su  `rgb` se non  `icc=` è specificato, altrimenti corrisponde al tipo di pixel del profilo ICC specificato.

## Consultate anche {#section-c55efc881fc94c70bff91b870e026a7b}

[attributo::Format](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-format.md#reference-da5207242f1c4f1c8fa4df6027121ff2) ,  [attributo::JpegQuality](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-jpegquality.md#reference-d86fc5ad18bb436891efdbe1f98fea50),  [attributo::TiffEncoding](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-tiffencoding.md#reference-a3425191166042d59db766c468857d0e),  [qlt=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-qlt.md#reference-27b91c226eb241d0a14a29af3b3afdbd),  [iccEmbed=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-iccembed.md#reference-47a433138c7c4b29b9b29871b2491a7f),  [pathEmbed=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-pathembed.md#reference-dfff01079fc74dbd896362cc740d7f5f),  [req=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-req.md#reference-792b1a663fb64261bd2de2a209b847fb),  [quantize=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-quantize.md#reference-b8069670fa474e4799ac29f0d693ca38)
