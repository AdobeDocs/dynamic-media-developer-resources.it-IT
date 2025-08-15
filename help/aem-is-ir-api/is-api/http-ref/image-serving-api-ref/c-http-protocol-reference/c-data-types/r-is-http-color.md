---
description: Valori colore. Puoi specificare i valori dei colori utilizzando la notazione esadecimale, un elenco separato da virgole di valori dei componenti o i decimali.
solution: Experience Manager
title: colore
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: eba88ff0-877d-432e-bbd6-9172f5b460e9
source-git-commit: 2ff380ad30911a85bc066ae53f0cb69360ed99e4
workflow-type: tm+mt
source-wordcount: '452'
ht-degree: 2%

---

# colore{#color}

Valori colore. Puoi specificare i valori dei colori utilizzando la notazione esadecimale, un elenco separato da virgole di valori dei componenti o i decimali.

<table id="simpletable_9EBE66066E854ABE978F8F7ADC66BDE3"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> colore</span> </span> </p></td> 
  <td class="stentry"> <p> <span class="codeph">&lcub;&lcub;<span class="varname"> grigio</span>[,<span class="varname"> alfa</span>][g]&rcub;|</span> </p> <p> <span class="codeph"> {<span class="varname"> rosso</span>,<span class="varname"> verde</span>,<span class="varname"> blu</span>[ ,<span class="varname"> rgbAlpha</span>][r]}|</span> </p> <p> <span class="codeph"> {<span class="varname"> ciano</span>, <span class="varname"> magenta</span>, <span class="varname"> giallo</span>, <span class="varname"> nero</span>[,alfa]k}|</span> </p> <p> <span class="codeph"> {0x{hex2|hex4}[g]}|</span> </p> <p> <span class="codeph">{[0x]{<span class="varname"> hex6</span>|<span class="varname"> hex8</span>}[r]}|</span> </p> <p> <span class="codeph"> {[0x]{<span class="varname"> hex8</span>|<span class="varname"> hex10</span>}k}&rcub;[s]</span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> rosso</span>, <span class="varname"> verde</span>, <span class="varname"> blu</span>, <span class="varname"> rgbAlpha</span></span> </p> </td> 
  <td class="stentry"> <p>valore componente colore (0...255, int decimale) </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> ciano</span>, <span class="varname"> magenta</span>, <span class="varname"> giallo</span>, <span class="varname"> nero</span>, <span class="varname"> alfa</span></span> </p></td> 
  <td class="stentry"> <p>Valore del componente colore CMYK (0,100 %, int decimale) </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> grigio</span>, <span class="varname"> alfa</span></span> </p> </td> 
  <td class="stentry"> <p>Valore componente colore grigio (0... 100%, decimale int) </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> esadecimale2</span> </span> </p></td> 
  <td class="stentry"> <p>Valore di colore grigio esadecimale (GG) a due cifre imballato </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> esadecimale4</span> </span> </p> </td> 
  <td class="stentry"> <p>colore grigio esadecimale a quattro cifre con valore di colore alfa (GGAA) </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> hex6</span> </span> </p> </td> 
  <td class="stentry"> <p>valore colore RGB esadecimale a sei cifre imballato (RRGGBB) </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> hex8</span> </span> </p> </td> 
  <td class="stentry"> <p>valore colore RGBA (RRGGBBAA) o CMYK (CCMMYYKK) esadecimale a otto cifre imballato (se specificato con il suffisso "k") </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> hex10</span> </span> </p></td> 
  <td class="stentry"> <p>CMYK esadecimale a dieci cifre imballato con valore alfa (CCYYMMKKAA) </p> </td> 
 </tr> 
</table>

I valori dei componenti decimali per i colori RGB sono compresi nell&#39;intervallo 0...255. I valori dei componenti decimali per CMYK e grigio sono compresi nell&#39;intervallo 0..100%. Tutti i valori esadecimali dei componenti sono compresi nell&#39;intervallo 0...0xFF.

Si presume che i valori dei componenti colore siano indipendenti dal valore alfa (non premoltiplicati).

Per tutti i valori di colore, i prefissi e i suffissi non viene fatta distinzione tra maiuscole e minuscole.

Il suffisso di tipo &#39;k&#39; è obbligatorio per i valori di colore CMYK. Facoltativamente è possibile specificare un suffisso di tipo per i valori di colore RGB e grigio.

Il prefisso &#39;0x&#39; è obbligatorio per i valori esadecimali dei colori grigi.

Il suffisso &#39;s&#39; specifica che il valore del colore è associato allo spazio colore di input (sorgente) corrispondente al tipo di pixel del valore del colore (definito con `attribute::IccProfileSrc*`). Se questo suffisso non è presente, il valore del colore è associato allo spazio colore di output (destinazione) definito con `icc=` o `attribute::IccProfile*`.

## Predefinito {#section-737082a7da544acca8092a48d88480e7}

Se un valore alfa non è specificato in modo esplicito, si presume che sia 255, 0xFF o 100% (completamente opaco).

## Esempi {#section-4ac69026349949f8b595a6d4a9ce474d}

Alcuni esempi di specificatori di colore validi e il tipo di pixel, il valore di colore, il valore alfa e lo spazio colore predefinito corrispondenti:

<table id="table_1539E74A1EC545F1B5398D86A27079D1"> 
 <thead> 
  <tr> 
   <th class="entry"> <b><i>Colore</i> </b> </th> 
   <th class="entry"> <b>Tipo di pixel</b> </th> 
   <th class="entry"> <b>Colore Valore</b> </th> 
   <th class="entry"> <b>Valore Alpha</b> </th> 
   <th class="entry"> <b>Spazio colore predefinito </b> </th> 
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
   <td> <p>0,100,200,200 rs </p> </td> 
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
   <td> <p>0X70 G </p> </td> 
   <td> <p>grigio </p> </td> 
   <td> <p>44% </p> </td> 
   <td> <p>44% </p> </td> 
   <td> <p> <span class="codeph"> Grigio profilo ICC</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>0xddeegs </p> </td> 
   <td> <p>grigio </p> </td> 
   <td> <p>87% </p> </td> 
   <td> <p>93% </p> </td> 
   <td> <p> <span class="codeph"> IccProfileSrcGray </span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>94,11,50,33 k </p> </td> 
   <td> <p>CMYK </p> </td> 
   <td> <p>94-11-50-33% </p> </td> 
   <td> <p>100% </p> </td> 
   <td> <p> <span class="codeph"> IccProfileCmyk</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>22,23,24,25,26 K </p> </td> 
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

Lo spazio colore di output specificato con `icc=` viene applicato al posto dello spazio colore predefinito quando il tipo di pixel di un colore di output corrisponde al tipo di pixel dell&#39;immagine di output.
