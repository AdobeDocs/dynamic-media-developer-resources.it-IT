---
description: Image Conversion Utility
solution: Experience Manager
title: ic
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: ab653aae-532b-4f3d-8541-f6296fbf9172
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '1239'
ht-degree: 0%

---

# ic {#ic}

Image Conversion Utility

`ic` è uno strumento da riga di comando che converte i file immagine nel formato PTIFF (Pyramid TIFF Format) ottimizzato. Mentre Image Server può elaborare le immagini senza conversione, ti consigliamo di convertire tutte le immagini di dimensioni superiori a 512x512 pixel in PTIFF. Questa conversione garantisce prestazioni ottimali del server e l’utilizzo delle risorse, riducendo al minimo i tempi di risposta.

È consigliabile che i file PTIFF contenenti contenuto fotografico siano codificati in JPEG (specificare `-jpegcompress`). I contenuti generati dal computer possono beneficiare di una compressione senza perdita (`-deflatecompress` o `-lzwcompress`). A meno che non sia necessaria una conversione del colore o del tipo di pixel, i dati dell&#39;immagine sorgente JPEG vengono trasferiti al PTIFF senza decodifica, per evitare il degrado della qualità. In questo caso, le opzioni di compressione specificate si applicano solo ai livelli piramidali a risoluzione inferiore.

Se non si convertono immagini di grandi dimensioni, non è necessario impostare i parametri che controllano la quantità di memoria da utilizzare. Tuttavia, se lo sei, concedi a `ic` più memoria utilizzando l&#39;impostazione `-maxmem` descritta di seguito. Una buona regola per calcolare la quantità di memoria necessaria è moltiplicare la larghezza dell&#39;immagine per l&#39;altezza dell&#39;immagine per il numero di canali. Ad esempio, quattro per un’immagine RGB con alfa per tre. Inoltre, se i canali sono a 16 bit per componente invece di 8, il risultato finale sarà doppio.

## Utilizzo {#section-fb5293fa79894442aba831c1e14c5cc9}

`ic -convert` `[`*`options`*`]`*`sourceFiledestFile`*

` ic -convert` `[`*`options`*`]`*`sourceFolderdestFolder`*

` -c -convert` `[`*`options`*`]`*`sourceFiledestFolder`*

