---
description: Formato immagine di risposta.
seo-description: Formato immagine di risposta.
seo-title: fmt
solution: Experience Manager
title: fmt
uuid: 29151740-3bbc-4c5e-bbc7-4afe9064ff5f
feature: Dynamic Media Classic, SDK/API
role: Sviluppatore, Business Practices
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '864'
ht-degree: 3%

---


# fmt{#fmt}

Formato immagine di risposta.

`fmt=format[,` `[`*`pixelType`*`]`,`[`*`compression`*`]]`

*`format`* — jpeg | jpg | pjpeg | png | png8 | png-alpha | png8-alpha | tif | tif-alfa | swf | swf-alpha | swf3 | swf3-alpha | eps | gif | gif-alpha | m3u8 | f4m | web | webp-alpha | jpeg2000 | jpeg2000-alpha | jpegxr | jpegxr-alpha

| *`format`* | Descrizione |
|---|---| 
| `jpeg` | JPEG in perdita |
| `jpg` | JPG in perdita |
| `pjpeg` | JPEG progressivo |
| `png` | PNG senza perdita a 24 bit |
| `png8` | PNG senza perdita a 8 bit |
| `png-alpha` | PNG senza perdita a 24 bit con canale alfa |
| `png8-alpha` | PNG senza perdita a 8 bit con canale alfa |
| `tif` | TIFF |
| `tif-alpha` | TIFF con canale alfa |
| `pdf` | Immagine incorporata in PDF |
| `eps` | PostScript incapsulato binario non compresso |
| `gif` | GIF con 2-256 colori |
| `gif-alpha` | GIF a 2-256 colori più trasparenza basata su colore chiave |
| `swf` | File JPEG con perdita incorporato in un file swf AS2 di Adobe |
| `swf-alpha` | JPEG in perdita e una maschera con deflazione compressa incorporata in un file swf AS2 in Adobe |
| `swf3` | File JPEG con perdita incorporato in un file swf AS3 di Adobe |
| `swf3-alpha` | JPEG con perdita e una maschera compressa in deflazione incorporata in un file swf AS3 di Adobe. **Nota**: i formati swf e swf-alpha sono più utilizzati per le applicazioni ActionScript 2 (Flash Player 8 e versioni precedenti). Si consiglia l&#39;utilizzo di swf3 e swf3-alpha per le applicazioni ActionScript3 (Flash Player 9 e versioni successive) |
| `m3u8` | Formato manifesto server di streaming Apple |
| `f4m` | Formato manifesto del server di streaming Flash |
| `webp` | WebP in perdita e senza perdita |
| `webp-alpha` | WebP perdente e senza perdita con canale alfa |
| `jpeg2000` | JPEG 2000 senza perdite e perdite |
| `jpeg2000-alpha` | JPEG 2000 senza perdite e perdite con canale alfa |
| `jpegxr` | JPEG XR con perdita di dati e perdite |
| `jpegxr-alpha` | JPEG XR Perdita e senza perdita con canale alfa |


| *`pixelType`* — rgb | grigio | cmyk |
| *`pixelType`* | Descrizione |
|---|---|
| `rgb` | Restituire i dati immagine RGB. |
| `gray` | Restituisce i dati immagine in scala di grigi. |
| `cmyk` | Restituisci i dati immagine CMYK. |

| *`compression`* — none | lzw | zip | jpeg | scemo | senza perdite |
| *`compression`* | Descrizione |
|---|---|
| `none` | Non compresso |
| `lzw` | Compressione LZW (Lempel-Ziv-Welch) (senza perdita) |
| `zip` | Compressione &quot;Deflate&quot; (senza perdita) |
| `jpeg` | Compressione JPEG (con perdita) |
| `lossy` | Compressione WebP, JPEG 2000 e JPEG XR (con perdita) |
| `lossless` | Compressione WebP, JPEG 2000 e JPEG XR (senza perdita) |

* *`format`* specifica il formato di codifica dell’immagine per i dati immagine inviati al client e il tipo MIME di risposta corrispondente per l’intestazione di risposta HTTP.
* *`pixelType`* può essere utilizzato per effettuare la conversione dello spazio colore in uscita quando non  `icc=` è specificato.

   Viene applicato il profilo colore predefinito corrispondente a *`pixelType`*. Se la gestione del colore è disabilitata, viene applicata una conversione ingenua. *`pixelType`* viene ignorato quando  `icc=` viene specificato, che determina il tipo di pixel di output.

* *`compression`* è consentito solo se  `tif`,  `tif-alpha`,  `pdf`,  `webp`,  `webp-alpha`,  `jpeg2000`,  `jpeg2000-alpha`,  `jpegxr` o  `jpegxr-alpha` è specificato come  *`format`*. Per le opzioni di compressione supportate per questi formati immagine, fare riferimento alla tabella seguente.

È possibile utilizzare `qlt=` per impostare le opzioni di codifica JPEG per questi formati: JPEG, TIFF con compressione JPEG, PDF con compressione JPEG e SWF. WebP, JPEG 2000 e JPEG XR utilizzano anche `qlt=` ma i valori producono qualità diverse per i diversi formati. Utilizzare `quantize=` se `fmt=gif` o `fmt=gif-alpha`. Per ulteriori informazioni, fare riferimento alle descrizioni dei comandi. Gli altri formati non dispongono di opzioni impostabili.

