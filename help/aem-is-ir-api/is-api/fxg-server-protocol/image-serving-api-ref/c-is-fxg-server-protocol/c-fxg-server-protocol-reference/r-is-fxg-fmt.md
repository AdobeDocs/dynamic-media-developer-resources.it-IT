---
description: Formato immagine di risposta.
solution: Experience Manager
title: fmt
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: e179fc51-0461-4000-99eb-4390c35d5606
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '284'
ht-degree: 0%

---

# fmt{#fmt}

Formato immagine di risposta.

`fmt=format [,pixelType ]`

<table id="simpletable_66FAABB7BD7A4BBB815A570BEA4C1AE8"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> formato</span> </span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> jpeg | png | png-alfa | tif | tif-alfa | swf | pdf | gif | gif-alfa | FXG | fxgraw</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"></td> 
  <td class="stentry"> <p> Specifica il formato di codifica dell'immagine per i dati immagine inviati al client e il tipo MIME di risposta corrispondente per l'intestazione di risposta HTTP. </p> <p> <span class="codeph">  jpeg </span>: JPEG con perdita di dati </p> <p> <span class="codeph"> png </span>: PNG senza perdita di dati </p> <p> <span class="codeph"> png-alfa </span>: PNG senza perdita di dati con canale alfa </p> <p> <span class="codeph">  tif </span>: TIFF </p> <p> <span class="codeph"> tif-alfa </span>: TIFF con canale alfa </p> <p> <span class="codeph">  swf </span>: JPEG con perdita di dati incorporato in un file swf di Adobe </p> <p> <span class="codeph"> pdf </span>: immagine incorporata in PDF </p> <p> <span class="codeph"> gif </span>: GIF con 2-256 colori </p> <p> <span class="codeph"> gif-alfa </span>: GIF con 2-255 colori più trasparenza chiave-colore </p> <p> <span class="codeph"> fxg </span>: FXG con variabili e manipolazione DOM applicate </p> <p> <span class="codeph">  fxgraw </span>: file FXG originale memorizzato sul server </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> pixelType</span> </span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> rgb | grigio | cmyk</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"></td> 
  <td class="stentry"> <p> Può essere utilizzato per influire sullo spazio colore di output. </p> <p> <span class="codeph">  rgb </span>: restituisce i dati immagine RGB </p> <p> <span class="codeph"> grigio </span>: restituisce dati immagine in scala di grigio </p> <p> <span class="codeph"> cmyk </span>: restituisce dati immagine CMYK </p> </td> 
 </tr> 
</table>

`tiffCompression` è consentito solo se il formato specificato è tif, tif-alfa. Per informazioni sulle opzioni di compressione supportate per questi formati di immagine, consulta la tabella seguente.

`qlt=` può essere utilizzato per impostare le opzioni di codifica JPEG per i seguenti formati: JPEG, TIFF con compressione JPEG. quantize= può essere utilizzato se fmt=gif o fmt=gif-alpha. Per ulteriori informazioni, consultare le descrizioni dei comandi. Gli altri formati non dispongono di opzioni impostabili.

vengono restituiti 8 bit per componente pixel per tutti i formati e `pixelTypes[7]`.

Nella tabella seguente sono elencate le combinazioni valide di formato e `pixelType`, i corrispondenti tipi MIME di risposta HTTP.

<table id="table_54AFE58185004C74971EFBA845E177B6"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p><span class="varname"> formato</span> </p> </th> 
   <th colname="col2" class="entry"> <p><span class="varname"> pixelType</span> </p> </th> 
   <th colname="col3" class="entry"> <p>Tipo MIME di risposta </p> </th> 
   <th colname="col4" class="entry"> <p>Incorpora profilo ICC </p> </th> 
   <th colname="col5" class="entry"> <p>Opzioni </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p>jpeg </p> </td> 
   <td> <p>rgb, grigio, cmyk </p> </td> 
   <td> <p>&lt;image/jpeg&gt; </p> </td> 
   <td> <p>sì </p> </td> 
   <td> <p><span class="codeph"> qlt=</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>png, png-alfa </p> </td> 
   <td> <p>rgb, grigio </p> </td> 
   <td> <p>&lt;image/png&gt; </p> </td> 
   <td> <p>sì </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>tif, tif-alfa </p> </td> 
   <td> <p>rgb, grigio, cmyk </p> </td> 
   <td> <p>&lt;image/tiff&gt; </p> </td> 
   <td> <p>sì </p> </td> 
   <td> <p><span class="codeph"> <span class="varname"> tiffCompression</span> ( nessuno | lzw | zip | jpeg), qlt=</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>swf, swf-alfa </p> </td> 
   <td> <p>rgb </p> </td> 
   <td> <p>&lt;application/x-shockwave-flash&gt; </p> </td> 
   <td> <p>no </p> </td> 
   <td> <p><span class="codeph"> qlt= </span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>pdf </p> </td> 
   <td> <p>rgb, grigio, cmyk </p> </td> 
   <td> <p>&lt;application/pdf&gt; </p> </td> 
   <td> <p>sì </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>gif, gif-alfa </p> </td> 
   <td> <p>rgb, grigio </p> </td> 
   <td> <p>&lt;image/gif&gt; </p> </td> 
   <td> <p>no </p> </td> 
   <td> <p><span class="codeph"> quantize= quantizza</span> </p> </td> 
  </tr> 
 </tbody> 
</table>

## Esempio {#section-2135175ab3ec453f9f5388d5690b0da4}

[!DNL http://server/is/agm/myRootId/myImageId?fmt=swf]