<table id="table_E368E220299D449D8311478AB5042987"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"><i>opzioni</i> </span> </span> </p> </td> 
   <td colname="col2"> <p>Opzioni di comando (vedere di seguito). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> <i>sourceFile</i> </span> </span> </p> </td> 
   <td colname="col2"> <p>File immagine di input singolo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"><i>destFile</i></span> </span> </p> </td> 
   <td colname="col2"> <p>Singolo file PTIFF di output (non valido se utilizzato con SourceDirectory). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"><i>cartellaOrigine</i></span> </span> </p> </td> 
   <td colname="col2"> <p>Cartella contenente le immagini di input. </p> </td> 
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
   <td colname="col1"> <p> <span class="codeph"> - non compresso </span> </p> </td> 
   <td colname="col2"> <p>Non comprimere l'immagine di output. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -deflatecompress </span> </p> </td> 
   <td colname="col2"> <p>Utilizza la compressione Deflate (zip) (impostazione predefinita). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -lzwcompress </span> </p> </td> 
   <td colname="col2"> <p>Utilizzare la compressione Lempel-Ziv-Welch (LZW). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -jpegcompress </span> </p> </td> 
   <td colname="col2"> <p>Utilizza la codifica JPEG. Ignorato se <span class="codeph"> <span class="varname"> sourceFile </span> </span> include dati alfa. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -jpegquality &lt; <span class="varname"> qualità </span>&gt; </span> </p> </td> 
   <td colname="col2"> <p>Qualità JPEG (0-100; il valore predefinito è 95). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> - fullsamplechrominance </span> </p> </td> 
   <td colname="col2"> <p>Disattiva il downsampling della crominanza JPEG (può migliorare la qualità del testo e della grafica a colori). Questo non ha alcun effetto sulle immagini di output in CMYK o in scala di grigi. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -usm &lt; <span class="varname"> importo </span>&gt; &lt; <span class="varname"> raggio </span>&gt; &lt; soglia <span class="varname"> </span>&gt; &lt; <span class="varname"> monocromatico </span>&gt; </span> </p> </td> 
   <td colname="col2"> <p>Applicate la maschera di contrasto ai livelli piramidali sottocampionati. Per ulteriori dettagli, vedere <a href="../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-usm.md#reference-51ac75adadfe4346ab60953192d0a1aa" type="reference" format="dita" scope="local"> op_usm= </a>. (non applicata all'immagine a risoluzione completa). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -applyClippath </span> </p> </td> 
   <td colname="col2"> <p>Utilizzate il percorso di clip nel file di origine, se presente, per creare i dati alfa associati. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -dpi &lt; <span class="varname"> dpi </span>&gt; </span> </p> </td> 
   <td colname="col2"> <p>Risoluzione di stampa (dpi) per <span class="codeph"> <span class="varname"> destFile </span> </span>; se non specificata, la risoluzione di stampa di <span class="codeph"> srcFile </span> viene copiata in <span class="codeph"> <span class="varname"> destFile </span> </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -autocrop &lt; <span class="varname"> angolo </span>&gt; &lt; modalità <span class="varname"> </span>&gt; &lt; tolleranza <span class="varname"> </span>&gt; &lt; <span class="varname"> infoFile </span>&gt; </span> </p> </td> 
   <td colname="col2"> <p>Calcola un rettangolo di ritaglio per ridurre al minimo lo sfondo di un colore a tinta unita. Se con l’algoritmo di ritaglio automatico l’intera immagine viene ritagliata, non viene generata alcuna informazione di ritaglio. </p> <p>Per calcolare il rettangolo di ritaglio senza convertire l'immagine, specificare <span class="codeph"> -autocrop </span> senza <span class="codeph"> -convert </span> e senza <span class="codeph"> <span class="varname"> destFile.</span> </span></p>

<p><i><b>angolo</b></i> - ul | ur | ll | lr </p>
   <p> Specifica l'angolo dell'immagine da utilizzare come punto di partenza. Ignorato se la modalità è 1.</p>
   <p><i><b>modalità</b></i> - 0 | 1</p>
   <p>Impostate questo valore su 0 per ritagliare in base al colore del pixel d'angolo specificato; funziona sui dati di colore premoltiplicati se all'immagine sorgente sono associati dati alfa.</p>
   <p>Impostate questo valore su 1 per ritagliare in base ai dati alfa; corner viene ignorato e 0 è sempre il valore di partenza; non viene applicato alcun ritaglio se all'immagine sorgente non sono associati dati alfa.</p> 
   <p><i><b>tolleranza</b></i> - Corrispondenza tolleranza. Valore reale da 0,0 a 1,0. Specifica la tolleranza per i valori dei componenti pixel corrispondenti. Imposta su 0 per le corrispondenze esatte.</p>
   <p><i><b>infoFile</b></i> - Percorso e nome del file di output XML in cui vengono scritti i dati delle informazioni di ritaglio.</p>

<p>  
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -embedXmpData </span> </p> </td> 
   <td colname="col2"> <p>Copiare i metadati XMP, se disponibili, da <span class="codeph"> <span class="varname"> sourceFile </span> </span> a <span class="codeph"> <span class="varname"> destFile </span> </span> senza modifiche. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -embedColorProfile </span> </p> </td> 
   <td colname="col2"> <p> Incorpora il profilo colore ICC in <span class="codeph"> <span class="varname"> destFile </span> </span>, se disponibile (nessun profilo è incorporato per impostazione predefinita). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -imageprofile &lt; <span class="varname"> file </span>&gt; </span> </p> </td> 
   <td colname="col2"> <p>Percorso e nome di un file di profilo ICC. Definisce lo spazio colore di <span class="codeph"> <span class="varname"> sourceFile </span> </span> e deve corrispondere al relativo tipo di pixel. È necessario specificare solo se non è incorporato alcun profilo in <span class="codeph"> <span class="varname"> sourceFile </span> </span>, in quanto questo sostituisce il profilo incorporato. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -viewprofile &lt; <span class="varname"> file </span>&gt; </span> </p> </td> 
   <td colname="col2"> <p>Percorso e nome di un file di profilo ICC. Definisce il tipo di pixel e lo spazio colore di <span class="codeph"> <span class="varname"> destFile </span> </span>. IC viene convertito in questo profilo se <span class="codeph"> <span class="varname"> sourceFile </span> </span> ha un profilo incorporato o se <span class="codeph"> -imageprofile </span> è specificato. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -intentPerceptual </span> </p> </td> 
   <td colname="col2"> <p>Intento di rendering percettivo per le conversioni di spazio colore. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -intentRelColorimetric </span> </p> </td> 
   <td colname="col2"> <p> Intento di rendering colorimetrico relativo per le conversioni dello spazio colore (impostazione predefinita). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -intentAbsColorimetric </span> </p> </td> 
   <td colname="col2"> <p>Intento di rendering colorimetrico assoluto per le conversioni dello spazio colore. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -intentSaturation </span> </p> </td> 
   <td colname="col2"> <p>Intento di rendering di saturazione per le conversioni dello spazio colore. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -cmsNoBlackPointCompensation </span> </p> </td> 
   <td colname="col2"> <p>Disattiva la compensazione del punto nero per determinate conversioni di colore </p> <p>Abilitato per impostazione predefinita. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -cmsNoDither8 </span> </p> </td> 
   <td colname="col2"> <p>Disattiva il dithering (diffusione degli errori) durante la conversione del colore. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -maintainpixeltype </span> </p> </td> 
   <td colname="col2"> <p> Disattiva la conversione automatica da CMYK a RGB. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> - forceJPEGDecompress </span> </p> </td> 
   <td colname="col2"> <p>Imponi la decodifica e la nuova codifica delle immagini di input JPEG. </p> <p> <b>Attenzione:</b> L'applicazione di questa opzione potrebbe ridurre la qualità dell'immagine. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -downsampling2x2 </span> </p> </td> 
   <td colname="col2"> <p>Utilizzare un filtro di ricampionamento di qualità standard (bi-lineare). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -downsample8x8 </span> </p> </td> 
   <td colname="col2"> <p>Utilizza un filtro di ricampionamento di qualità superiore (finestra Lanczos) (impostazione predefinita). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -downsample8x8FlashPix </span> </p> </td> 
   <td colname="col2"> <p>Utilizzare un filtro di ricampionamento di qualità superiore (FlashPix). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -downsample8x8BicubicSharp </span> </p> </td> 
   <td colname="col2"> <p>Downsampling con filtro bicubic-sharp in stile Photoshop 8x8. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -nousage </span> </p> </td> 
   <td colname="col2"> <p> Se specificata come prima opzione, sopprime l’output delle informazioni di utilizzo quando vengono rilevate opzioni non valide. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -sovrascrivi </span> </p> </td> 
   <td colname="col2"> <p>Consenti la sovrascrittura di un <span class="codeph"> <span class="varname"> destFile </span> </span> esistente. Per impostazione predefinita, al nome del file viene aggiunto un suffisso numerico per impedire la sovrascrittura. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -nascosto </span> </p> </td> 
   <td colname="col2"> <p>Ignora i file di origine nascosti. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -continueonerror </span> </p> </td> 
   <td colname="col2"> <p>Non interrompere l’elaborazione quando si verifica un errore. Ha effetto solo quando si elaborano più file. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -logfile &lt; <span class="varname"> file </span>&gt; </span> </p> </td> 
   <td colname="col2"> <p>Percorso e nome del file di registro (impostazione predefinita: <span class="codeph"> stdout </span>). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -loglevel &lt; <span class="varname"> livello </span>&gt; </span> </p> </td> 
   <td colname="col2"> <p>Livello del registro. </p> 
   <p>&lt; 0 - Registrazione disabilitata.</p>
   <p>0 - Elencare i file da elaborare.</p>
   <p>1 - Aggiungere rapporti per i file non necessari.</p>
   <p>2 - Aggiungere rapporti sull’avanzamento.</p>
   <p>3 - Aggiungere rapporti su ogni file rilevato.</p>
   <p>4 - Aggiungere rapporti sull’avanzamento a livello di file.</p>
   <p> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -logappend </span> </p> </td> 
   <td colname="col2"> <p>Aggiungi al file di registro (impostazione predefinita). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -nologappend </span> </p> </td> 
   <td colname="col2"> <p>Sovrascrivi file di registro. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -logprogressmsec &lt; <span class="varname"> msec </span>&gt; </span> </p> </td> 
   <td colname="col2"> <p>Intervallo di registrazione in msec per loglevel 2 e versioni successive (il valore predefinito è 3000). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -maxmem &lt; <span class="varname"> byte </span>&gt; </span> </p> </td> 
   <td colname="col2"> <p>Limite di utilizzo della memoria. Deve essere di almeno 10 MB. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -maxmempercent &lt; <span class="varname"> percent </span>&gt; </span> </p> </td> 
   <td colname="col2"> <p>Limite di utilizzo della memoria. Il valore predefinito corrisponde al 25% della memoria fisica. Se né <span class="codeph"> maxmem </span> né <span class="codeph"> maxmempercent </span> sono impostati in modo esplicito, viene utilizzato il valore predefinito maxmempercent. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> - versione </span> </p> </td> 
   <td colname="col2"> <p> Restituire le informazioni sulla versione per questa utility. Specifica senza altre opzioni. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Formati supportati per le immagini in ingresso {#section-ab13d941d6724e65b9f84b62d949d31c}

Nella tabella seguente sono elencati i formati di file immagine e le opzioni di formato supportate da IC.

<table id="table_1EB2B60993D34B1887275EA4E3491401"> 
 <thead> 
  <tr> 
   <th class="entry"> <p> Formato <b></b> </p> </th> 
   <th class="entry"> <p> <b> Tipo Di Pixel</b> <b> Bit/Chan</b> </p> </th> 
   <th class="entry"> <p> <b> Bit/Chan</b> </p> </th> 
   <th class="entry"> <p> Compressione <b></b> </p> </th> 
   <th class="entry"> <p> <b> note</b> </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <b> BMP</b> <p> (Bitmap Windows) </p> </td> 
   <td> <p> RGB | indicizzato </p> </td> 
   <td> <p> 1 | 5/6 | 8 </p> </td> 
   <td> <p> non compresso | RUOLO </p> </td> 
   <td> <p> 5/6 bit/canale indica il supporto per RGB a 16 bit (5-5-5 e 5-6-5 bit/canale). </p> </td> 
  </tr> 
  <tr> 
   <td> <b> EPS</b> <p> (PostScript incapsulato) </p> </td> 
   <td> <p> CMYK | RGB | grigio </p> </td> 
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
   <td> <p> Se presente, il valore di trasparenza nella palette viene convertito in alfa. </p> </td> 
  </tr> 
  <tr> 
   <td> <b> JPG</b> <p> (JFIF/JPEG) </p> </td> 
   <td> <p> CMYK | RGB | grigio </p> </td> 
   <td> <p> 8 </p> </td> 
   <td> <p> JPEG </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> Photoshop </p> <b>PSD</b> </td> 
   <td> <p> CMYK | CMYKA | RGB | RGBA | grigio | grigioA </p> </td> 
   <td> <p> 1 | 8 | 16 </p> </td> 
   <td> <p> non compresso | compresso </p> </td> 
   <td> <p> Solo immagine unita; i livelli e i canali aggiuntivi vengono ignorati. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> Macintosh </p> <b>IMMAGINE</b> </td> 
   <td> <p> RGB </p> </td> 
   <td> <p> 8 </p> </td> 
   <td> <p> RUOLO </p> </td> 
   <td> <p> Solo dati bitmap; i dati vettoriali vengono ignorati. </p> </td> 
  </tr> 
  <tr> 
   <td> <b> PNG</b> </td> 
   <td> <p> RGB | RGBA | grigio | grigioA | indicizzato </p> </td> 
   <td> <p> 1 | 2 | 4 | 8 | 16 </p> </td> 
   <td> <p> compresso </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <b> TIFF</b> </td> 
   <td> <p> CMYK | CMYKA | RGB | RGBA | grigio | grigioA | indicizzato </p> </td> 
   <td> <p> 1 | 8 | 16 </p> </td> 
   <td> <p> non compresso | ZIP | LZW | JPEG | REGOLA CCITT | CCITT G3 | CCITT G4 | Pacchetti </p> </td> 
   <td> <p> Ad eccezione del primo canale alfa associato, i canali aggiuntivi vengono ignorati. </p> </td> 
  </tr> 
 </tbody> 
</table>

I profili ICC incorporati vengono riconosciuti nei file EPS, JPG PSD, PNG e TIFF.

I percorsi incorporati e i metadati XMP vengono riconosciuti nei file EPS, JPG PSD, e TIFF.

## Esempi {#section-3c1986b30315431989bd76b1ee5bef6d}

Converti una singola immagine alla migliore qualità e mantienila nella stessa cartella:

`ic -convert src/myFile.png src/myFile.tif`

Converti tutte le immagini in *`srcFolder`* in TIFF piramidali con codifica JPEG e inserisci in *`destFolder`*:

`ic -convert -jpegcompress -jpegquality 90 -overwrite -continueOnError srcFolder destFolder`

Convertire tutte le immagini in *`srcFolder`*. I dati immagine codificati dei file JPG vengono utilizzati per la compressione LZW a piena risoluzione, senza perdita di dati, per il resto della piramide di immagini di queste immagini e per l&#39;intera immagine di output di tutti i file di input non JPG. I tipi di pixel, i profili di colore incorporati, i metadati XMP e così via. sono mantenuti.

`ic -convert -lzwcompress -embedXmpData -embedColorProfile -maintainpixeltype -overwrite -continueOnError srcFolder destFolder`
