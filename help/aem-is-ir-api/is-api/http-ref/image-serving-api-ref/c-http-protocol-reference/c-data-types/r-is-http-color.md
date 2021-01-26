---
description: Valori colore. È possibile specificare valori di colore utilizzando la notazione esadecimale, un elenco separato da virgole di valori di componente o decimali.
seo-description: Valori colore. È possibile specificare valori di colore utilizzando la notazione esadecimale, un elenco separato da virgole di valori di componente o decimali.
seo-title: color
solution: Experience Manager
title: color
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 61308b8e-eaac-4b2e-8500-2f9efa8a6ce8
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '456'
ht-degree: 13%

---


# color{#color}

Valori colore. È possibile specificare valori di colore utilizzando la notazione esadecimale, un elenco separato da virgole di valori di componente o decimali.

<table id="simpletable_9EBE66066E854ABE978F8F7ADC66BDE3"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> color</span> </span> </p></td> 
  <td class="stentry"> <p> <span class="codeph">{{<span class="varname"> grigio</span>[,<span class="varname"> alfa</span>][g]}|</span> </p> <p> <span class="codeph"> {<span class="varname"> rosso</span>,<span class="varname"> verde</span>,<span class="varname"> blu</span>[ ,<span class="varname"> rgbAlpha</span>][r]}|</span> </p> <p> <span class="codeph"> {<span class="varname"> ciano</span>,  <span class="varname"> magenta</span>,  <span class="varname"> giallo</span>,  <span class="varname"> nero</span>[,alfa]k}|</span> </p> <p> <span class="codeph"> {0x{hex2|hex4}[g]}|</span> </p> <p> <span class="codeph">{[0x]{<span class="varname"> hex6</span>|<span class="varname"> hex8</span>}[r]}|</span> </p> <p> <span class="codeph"> {[0x]{<span class="varname"> hex8</span>|<span class="varname"> hex10</span>}k}[s]</span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> rosso</span>,  <span class="varname"> verde</span>,  <span class="varname"> blu</span>,  <span class="varname"> rgbAlpha</span></span> </p> </td> 
  <td class="stentry"> <p>valore componente colore (0...255, numero decimale) </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> ciano</span>,  <span class="varname"> magenta</span>,  <span class="varname"> giallo</span>,  <span class="varname"> nero</span>,  <span class="varname"> alfa</span></span> </p></td> 
  <td class="stentry"> <p>Valore componente colore CMYK (0,100 %, numero decimale) </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> grigio</span>,  <span class="varname"> alfa</span></span> </p> </td> 
  <td class="stentry"> <p>valore componente colore grigio (0...100%, numero decimale) </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> ex2</span> </span> </p></td> 
  <td class="stentry"> <p>valore compresso del colore grigio esadecimale a due cifre (GG) </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> hex4</span> </span> </p> </td> 
  <td class="stentry"> <p>grigio esadecimale a quattro cifre con valore alfa (GGAA) </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> ex6</span> </span> </p> </td> 
  <td class="stentry"> <p>valore di colore RGB esadecimale compresso a sei cifre (RRGGBB) </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> hex8</span> </span> </p> </td> 
  <td class="stentry"> <p>compresso valore di colore esadecimale RGBA (RRGGBBAA) o CMYK (CCMMYKK) a otto cifre (se specificato con il suffisso "k") </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> hex10</span> </span> </p></td> 
  <td class="stentry"> <p>CMYK esadecimale a dieci cifre compresso con valore alfa (CYMMKAA) </p> </td> 
 </tr> 
</table>

I valori dei componenti decimali per i colori RGB sono compresi tra 0 e 255. I valori dei componenti decimali per CMYK e grigio sono compresi tra 0,100% e Tutti i valori dei componenti esadecimali sono compresi nell’intervallo 0...0xFF.

I valori dei componenti colore sono considerati indipendenti dal valore alfa (non premoltiplicato).

Tutti i valori di colore, i prefissi e i suffissi non fanno distinzione tra maiuscole e minuscole.

Il suffisso &quot;k&quot; del tipo è richiesto per i valori di colore CMYK. È possibile specificare un suffisso di tipo per i valori di colore RGB e grigio.

Il prefisso &#39;0x&#39; è richiesto per i valori di colore grigio esadecimale.

Il suffisso &#39;s&#39; specifica che il valore del colore è associato allo spazio colore di input (sorgente) corrispondente al tipo di pixel del valore del colore (definito con `attribute::IccProfileSrc*`). Se questo suffisso non è presente, il valore del colore è associato allo spazio colore di output (destinazione) (definito con `icc=` o `attribute::IccProfile*`).

## Predefinito {#section-737082a7da544acca8092a48d88480e7}

Se il valore alfa non viene specificato in modo esplicito, si presume che sia 255, 0xFF o 100% (completamente opaco).

## Esempi {#section-4ac69026349949f8b595a6d4a9ce474d}

Alcuni esempi di specifici di colore validi e il tipo di pixel, il valore del colore, il valore alfa e lo spazio colore predefinito corrispondenti:

<table id="table_1539E74A1EC545F1B5398D86A27079D1"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> <i>color</i> </b> </th> 
   <th class="entry"> <b>Tipo di pixel</b> </th> 
   <th class="entry"> <b>Valore colore</b> </th> 
   <th class="entry"> <b>Valore alfa</b> </th> 
   <th class="entry"> <b>Spazio colore predefinito  </b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p>0.100.200 </p> </td> 
   <td> <p>RGB </p> </td> 
   <td> <p>0.100.200 </p> </td> 
   <td> <p>255 </p> </td> 
   <td> <p> <span class="codeph"> IccProfileRgb</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>0.100.200.200 ore </p> </td> 
   <td> <p>RGB </p> </td> 
   <td> <p>0.100.200 </p> </td> 
   <td> <p>200 </p> </td> 
   <td> <p> <span class="codeph"> IccProfileSrcRgb</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>0x010203S </p> </td> 
   <td> <p>RGB </p> </td> 
   <td> <p>1,2,3 </p> </td> 
   <td> <p>255 </p> </td> 
   <td> <p> <span class="codeph"> IccProfileSrcRgb</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>a0b1c2d3R </p> </td> 
   <td> <p>RGB </p> </td> 
   <td> <p>160.177.194 </p> </td> 
   <td> <p>211 </p> </td> 
   <td> <p> <span class="codeph"> IccProfileRgb</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>100 S </p> </td> 
   <td> <p>grigio </p> </td> 
   <td> <p>100% </p> </td> 
   <td> <p>100% </p> </td> 
   <td> <p> <span class="codeph"> IccProfileSrcGray</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>50,75 g </p> </td> 
   <td> <p>grigio </p> </td> 
   <td> <p>50% </p> </td> 
   <td> <p>75% </p> </td> 
   <td> <p> <span class="codeph"> IccProfileGray</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>0X70G </p> </td> 
   <td> <p>grigio </p> </td> 
   <td> <p>44% </p> </td> 
   <td> <p>44% </p> </td> 
   <td> <p> <span class="codeph"> IccProfileGray</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>0xddeegs </p> </td> 
   <td> <p>grigio </p> </td> 
   <td> <p>87% </p> </td> 
   <td> <p>93% </p> </td> 
   <td> <p> <span class="codeph"> IccProfileSrcGray  </span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>94,11,50,33 k </p> </td> 
   <td> <p>CMYK </p> </td> 
   <td> <p>94-11-50-33% </p> </td> 
   <td> <p>100% </p> </td> 
   <td> <p> <span class="codeph"> IccProfileCmyk</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>22,23,24,25,26 KS </p> </td> 
   <td> <p>CMYK </p> </td> 
   <td> <p>22-23-24-25% </p> </td> 
   <td> <p>26% </p> </td> 
   <td> <p> <span class="codeph"> IccProfileSrcCmyk</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>38393A3bK </p> </td> 
   <td> <p>CMYK </p> </td> 
   <td> <p>56-57-58-59% </p> </td> 
   <td> <p>100% </p> </td> 
   <td> <p> <span class="codeph"> IccProfileCmyk</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>0x0a0b0C0d0eks </p> </td> 
   <td> <p>CMYK </p> </td> 
   <td> <p>10-11-12-13% </p> </td> 
   <td> <p>14% </p> </td> 
   <td> <p> <span class="codeph"> IccProfileSrcCmyk</span> </p> </td> 
  </tr> 
 </tbody> 
</table>

Lo spazio colore di output specificato con `icc=` si applica invece dello spazio colore predefinito quando il tipo di pixel di un colore di output corrisponde al tipo di pixel dell&#39;immagine di output.
