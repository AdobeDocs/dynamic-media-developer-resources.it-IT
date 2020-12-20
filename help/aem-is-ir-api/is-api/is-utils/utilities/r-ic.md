---
description: Image Conversion Utility.
seo-description: Image Conversion Utility.
seo-title: ic
solution: Experience Manager
title: ic
topic: Scene7 Image Serving - Image Rendering API
uuid: 08fabcc9-d0b5-4136-81fc-ac896c341e1d
translation-type: tm+mt
source-git-commit: e0f8153b038446180ddad313e591828223ed31e9
workflow-type: tm+mt
source-wordcount: '1208'
ht-degree: 1%

---


# ic {#ic}

Image Conversion Utility.

`ic` è uno strumento della riga di comando che converte i file di immagine nel formato TIFF piramidale ottimizzato (PTIFF). Mentre Image Serving può elaborare le immagini senza conversione, si consiglia di convertire tutte le immagini più grandi di 512x512 pixel in PTIFF. Questa conversione assicura prestazioni e utilizzo delle risorse ottimali del server e riduce i tempi di risposta.

Si consiglia di codificare in JPEG i file PTIFF che contengono contenuto fotografico (specificare `-jpegcompress`). I contenuti generati dai computer possono beneficiare di una compressione senza perdita di dati (`-deflatecompress` o `-lzwcompress`). A meno che non sia necessaria una conversione del colore o del tipo di pixel, i dati dell’immagine sorgente JPEG vengono trasferiti al PTIFF senza decodifica, per evitare il degrado della qualità. In questo caso, le opzioni di compressione specificate si applicano solo ai livelli della piramide a risoluzione inferiore.

Se non state convertendo immagini di grandi dimensioni, non dovete impostare i parametri che controllano la quantità di memoria da utilizzare. Tuttavia, in caso affermativo, date a `ic` più memoria utilizzando l&#39;impostazione `-maxmem` descritta di seguito. Una buona regola di pollice per calcolare la quantità di memoria necessaria è moltiplicare la larghezza dell&#39;immagine per l&#39;altezza dell&#39;immagine per il numero di canali. Ad esempio, quattro per un’immagine RGB con alfa per tre. Inoltre, se i canali sono a 16 bit per componente invece di 8, il risultato finale è doppio.

## Utilizzo {#section-fb5293fa79894442aba831c1e14c5cc9}

`ic -convert` `[`*`options`*`]` *`sourceFiledestFile`*

` ic -convert` `[`*`options`*`]` *`sourceFolderdestFolder`*

` -c -convert` `[`*`options`*`]` *`sourceFiledestFolder`*

