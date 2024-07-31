---
title: fmt
description: Formato immagine di risposta.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 67f8a58d-88f5-4993-9749-41a3c530adba
source-git-commit: 67e12fae514341137e4218ea950f34da0d9997f3
workflow-type: tm+mt
source-wordcount: '1017'
ht-degree: 1%

---

# fmt{#fmt}

Formato immagine di risposta.

`fmt=format[,` `[`*`pixelType`*`]`,`[`*`compression`*`]]`

*`format`* - avif-alpha | avif | eps | f4m | gif-alfa | gif | heic | jpeg | jpeg2000-alfa | jpeg2000 | jpegxr-alpha | jpegxr | jpg | m3u8 | pdf | pjpeg | png-alfa | png | png8-alfa | png8 | swf-alfa | swf | swf3-alfa | swf3 | tif-alfa | tif | alfa-web | webp

| *`format`* | Descrizione |
|---|---|
| `avif-alpha` | AVIF con perdita di dati e senza perdita di dati con canale alfa. |
| `avif` | Perdita e senza perdita di avf. |
| `eps` | PostScript incapsulato binario non compresso. |
| `f4m` | Formato del manifesto del server di streaming di Flash. |
| `gif-alpha` | GIF con 2-255 colori più trasparenza chiave-colore. |
| `gif` | GIF con 2-256 colori. |
| `heic` | EIC senza perdita di dati. Se non è supportato, questo formato viene scaricato per impostazione predefinita dal browser. |
| `jpeg` | Lossy JPEG. |
| `jpeg2000-alpha` | Lossy e lossless JPEG 2000 con canale alfa. |
| `jpeg2000` | Lossy e lossless JPEG 2000. |
| `jpegxr-alpha` | Lossy e lossless JPEG XR con canale alfa. |
| `jpegxr` | Lossy e lossless JPEG XR. |
| `jpg` | Perdita JPG-. |
| `m3u8` | Formato del manifesto di Apple Streaming Server. |
| `pdf` | Immagine incorporata in PDF. |
| `pjpeg` | JPEG progressivo. |
| `png-alpha` | PNG senza perdite a 24 bit con canale alfa. |
| `png` | PNG senza perdite a 24 bit. |
| `png8-alpha` | PNG senza perdita di 8 bit con canale alfa. |
| `png8` | PNG senza perdita di 8 bit. |
| `swf-alpha` | Lossy JPEG e una maschera compressa deflata incorporata in un file SWF AS2 di Adobe. |
| `swf` | Lossy JPEG incorporato in un file SWF AS2 Adobe. |
| `swf3-alpha` | Lossy JPEG e una maschera compressa deflata incorporata in un file SWF AS3 di Adobe. **Nota:** i formati swf e swf-alpha sono più adatti per le applicazioni ActionScript 2 (Flash Player 8 e versioni precedenti). I formati swf3 e swf3-alpha sono consigliati per l&#39;uso nelle applicazioni ActionScript 3 (Flash Player 9 e versioni successive). |
| `swf3` | Lossy JPEG incorporato in un file SWF AS3 di Adobe. |
| `tif-alpha` | TIFF con canale alfa. |
| `tif` | TIFF. |
| `webp-alpha` | WebP senza perdita di dati con canale alfa. |
| `webp` | WebP senza perdita di dati. |

*`pixelType`* - rgb | grigio | cmyk

| *`pixelType`* | Descrizione |
|---|---|
| `cmyk` | Restituisci dati immagine CMYK. |
| `gray` | Restituisci dati immagine in scala di grigio. |
| `rgb` | Restituisci dati immagine RGB. |

*`compression`* - jpeg | lossy | senza perdita | lzw | nessuno | zip

| *`compression`* | Descrizione |
|---|---|
| `jpeg` | Compressione JPEG (con perdita di dati). |
| `lossy` | JPEG 2000, compressione JPEG XR (con perdita di dati) e WebP. |
| `lossless` | HEIC, JPEG 2000 e compressione JPEG XR (senza perdita di dati) e WebP. |
| `lzw` | Compressione LZW (Lempel-Ziv-Welch) (senza perdita di dati). |
| `none` | Non compresso. |
| `zip` | Compressione Deflate (senza perdita di dati). |

* *`format`* specifica il formato di codifica immagine per i dati immagine inviati al client e il tipo MIME di risposta corrispondente per l&#39;intestazione di risposta HTTP.
* È possibile utilizzare *`pixelType`* per eseguire la conversione dello spazio colore di output quando `icc=` non è specificato.

  Viene applicato il profilo colore predefinito corrispondente a *`pixelType`*. Se la gestione del colore è disattivata, viene applicata la conversione naïve. *`pixelType`* viene ignorato quando si specifica `icc=`, che determina il tipo di pixel di output.