Vengono restituiti 8 bit per componente pixel per tutti i formati *`formats`* e *`pixelTypes`* (8 bit per pixel per GIF).

Nella tabella seguente sono elencate le combinazioni valide di *`format`*e *`pixelType`*, i tipi MIME di risposta HTTP corrispondenti, se i profili ICC possono essere incorporati (vedi [iccEmbed=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-iccembed.md#reference-e3b774fb322046a2a6dde3a7bab5583e)) e quali opzioni specifiche per il formato puoi applicare.

<table id="table_12F897A34D1D47F3AA492D4F074F09D5"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> <i> format</i> </b> </th> 
   <th class="entry"> <b> <i> pixelType</i> </b> </th> 
   <th class="entry"> <b> Tipo MIME di risposta</b> </th> 
   <th class="entry"> <b>Incorpora profilo ICC</b> </th> 
   <th class="entry"> <b> Opzioni</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr valign="top"> 
   <td colname="col1"> <p> jpeg, jpg, pjpeg </p> </td> 
   <td colname="col2"> <p>rgb, grigio, cmyk </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;image&gt; </span> </p> </td> 
   <td colname="col4"> <p>Sì </p> </td> 
   <td colname="col5"> <p> <span class="codeph"> pathEmbed=  </span>,  <span class="codeph"> pscan=  </span>,  <span class="codeph"> qlt=  </span>,  <span class="codeph"> xmpEmbed=  </span> </p> <p>Il parametro <span class="codeph"> pscan= </span> si applica solo al formato pjpeg. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> png, png-alpha </p> </td> 
   <td colname="col2"> <p>rgb, grigio </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;image&gt; </span> </p> </td> 
   <td colname="col4"> <p>Sì </p> </td> 
   <td colname="col5"> <p> </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p>png8, png8-alpha </p> </td> 
   <td colname="col2"> <p>rgb </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;image&gt; </span> </p> </td> 
   <td colname="col4"> <p>Sì </p> </td> 
   <td colname="col5"> <p> </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> tif, tif-alfa </p> </td> 
   <td colname="col2"> <p>rgb, grigio, cmyk </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;image&gt; </span> </p> </td> 
   <td colname="col4"> <p>Sì </p> </td> 
   <td colname="col5"> <span class="codeph"> <span class="varname"> compressione  </span> </span> <p> ( <span class="codeph"> none|lzw|zip|jpeg </span>) </p> <p>solo "tiff"; 'tiff-alpha' non supporta la compressione jpeg. </p> <p> <span class="codeph"> qlt=  </span> </p> <p> <span class="codeph"> qlt=  </span> viene ignorato a meno che  <span class="varname"> la compressione non  </span> sia impostata su  <span class="codeph"> jpeg  </span>. </p> <p>, pathEmbed=, xmpEmbed= </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> swf,swf3, swf-alpha, swf-alpha3 </p> </td> 
   <td colname="col2"> <p>rgb, grigio </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;application&gt; </span> </p> </td> 
   <td colname="col4"> <p>No </p> <p> <p>Nota:  Il Flash Player di Adobe ignora i profili ICC incorporati. </p> </p> </td> 
   <td colname="col5"> <p> <span class="codeph"> qlt=  </span>,  <span class="codeph"> attributo::TrustedDomains  </span> </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> pdf </p> </td> 
   <td colname="col2"> <p>rgb, grigio, cmyk </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;application&gt; </span> </p> </td> 
   <td colname="col4"> <p>Sì </p> </td> 
   <td colname="col5"> <span class="codeph"> <span class="varname"> compressione  </span> </span> <p> ( <span class="codeph"> none|zip|jpeg </span>), <span class="codeph"> qlt= </span> </p> <p> <span class="codeph"> qlt=  </span> viene ignorato a meno che  <span class="codeph"> <span class="varname"> la compressione non  </span> </span> sia impostata su  <span class="codeph"> jpeg  </span>. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> eps </p> </td> 
   <td colname="col2"> <p>rgb, grigio, cmyk </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;image&gt; </span> </p> </td> 
   <td colname="col4"> <p>Sì </p> </td> 
   <td colname="col5"> <p> <span class="codeph"> pathEmbed=  </span> </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> gif, gif-alpha </p> </td> 
   <td colname="col2"> <p>rgb, grigio </p> <p>I dati vengono convertiti in palette dopo la conversione in grigio o rgb. </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;image&gt; </span> </p> </td> 
   <td colname="col4"> <p>No </p> </td> 
   <td colname="col5"> <p> <span class="codeph"> quantize=  </span> </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p>web, webp-alpha </p> </td> 
   <td> <p>rgb </p> </td> 
   <td> <p> <span class="codeph"> &lt;image&gt; </span> </p> </td> 
   <td> <p>No </p> </td> 
   <td> <p> <span class="codeph"> <span class="varname"> compressione  </span> </span> (  <span class="codeph"> perdita  </span>,  <span class="codeph"> senza perdita  </span>) </p> <p> <span class="codeph"> qlt=  </span> viene ignorato per  <span class="codeph"> lossless  </span>. </p> <p>Poiché non esiste alcun concetto di sottocampionamento della crominanza con il formato WebP, se si utilizza un secondo valore con <span class="codeph"> qlt </span> (ad esempio, <span class="codeph"> qlt=80,1 </span>) il secondo valore ( <span class="codeph"> 1 </span>) viene ignorato. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p>jpeg2000, jpeg2000-alpha </p> </td> 
   <td> <p>rgb, grigio </p> </td> 
   <td> <p> <span class="codeph"> &lt;image&gt; </span> </p> </td> 
   <td> <p>No </p> </td> 
   <td> <p>Come sopra. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p>jpegxr, jpegxr-alpha </p> </td> 
   <td> <p>rgb </p> </td> 
   <td> <p> <span class="codeph"> &lt;image&gt; </span> </p> </td> 
   <td> <p>No </p> </td> 
   <td> <p>Come sopra. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Proprietà {#section-5f96b0ce7c5a4df1bf52e24ea78c3dae}

Attributo di richiesta. Si applica indipendentemente dall&#39;impostazione del livello corrente se `req=img` (predefinito) o `req=mask`; altrimenti ignorato.

*`type`* viene ignorato se  `iccProfile=` è specificato.

## Predefinito {#section-f885a785b32c44fea347db15fdb2ab1f}

` fmt=jpeg, *`defaultType`*,none`, in cui  *`defaultType`* viene gestito come segue: Se  `icc=` viene specificato,  *`defaultType`* corrisponde al tipo di pixel del profilo ICC specificato. Se `icc=` non è specificato, *`defaultType`* è `gray` se `req=mask`, altrimenti è `rgb`.

## Esempi {#section-b93222e652df404a84c69025247f07df}

**Richiedi un&#39;anteprima piccola e di bassa qualità in formato JPEG (predefinito):**

` http:// *`server`*/myRootId/myImageId?qlt=60&wid=200`

**Richiedi la stessa immagine convertita in scala di grigio:**

` http:// *`server`*/myRootId/myImageId?fmt=jpeg,gray&qlt=60&wid=200`

**Richiedi la stessa immagine in un formato senza perdita con canale alfa e ad alta risoluzione:**

` http:// *`server`*/myRootId/myImageId?fmt=png-alpha&wid=300`

**Richiedi il canale alfa per la stessa immagine di un&#39;immagine TIFF in scala di grigi:**

` http:// *`server`*/myRootId/myImageId?req=mask&fmt=tif,gray&wid=300`

**Converti la stessa immagine in cmyk utilizzando i profili ICC predefiniti:**

` http:// *`server`*/myRootId/myImageId?fmt=tif,cmyk&wid=300`

**Converti la stessa immagine in cmyk utilizzando un profilo ICC diverso e incorpora il profilo nell’immagine TIFF:**

` http:// *`server`*/myRootId/myImageId?fmt=tif&wid=300&icc=myPrinterProfile&iccEmbed=1`

**Fornire questa immagine come file TIF con compressione JPEG senza conversione del tipo di pixel:**

` http:// *`server`*/myRootId/myImageId?fmt=tif,,jpeg&qlt=95&wid=300`

**Converti l&#39;immagine in GIF bictonale con trasparenza a colori chiave e forza i colori in bianco e nero:**

` http:// *`server`*/myRootId/myImageId?fmt=gif-alpha&wid=100&quantize=adaptive,off,2,000000,ffffff`

**Perdita con impostazione di qualità di 80:**

` http:// *`server`*/myRootId/myImageId?wid=300&fmt=webp&qlt=80`

**Senza perdita con alfa:**

` http:// *`server`*/myRootId/myImageId?wid=300&fmt=webp-alpha,,lossless`

**Perdita con impostazione di qualità di 80:**

`http://server/myRootId/myImageId?wid=300&fmt=jpeg2000&qlt=80`

**Senza perdita con alfa:**

`http://server/myRootId/myImageId?wid=300&fmt=jpeg2000-alpha,,lossless`

**Perdita con impostazione di qualità di 80:**

`http://server/myRootId/myImageId?wid=300&fmt=jpegxr&qlt=80`

**Senza perdita con alfa:**

`http://server/myRootId/myImageId?wid=300&fmt=jpegxr-alpha,,lossless`

## Consultate anche {#section-fce8d69c74234bf48cf814d799409541}

[qlt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-qlt.md#reference-f69ed0758c784b0385d979820546d352) ,  [quantize=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-quantize.md#reference-b8069670fa474e4799ac29f0d693ca38),  [req=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76),  [icc=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-icc.md#reference-182b5679e21e4df3b4d330535a5a7517),  [iccEmbed=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-iccembed.md#reference-e3b774fb322046a2a6dde3a7bab5583e),  [pathEmbed=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-pathembed.md#reference-9ccf0771d6634cf68c1c9c33cd428301),  [pscan](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-pscan.md#reference-b8101ed8e6c04dd28173f9597e52b135).