<table id="table_E368E220299D449D8311478AB5042987"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"><i>options</i> </span> </span> </p> </td> 
   <td colname="col2"> <p>Opzioni dei comandi (vedere di seguito). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> <i>sourceFile</i> </span> </span> </p> </td> 
   <td colname="col2"> <p>Singolo file immagine di input. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"><i>destFile</i></span> </span> </p> </td> 
   <td colname="col2"> <p>File PTIFF di output singolo (non valido se utilizzato con SourceDirectory). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"><i>sourceFolder</i></span> </span> </p> </td> 
   <td colname="col2"> <p>Cartella contenente immagini di input. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"><i>destFolder</i></span> </span> </p> </td> 
   <td colname="col2"> <p>Cartella in cui vengono scritti i file PTIFF di output. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Restituisce {#section-36a2dcfa39824d29b69547c432366219}

0 in caso di esito positivo. Se si verifica un errore, viene restituito un valore diverso da zero e i dettagli dell&#39;errore vengono inviati a `stderr`.

## Opzioni {#section-df311ace43f947b3817b60b667ae04ca}

<table id="table_02011C7C076745A8BF4378B22C48C8A3"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -non compresso  </span> </p> </td> 
   <td colname="col2"> <p>Non comprimete l’immagine di output. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -deflatecompress  </span> </p> </td> 
   <td colname="col2"> <p>Utilizzare la compressione deflate (zip) (impostazione predefinita). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -lzwcompress  </span> </p> </td> 
   <td colname="col2"> <p>Utilizzare la compressione Lempel-Ziv-Welch (LZW). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -jpegcompress  </span> </p> </td> 
   <td colname="col2"> <p>Utilizzate la codifica JPEG. Ignorato se <span class="codeph"> <span class="varname"> sourceFile </span> </span> include dati alfa. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -jpegquality  &lt;&gt; quality  </span>&gt;  </span><span class="varname"> </span></p> </td> 
   <td colname="col2"> <p>Qualità JPEG (0-100; il valore predefinito è 95). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -fullsamplechrominance  </span> </p> </td> 
   <td colname="col2"> <p>Disattivate il downsampling della crominanza JPEG (per migliorare la qualità del testo a colori e della grafica). Questo non ha alcun effetto sulle immagini di output CMYK o in scala di grigio. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -usm  &lt;&gt; amount  </span>&gt;  &lt;&gt; radius  </span>&gt;  &lt;&gt; threshold  </span>&gt;  &lt;&gt; monocromatico  </span>&gt;  </span><span class="varname"><span class="varname"><span class="varname"><span class="varname"> </span></span></span></span></p> </td> 
   <td colname="col2"> <p>Applica la maschera di contrasto ai livelli della piramide sottocampionata. Per ulteriori informazioni, vedere <a href="../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-usm.md#reference-51ac75adadfe4346ab60953192d0a1aa" type="reference" format="dita" scope="local"> op_usm= </a>. (Non applicato all’immagine a risoluzione completa). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -applyClippath  </span> </p> </td> 
   <td colname="col2"> <p>Per creare i dati alfa associati, utilizzate il percorso della clip nel file di origine, se presente. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -dpi  &lt;&gt; dpi  </span>&gt;  </span><span class="varname"> </span></p> </td> 
   <td colname="col2"> <p>risoluzione di stampa (dpi) per <span class="codeph"> <span class="varname"> destFile </span> </span>; se non viene specificato, la risoluzione di stampa di <span class="codeph"> srcFile </span> viene copiata in <span class="codeph"> <span class="varname"> destFile </span> </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -autocrop  &lt;&gt; corner  </span>&gt;  &lt;&gt; mode  </span>&gt;  &lt;&gt; Allowance  </span>&gt;  &lt;&gt; infoFile  </span>&gt;  </span><span class="varname"><span class="varname"><span class="varname"><span class="varname"> </span></span></span></span></p> </td> 
   <td colname="col2"> <p>Calcolare un rettangolo di ritaglio per ridurre al minimo lo sfondo a colori in tinta unita. Se l’algoritmo di ritaglio automatico causa il ritaglio dell’intera immagine, non viene generata alcuna informazione di ritaglio. </p> <p>Per calcolare il rettangolo di ritaglio senza convertire l'immagine, specificate <span class="codeph"> -autocrop </span> senza <span class="codeph"> -convert </span> e senza <span class="codeph"> <span class="varname"> destFile.</span> </span></p>

<p><i><b>corner</b></i> - ul | ur | ll | lr </p>
   <p> Specifica quale angolo dell’immagine usare come punto di partenza. Ignorato se la modalità è 1.</p>
   <p><i><b>mode</b></i> - 0 | 1</p>
   <p>Impostare su 0 per il ritaglio in base al colore del pixel d’angolo specificato; funziona sui dati di colore premoltiplicati se i dati alfa sono associati all'immagine di origine.</p>
   <p>Impostare su 1 per ritagliare in base ai dati alfa; corner viene ignorato e 0 è sempre il valore seed; se non sono associati dati alfa all'immagine di origine, non viene applicato alcun ritaglio.</p> 
   <p><i><b>tolleranza</b></i>  - Corrispondenza tolleranza. Valore reale da 0,0 a 1,0. Specifica la tolleranza per i valori dei componenti pixel corrispondenti. Impostate su 0 per le corrispondenze esatte.</p>
   <p><i><b>infoFile</b></i>  - Percorso e nome del file di output XML in cui verranno scritti i dati di ritaglio.</p>

<p>  
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -embedXmpData  </span> </p> </td> 
   <td colname="col2"> <p>Copiare XMP metadati, se disponibili, da <span class="codeph"> <span class="varname"> sourceFile </span> </span> a <span class="codeph"> <span class="varname"> destFile </span> </span> senza modifiche. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -embedColorProfile  </span> </p> </td> 
   <td colname="col2"> <p> Incorpora il profilo colore ICC in <span class="codeph"> <span class="varname"> destFile </span> </span>, se disponibile (nessun profilo è incorporato per impostazione predefinita). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -imageprofile  &lt;&gt; file  </span>&gt;  </span><span class="varname"> </span></p> </td> 
   <td colname="col2"> <p>Percorso e nome di un file di profilo ICC. Definisce lo spazio colore di <span class="codeph"> <span class="varname"> sourceFile </span> </span> e deve corrispondere al tipo di pixel. Deve essere specificato solo se non è incorporato alcun profilo in <span class="codeph"> <span class="varname"> sourceFile </span> </span>, in quanto sostituisce il profilo incorporato. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -viewprofile  &lt;&gt; file  </span>&gt;  </span><span class="varname"> </span></p> </td> 
   <td colname="col2"> <p>Percorso e nome di un file di profilo ICC. Definisce il tipo di pixel e lo spazio colore di <span class="codeph"> <span class="varname"> destFile </span> </span>. L'IC converte in questo profilo se <span class="codeph"> <span class="varname"> sourceFile </span> </span> ha un profilo incorporato o se è specificato anche <span class="codeph"> -imageprofile </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -IntentPerceptual  </span> </p> </td> 
   <td colname="col2"> <p>Intento di rendering percettivo per le conversioni dello spazio colore. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -IntentRelColorimetric  </span> </p> </td> 
   <td colname="col2"> <p> Intento di rendering Colorimetrico relativo per le conversioni dello spazio colore (predefinito). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -IntentAbsColorimetric  </span> </p> </td> 
   <td colname="col2"> <p>Intento di rendering Colorimetrico assoluto per le conversioni dello spazio colore. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -intentoSaturazione  </span> </p> </td> 
   <td colname="col2"> <p>Intento di rendering della saturazione per le conversioni dello spazio colore. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -cmsNoBlackPointCompensation  </span> </p> </td> 
   <td colname="col2"> <p>Disattiva compensazione punto nero per determinate conversioni colore </p> <p>Abilitato per impostazione predefinita. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -cmsNoDither8  </span> </p> </td> 
   <td colname="col2"> <p>Disattivate il dithering (diffusione errore) durante la conversione del colore. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -Mantainpixeltype  </span> </p> </td> 
   <td colname="col2"> <p> Disattiva la conversione automatica da CMYK a RGB. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> - forceJPEGDecompress  </span> </p> </td> 
   <td colname="col2"> <p>Forza la decodifica e la codifica delle immagini di input JPEG. </p> <p> <b>Attenzione:</b> l’applicazione di questa opzione può ridurre la qualità dell’immagine. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -downsampling2x2  </span> </p> </td> 
   <td colname="col2"> <p>Usate il filtro di ricampionamento della qualità standard (bilineare). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -downsampling8x8  </span> </p> </td> 
   <td colname="col2"> <p>Usate il filtro di ricampionamento di qualità superiore (finestra Lanczos) (impostazione predefinita). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -downsampling8x8FlashPix  </span> </p> </td> 
   <td colname="col2"> <p>Usate un filtro di ricampionamento di qualità superiore (FlashPix). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -downsampling8x8BicubicSharp  </span> </p> </td> 
   <td colname="col2"> <p>Downsampling con filtro bicubico 8x8 stile Photoshop. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -nousing  </span> </p> </td> 
   <td colname="col2"> <p> Se specificata come prima opzione, rimuove l'output delle informazioni di utilizzo quando vengono rilevate opzioni non valide. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -overwrite  </span> </p> </td> 
   <td colname="col2"> <p>Consentire la sovrascrittura di un <span class="codeph"> <span class="varname"> destFile </span> </span> esistente. Per impostazione predefinita, al nome del file viene aggiunto un suffisso numerico per impedire la sovrascrittura. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -skiphidden  </span> </p> </td> 
   <td colname="col2"> <p>Ignora i file sorgente nascosti. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -continue eonerror  </span> </p> </td> 
   <td colname="col2"> <p>Non interrompere l'elaborazione quando si verifica un errore. Ha un effetto solo quando si elaborano più file. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -logfile  &lt;&gt; file  </span>&gt;  </span><span class="varname"> </span></p> </td> 
   <td colname="col2"> <p>Percorso e nome del file di registro (per impostazione predefinita, <span class="codeph"> stdout </span>). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> - &lt;&gt; livello loglevel  </span>&gt;  </span><span class="varname"> </span></p> </td> 
   <td colname="col2"> <p>Livello di registro. </p> 
   <p>&lt; 0=""&gt;</p>
   <p>0 - Elenca i file da elaborare.</p>
   <p>1 - Aggiunta di rapporti per i file non necessari.</p>
   <p>2 - Aggiunta di rapporti sullo stato di avanzamento.</p>
   <p>3 - Aggiungete i rapporti su ogni file rilevato.</p>
   <p>4 - Aggiungete i rapporti sullo stato di avanzamento a livello di file.</p>
   <p> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -logappend  </span> </p> </td> 
   <td colname="col2"> <p>Aggiungi al file di registro (predefinito). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -nologappend  </span> </p> </td> 
   <td colname="col2"> <p>Sovrascrivi file di registro. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -logprogressmsec  &lt;&gt; msec  </span>&gt;  </span><span class="varname"> </span></p> </td> 
   <td colname="col2"> <p>Intervallo di registrazione in msec per il livello 2 e superiore (il valore predefinito è 3000). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -maxmem  &lt;&gt; byte  </span>&gt;  </span><span class="varname"> </span></p> </td> 
   <td colname="col2"> <p>Limite di utilizzo della memoria. Deve essere almeno 10 MB. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -maxmpercentuale  &lt;&gt; percentuale  </span>&gt;  </span><span class="varname"> </span></p> </td> 
   <td colname="col2"> <p>Limite di utilizzo della memoria. Il valore predefinito è il 25% della memoria fisica. Se non viene impostato in modo esplicito <span class="codeph"> maxmem </span> o <span class="codeph"> maxmpercentuale </span>, viene utilizzato il valore massimo predefinito. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -version  </span> </p> </td> 
   <td colname="col2"> <p> Restituisce le informazioni sulla versione per questa utility. Specificate senza altre opzioni. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Formati immagine di input supportati {#section-ab13d941d6724e65b9f84b62d949d31c}

Nella tabella seguente sono elencati i formati dei file immagine e le opzioni di formato supportati da IC.

<table id="table_1EB2B60993D34B1887275EA4E3491401"> 
 <thead> 
  <tr> 
   <th class="entry"> <p> <b> Formato</b> </p> </th> 
   <th class="entry"> <p> <b> Pixel </b> <b> TypeBits/Chan</b> </p> </th> 
   <th class="entry"> <p> <b> Bit/Chan</b> </p> </th> 
   <th class="entry"> <p> <b> Compressione</b> </p> </th> 
   <th class="entry"> <p> <b> Note</b> </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <b> BMP</b> <p> (bitmap Windows) </p> </td> 
   <td> <p> RGB | indicizzato </p> </td> 
   <td> <p> 3 | 5/6 | 8 </p> </td> 
   <td> <p> non compresso | RLE </p> </td> 
   <td> <p> 5/6 bit/canale indica il supporto per RGB a 16 bit (5-5-5 e 5-6-5 bit/canale). </p> </td> 
  </tr> 
  <tr> 
   <td> <b> EPS</b> <p> (Encapsulated Postscript) </p> </td> 
   <td> <p> CMYK | RGB | grigia </p> </td> 
   <td> <p> 8 </p> </td> 
   <td> <p> ASCII | ASCII85 | Binario | JPEG </p> </td> 
   <td> <p> Sono supportati solo i file EPS generati da Photoshop. </p> </td> 
  </tr> 
  <tr> 
   <td> </td> 
   <td> </td> 
   <td> </td> 
   <td> </td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td> <p> CompuServe </p> <b>GIF</b> </td> 
   <td> <p> indicizzato </p> </td> 
   <td> <p> 8 </p> </td> 
   <td> <p> LZW </p> </td> 
   <td> <p> Se presente, il valore della trasparenza nella palette è convertito in alfa. </p> </td> 
  </tr> 
  <tr> 
   <td> <b> JPG</b> <p> (JFIF/JPEG) </p> </td> 
   <td> <p> CMYK | RGB | grigia </p> </td> 
   <td> <p> 8 </p> </td> 
   <td> <p> JPEG </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> Photoshop </p> <b>PSD</b> </td> 
   <td> <p> CMYK | CMYKA | RGB | RGBA | grigia | GreyA </p> </td> 
   <td> <p> 1 | 8 | 16 </p> </td> 
   <td> <p> non compresso | compressi </p> </td> 
   <td> <p> Solo immagine unita; i livelli e i canali aggiuntivi vengono ignorati. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> Macintosh </p> <b>PICT</b> </td> 
   <td> <p> RGB </p> </td> 
   <td> <p> 8 </p> </td> 
   <td> <p> RLE </p> </td> 
   <td> <p> Solo dati bitmap; i dati vettoriali vengono ignorati. </p> </td> 
  </tr> 
  <tr> 
   <td> <b> PNG</b> </td> 
   <td> <p> RGB | RGBA | grigia | GreyA | indicizzato </p> </td> 
   <td> <p> 1 | 2 | 4 | 8 | 16 </p> </td> 
   <td> <p> compresso </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <b> TIFF</b> </td> 
   <td> <p> CMYK | CMYKA | RGB | RGBA | grigia | GreyA | indicizzato </p> </td> 
   <td> <p> 3 | 8 | 16 </p> </td> 
   <td> <p> non compresso | ZIP | LZW | JPEG | RUOLO CCITT | CCITT G3 | CCITT G4 | Packbit </p> </td> 
   <td> <p> Ad eccezione del primo canale alfa associato, i canali aggiuntivi vengono ignorati. </p> </td> 
  </tr> 
 </tbody> 
</table>

I profili ICC incorporati sono riconosciuti nei file EPS, JPG, PSD, PNG e TIFF.

I percorsi incorporati e i metadati XMP sono riconosciuti nei file EPS, JPG, PSD e TIFF.

## Esempi {#section-3c1986b30315431989bd76b1ee5bef6d}

Convertite una singola immagine con la migliore qualità e mantenetela nella stessa cartella:

`ic -convert src/myFile.png src/myFile.tif`

Convertite tutte le immagini in *`srcFolder`* in TIFF con codifica JPEG e inserite in *`destFolder`*:

`ic -convert -jpegcompress -jpegquality 90 -overwrite -continueOnError srcFolder destFolder`

Converti tutte le immagini in *`srcFolder`*. I dati immagine codificati dei file JPG vengono utilizzati per la compressione LZW a risoluzione piena, senza perdita di dati per il resto della piramide delle immagini di queste immagini e per l&#39;intera immagine di output di tutti i file di input non JPG. Tipi di pixel, profili colore incorporati, metadati XMP ecc. sono mantenute.

`ic -convert -lzwcompress -embedXmpData -embedColorProfile -maintainpixeltype -overwrite -continueOnError srcFolder destFolder`