* *`compression`* è consentito solo se `tif`, `tif-alpha`, `pdf`, `webp`, `webp-alpha`, `jpeg2000`, `jpeg2000-alpha`, `jpegxr` o `jpegxr-alpha` è specificato come *`format`*. Per informazioni sulle opzioni di compressione supportate per questi formati di immagine, consulta la tabella seguente.

È possibile utilizzare `qlt=` per impostare le opzioni di codifica JPEG per i seguenti formati: JPEG, TIFF con compressione JPEG, PDF con compressione JPEG e SWF. Anche WebP, JPEG 2000 e JPEG XR utilizzano `qlt=`, ma i valori determinano qualità diverse per i diversi formati. Usa `quantize=` se `fmt=gif` o `fmt=gif-alpha`. Per ulteriori informazioni, consultare le descrizioni dei comandi. Gli altri formati non dispongono di opzioni impostabili.

Vengono restituiti 8 bit per componente pixel per tutti *`formats`* e *`pixelTypes`* (8 bit per pixel per GIF).

Nella tabella seguente sono elencate le combinazioni valide di *`format`*e *`pixelType`*, i tipi MIME di risposta HTTP corrispondenti, se i profili ICC possono essere incorporati (vedere [iccEmbed=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-iccembed.md#reference-e3b774fb322046a2a6dde3a7bab5583e)) e quali opzioni specifiche del formato è possibile applicare.

<table id="table_12F897A34D1D47F3AA492D4F074F09D5"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> <i> formato</i> </b> </th> 
   <th class="entry"> <b> <i> pixelType</i> </b> </th> 
   <th class="entry"> <b> tipo MIME risposta</b> </th> 
   <th class="entry"> <b>Incorpora profilo ICC</b> </th> 
   <th class="entry"> Opzioni <b></b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr valign="top"> 
   <td> <p> avif, avif-alfa </p> </td> 
   <td> <p>rgb</p> </td> 
   <td> <p> <span class="codeph"> &lt;image/avif&gt; </span> </p> </td> 
   <td> <p>No </p> </td> 
   <td> <p> Compressione <span class="codeph"> <span class="varname"> </span> </span> ( <span class="codeph"> con perdita </span>, <span class="codeph"> senza perdita </span>) </p> <p> <span class="codeph"> qlt= </span> ignorato per <span class="codeph"> senza perdita di dati </span>. </p> <p>Poiché non esiste alcun concetto di downsampling della crominanza con il formato WebP, se si utilizza un secondo valore con <span class="codeph"> qlt </span> (ad esempio, <span class="codeph"> qlt=80,1 </span>) il secondo valore ( <span class="codeph"> 1 </span>) viene ignorato. </p> </td> 
  </tr>
  <tr valign="top"> 
   <td colname="col1"> <p> eps </p> </td> 
   <td colname="col2"> <p>rgb, grigio, cmyk </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;image/eps&gt; </span> </p> </td> 
   <td colname="col4"> <p>Sì </p> </td> 
   <td colname="col5"> <p> <span class="codeph"> pathEmbed= </span> </p> </td> 
  </tr>
  <tr valign="top"> 
   <td colname="col1"> <p> gif, gif-alfa </p> </td> 
   <td colname="col2"> <p>rgb, grigio </p> <p>I dati vengono convertiti in palette dopo la conversione in grigio o rgb. </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;image/gif&gt; </span> </p> </td> 
   <td colname="col4"> <p>No </p> </td> 
   <td colname="col5"> <p> Quantize <span class="codeph">= </span> </p> </td> 
  </tr>
  <tr valign="top"> 
   <td colname="col1"> <p> heic </p> </td> 
   <td colname="col2"> <p>rgb </p> <p> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;image/heic&gt; </span> </p> </td> 
   <td colname="col4"> <p>No </p> </td> 
   <td colname="col5"> <p> </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p>jpeg2000, jpeg2000-alpha </p> </td> 
   <td> <p>rgb, grigio </p> </td> 
   <td> <p> <span class="codeph"> &lt;image/jp2&gt; </span> </p> </td> 
   <td> <p>No </p> </td> 
   <td> <p> Compressione <span class="codeph"> <span class="varname"> </span> </span> ( <span class="codeph"> con perdita </span>, <span class="codeph"> senza perdita </span>) </p> <p> <span class="codeph"> qlt= </span> ignorato per <span class="codeph"> senza perdita di dati </span>. </p> <p>Poiché non esiste alcun concetto di downsampling della crominanza con il formato WebP, se si utilizza un secondo valore con <span class="codeph"> qlt </span> (ad esempio, <span class="codeph"> qlt=80,1 </span>) il secondo valore ( <span class="codeph"> 1 </span>) viene ignorato. </p> </td> 
  </tr>
  <tr valign="top"> 
   <td colname="col1"> <p> jpeg, jpg, pjpeg </p> </td> 
   <td colname="col2"> <p>rgb, grigio, cmyk </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;image/jpeg&gt; </span> </p> </td> 
   <td colname="col4"> <p>Sì </p> </td> 
   <td colname="col5"> <p> <span class="codeph"> pathEmbed= </span>, <span class="codeph"> pscan= </span>, <span class="codeph"> qlt= </span>, <span class="codeph"> xmpEmbed= </span> </p> <p>Il parametro <span class="codeph"> pscan= </span> si applica solo al formato pjpeg. </p> </td> 
  </tr>
  <tr valign="top"> 
   <td> <p>jpegxr, jpegxr-alpha </p> </td> 
   <td> <p>rgb </p> </td> 
   <td> <p> <span class="codeph"> &lt;image/vnd.ms-photo&gt; </span> </p> </td> 
   <td> <p>No </p> </td> 
   <td> <p> Compressione <span class="codeph"> <span class="varname"> </span> </span> ( <span class="codeph"> con perdita </span>, <span class="codeph"> senza perdita </span>) </p> <p> <span class="codeph"> qlt= </span> ignorato per <span class="codeph"> senza perdita di dati </span>. </p> <p>Poiché non esiste alcun concetto di downsampling della crominanza con il formato WebP, se si utilizza un secondo valore con <span class="codeph"> qlt </span> (ad esempio, <span class="codeph"> qlt=80,1 </span>) il secondo valore ( <span class="codeph"> 1 </span>) viene ignorato. </p> </td> 
  </tr>
  <tr valign="top"> 
   <td colname="col1"> <p> pdf </p> </td> 
   <td colname="col2"> <p>rgb, grigio, cmyk </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;applicazione/pdf&gt; </span> </p> </td> 
   <td colname="col4"> <p>Sì </p> </td> 
   <td colname="col5"> Compressione <span class="codeph"> <span class="varname"> </span> </span> <p> ( <span class="codeph"> none|zip|jpeg </span>), <span class="codeph"> qlt= </span> </p> <p> <span class="codeph"> qlt= </span> viene ignorato a meno che la compressione <span class="codeph"> <span class="varname"> </span> </span> non sia impostata su <span class="codeph"> jpeg </span>. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p>png8, png8-alfa </p> </td> 
   <td colname="col2"> <p>rgb </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;image/png&gt; </span> </p> </td> 
   <td colname="col4"> <p>Sì </p> </td> 
   <td colname="col5"> <p> </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> png, png-alfa </p> </td> 
   <td colname="col2"> <p>rgb, grigio </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;image/png&gt; </span> </p> </td> 
   <td colname="col4"> <p>Sì </p> </td> 
   <td colname="col5"> <p> </p> </td> 
  </tr>
  <tr valign="top"> 
   <td colname="col1"> <p> swf,swf3, swf-alfa, swf-alfa3 </p> </td> 
   <td colname="col2"> <p>rgb, grigio </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;application/x-shockwave-flash&gt; </span> </p> </td> 
   <td colname="col4"> <p>No </p> <p> <p>Nota: il Flash Player di Adobi ignora i profili ICC incorporati. </p> </p> </td> 
   <td colname="col5"> <p> <span class="codeph"> qlt= </span>, attributo <span class="codeph">::DominiAttendibili </span> </p> </td> 
  </tr>
  <tr valign="top"> 
   <td colname="col1"> <p> tif, tif-alfa </p> </td> 
   <td colname="col2"> <p>rgb, grigio, cmyk </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;image/tiff&gt; </span> </p> </td> 
   <td colname="col4"> <p>Sì </p> </td> 
   <td colname="col5"> Compressione <span class="codeph"> <span class="varname"> </span> </span> <p> ( <span class="codeph"> none|lzw|zip|jpeg </span>) </p> <p>solo 'tiff'; 'tiff-alpha' non supporta la compressione jpeg. </p> <p> <span class="codeph"> qlt= </span> </p> <p> <span class="codeph"> qlt= </span> viene ignorato a meno che la compressione </span> di <span class="varname"> non sia impostata su <span class="codeph"> jpeg </span>. </p> <p>, pathEmbed=, xmpEmbed= </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p>webp, webp-alfa </p> </td> 
   <td> <p>rgb </p> </td> 
   <td> <p> <span class="codeph"> &lt;image/webp&gt; </span> </p> </td> 
   <td> <p>No </p> </td> 
   <td> <p> Compressione <span class="codeph"> <span class="varname"> </span> </span> ( <span class="codeph"> con perdita </span>, <span class="codeph"> senza perdita </span>) </p> <p> <span class="codeph"> qlt= </span> ignorato per <span class="codeph"> senza perdita di dati </span>. </p> <p>Poiché non esiste alcun concetto di downsampling della crominanza con il formato WebP, se si utilizza un secondo valore con <span class="codeph"> qlt </span> (ad esempio, <span class="codeph"> qlt=80,1 </span>) il secondo valore ( <span class="codeph"> 1 </span>) viene ignorato. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Proprietà {#section-5f96b0ce7c5a4df1bf52e24ea78c3dae}

Attributo della richiesta. Si applica indipendentemente dall&#39;impostazione del livello corrente se `req=img` (impostazione predefinita) o `req=mask`; altrimenti ignorato.

*`type`* viene ignorato se `iccProfile=` è specificato.

## Predefinito {#section-f885a785b32c44fea347db15fdb2ab1f}

` fmt=jpeg, *`defaultType`*,none`, in cui *`defaultType`* viene gestito come segue: se è specificato `icc=`, *`defaultType`* corrisponde al tipo di pixel del profilo ICC specificato. Se `icc=` non è specificato, *`defaultType`* è `gray` se `req=mask`, altrimenti è `rgb`.

## Esempi {#section-b93222e652df404a84c69025247f07df}

**Richiedi un&#39;immagine di anteprima piccola e di bassa qualità in formato JPEG (predefinito):**

` http:// *`server`*/myRootId/myImageId?qlt=60&wid=200`

**Richiedi la stessa immagine convertita in scala di grigio:**

` http:// *`server`*/myRootId/myImageId?fmt=jpeg,gray&qlt=60&wid=200`

**Richiedi la stessa immagine in un formato senza perdita di dati con canale alfa e ad alta risoluzione:**

` http:// *`server`*/myRootId/myImageId?fmt=png-alpha&wid=300`

**Richiedi il canale alfa per la stessa immagine di un&#39;immagine TIFF in scala di grigio:**

` http:// *`server`*/myRootId/myImageId?req=mask&fmt=tif,gray&wid=300`

**Convertire la stessa immagine in CMYK utilizzando i profili ICC predefiniti:**

` http:// *`server`*/myRootId/myImageId?fmt=tif,cmyk&wid=300`

**Converti la stessa immagine in CMYK utilizzando un profilo ICC diverso e incorpora il profilo nell&#39;immagine TIFF:**

` http:// *`server`*/myRootId/myImageId?fmt=tif&wid=300&icc=myPrinterProfile&iccEmbed=1`

**Distribuisci questa immagine come file TIF con compressione JPEG senza conversione del tipo di pixel:**

` http:// *`server`*/myRootId/myImageId?fmt=tif,,jpeg&qlt=95&wid=300`

**Converti l&#39;immagine in un GIF bicontonale con trasparenza dei colori chiave e forza i colori in bianco e nero:**

` http:// *`server`*/myRootId/myImageId?fmt=gif-alpha&wid=100&quantize=adaptive,off,2,000000,ffffff`

**Perdita con un&#39;impostazione di qualità di 80:**

` http:// *`server`*/myRootId/myImageId?wid=300&fmt=webp&qlt=80`

**Senza perdita con alfa:**

` http:// *`server`*/myRootId/myImageId?wid=300&fmt=webp-alpha,,lossless`

**Perdita con un&#39;impostazione di qualità di 80:**

`http://server/myRootId/myImageId?wid=300&fmt=jpeg2000&qlt=80`

**Senza perdita con alfa:**

`http://server/myRootId/myImageId?wid=300&fmt=jpeg2000-alpha,,lossless`

**Perdita con un&#39;impostazione di qualità di 80:**

`http://server/myRootId/myImageId?wid=300&fmt=jpegxr&qlt=80`

**Senza perdita con alfa:**

`http://server/myRootId/myImageId?wid=300&fmt=jpegxr-alpha,,lossless`

## Consultate anche {#section-fce8d69c74234bf48cf814d799409541}

[qlt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-qlt.md#reference-f69ed0758c784b0385d979820546d352) , [quantize=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-quantize.md#reference-b8069670fa474e4799ac29f0d693ca38), [req=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76), [icc=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-icc.md#reference-182b5679e21e4df3b4d330535a5a7517), [iccEmbed=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-iccembed.md#reference-e3b774fb322046a2a6dde3a7bab5583e), [pathEmbed=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-pathembed.md#reference-9ccf0771d6634cf68c1c9c33cd428301), [pscan](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-pscan.md#reference-b8101ed8e6c04dd28173f9597e52b135).
