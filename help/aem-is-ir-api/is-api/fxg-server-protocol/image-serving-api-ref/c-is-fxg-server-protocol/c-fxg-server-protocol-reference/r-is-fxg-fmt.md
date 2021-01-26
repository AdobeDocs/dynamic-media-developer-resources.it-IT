---
description: Formato immagine di risposta.
seo-description: Formato immagine di risposta.
seo-title: fmt
solution: Experience Manager
title: fmt
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 78ee7545-5ad9-4240-bbfc-20efe3e42ed3
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '288'
ht-degree: 0%

---


# fmt{#fmt}

Formato immagine di risposta.

`fmt=format [,pixelType ]`

<table id="simpletable_66FAABB7BD7A4BBB815A570BEA4C1AE8"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> format</span> </span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> jpeg | png | png-alpha | tif | tif-alpha | swf | pdf | gif | gif-alpha | fxg | fxgraw</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"></td> 
  <td class="stentry"> <p> Specifica il formato di codifica immagine per i dati immagine inviati al client e il tipo MIME di risposta corrispondente per l’intestazione della risposta HTTP. </p> <p> <span class="codeph">  jpeg  </span>: JPEG con perdita </p> <p> <span class="codeph"> png  </span>: PNG senza perdita di dati </p> <p> <span class="codeph"> png-alpha  </span>: PNG senza perdita di dati con canale alfa </p> <p> <span class="codeph">  tif  </span>: TIFF </p> <p> <span class="codeph"> tif-alpha  </span>: TIFF con canale alfa </p> <p> <span class="codeph">  swf  </span>: JPEG con perdita di dati incorporati in un file swf di Adobe </p> <p> <span class="codeph"> pdf  </span>: immagine incorporata in PDF </p> <p> <span class="codeph"> gif  </span>: GIF con 2-256 colori </p> <p> <span class="codeph"> gif-alpha  </span>: GIF con 2-255 colori più trasparenza con colore chiave </p> <p> <span class="codeph"> fxg  </span>: FXG con variabili e modifica DOM applicata </p> <p> <span class="codeph">  fxgraw  </span>: FXG originale memorizzato sul server </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> pixelType</span> </span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> rgb | grigia | cmyk</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"></td> 
  <td class="stentry"> <p> Può essere usato per applicare lo spazio colore di output. </p> <p> <span class="codeph">  rgb  </span>: restituisce dati immagine RGB </p> <p> <span class="codeph"> grigio  </span>: restituisce dati immagine in scala di grigio </p> <p> <span class="codeph"> cmyk  </span>: restituisce dati immagine CMYK </p> </td> 
 </tr> 
</table>

`tiffCompression` è consentito solo se tif, tif-alpha è specificato come formato. Per le opzioni di compressione supportate per questi formati di immagine, fare riferimento alla tabella seguente.

`qlt=` può essere utilizzato per impostare le opzioni di codifica JPEG per i seguenti formati: JPEG, TIFF con compressione JPEG. quantize= può essere utilizzato se fmt=gif o fmt=gif-alpha. Per informazioni dettagliate, fare riferimento alle descrizioni dei comandi. Gli altri formati non dispongono di opzioni impostabili.

Vengono restituiti 8 bit per componente pixel per tutti i formati e `pixelTypes[7]`.

Nella tabella seguente sono elencate le combinazioni valide di formato e `pixelType`, i tipi MIME di risposta HTTP corrispondenti.

<table id="table_54AFE58185004C74971EFBA845E177B6"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p><span class="varname"> format</span> </p> </th> 
   <th colname="col2" class="entry"> <p><span class="varname"> pixelType</span> </p> </th> 
   <th colname="col3" class="entry"> <p>Tipo MIME risposta </p> </th> 
   <th colname="col4" class="entry"> <p>Incorpora profilo ICC </p> </th> 
   <th colname="col5" class="entry"> <p>Opzioni </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p>jpeg </p> </td> 
   <td> <p>rgb, grigia, cmyk </p> </td> 
   <td> <p>&lt;image&gt; </p> </td> 
   <td> <p>yes </p> </td> 
   <td> <p><span class="codeph"> qlt=</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>png, png-alpha </p> </td> 
   <td> <p>rgb, grigio </p> </td> 
   <td> <p>&lt;image&gt; </p> </td> 
   <td> <p>yes </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>tif, tif-alpha </p> </td> 
   <td> <p>rgb, grigia, cmyk </p> </td> 
   <td> <p>&lt;image&gt; </p> </td> 
   <td> <p>yes </p> </td> 
   <td> <p><span class="codeph"> <span class="varname"> tiffCompression</span> ( none | lzw | zip | jpeg), qlt=</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>swf, swf-alpha </p> </td> 
   <td> <p>rgb </p> </td> 
   <td> <p>&lt;application&gt; </p> </td> 
   <td> <p>no </p> </td> 
   <td> <p><span class="codeph"> qlt=  </span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>pdf </p> </td> 
   <td> <p>rgb, grigia, cmyk </p> </td> 
   <td> <p>&lt;application&gt; </p> </td> 
   <td> <p>yes </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>gif, gif-alpha </p> </td> 
   <td> <p>rgb, grigio </p> </td> 
   <td> <p>&lt;image&gt; </p> </td> 
   <td> <p>no </p> </td> 
   <td> <p><span class="codeph"> quantizza=</span> </p> </td> 
  </tr> 
 </tbody> 
</table>

## Esempio {#section-2135175ab3ec453f9f5388d5690b0da4}

[!DNL http://server/is/agm/myRootId/myImageId?fmt=swf]
