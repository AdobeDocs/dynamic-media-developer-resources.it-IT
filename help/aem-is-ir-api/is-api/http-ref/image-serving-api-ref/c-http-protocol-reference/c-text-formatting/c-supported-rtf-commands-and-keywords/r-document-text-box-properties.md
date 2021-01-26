---
description: Le seguenti proprietà del documento sono supportate nelle caselle di testo.
seo-description: Le seguenti proprietà del documento sono supportate nelle caselle di testo.
seo-title: Proprietà documento (casella di testo)
solution: Experience Manager
title: Proprietà documento (casella di testo)
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 743a773a-83b0-4667-9c67-4cefbfe77bbd
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '222'
ht-degree: 1%

---


# Proprietà documento (casella di testo){#document-text-box-properties}

Le seguenti proprietà del documento sono supportate nelle caselle di testo.

<table id="table_8E1DF8E6BD894D7A9ACFC839918E2315"> 
 <thead> 
  <tr> 
   <th class="entry"> <b>Comando</b> </th> 
   <th class="entry"> <b>Descrizione</b> </th> 
   <th class="entry"> <b>Note</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <span class="codeph"> \fonttbl  </span> </td> 
   <td> <p>Tabella dei font. </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \fcharset  <span class="varname"> N  </span> </span> </td> 
   <td> <p>Set di caratteri per il font <i>N</i>. </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \colortbl  </span> </td> 
   <td> <p>Tavola colori RGB. </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \cmykcolortbl  </span> </td> 
   <td> <p>Tavola colori CMYK. </p> </td> 
   <td> <p>Estensione Dynamic Media. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \*\iscolortbl  </span> </td> 
   <td> <p>Tavola dei colori per Image Serving Colour (Serving immagini). </p> </td> 
   <td> <p>estensione Dynamic Media; Solo <span class="codeph"> textPs= </span> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \red  <span class="varname"> N  </span> </span> </td> 
   <td> <p>Componente colore rosso. </p> </td> 
   <td> <p>Può essere visualizzato solo in <span class="codeph"> \colortbl </span>; 0...255 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \green  <span class="varname"> N  </span> </span> </td> 
   <td> <p>Componente colore verde. </p> </td> 
   <td> <p>Può essere visualizzato solo in <span class="codeph"> \colortbl </span>; 0...255 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \blue  <span class="varname"> N  </span> </span> </td> 
   <td> <p>Componente colore blu. </p> </td> 
   <td> <p>Può essere visualizzato solo in <span class="codeph"> \colortbl </span>; 0...255 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \cyan  <span class="varname"> N  </span> </span> </td> 
   <td> <p>Componente colore ciano. </p> </td> 
   <td> <p>estensione Dynamic Media; può essere visualizzato solo in <span class="codeph"> \cmykcolortbl </span>; 0...100 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \magenta  <span class="varname"> N  </span> </span> </td> 
   <td> <p>Componente colore magenta. </p> </td> 
   <td> <p>estensione Dynamic Media; può essere visualizzato solo in <span class="codeph"> \cmykcolortbl </span>; 0...100 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \yellow  <span class="varname"> N  </span> </span> </td> 
   <td> <p>Componente colore giallo. </p> </td> 
   <td> <p>estensione Dynamic Media; può essere visualizzato solo in <span class="codeph"> \cmykcolortbl </span>; 0...100 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \black  <span class="varname"> N  </span> </span> </td> 
   <td> <p>Componente colore nero. </p> </td> 
   <td> <p>estensione Dynamic Media; può essere visualizzato solo in <span class="codeph"> \cmykcolortbl </span>; 0...100 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \margl  <span class="varname"> N  </span> </span> </td> 
   <td> <p>Margine sinistro. </p> </td> 
   <td> <p>Twip; Solo <span class="codeph"> textPs= </span> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \margr  <span class="varname"> N  </span> </span> </td> 
   <td> <p>Margine destro. </p> </td> 
   <td> <p>Twip; Solo <span class="codeph"> textPs= </span> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \margt  <span class="varname"> N  </span> </span> </td> 
   <td> <p>Margine superiore. </p> </td> 
   <td> <p>Twip; Solo <span class="codeph"> textPs= </span> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \margb  <span class="varname"> N  </span> </span> </td> 
   <td> <p>Margine inferiore. </p> </td> 
   <td> <p>Twip; Solo <span class="codeph"> textPs= </span> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \vertalt  </span> </td> 
   <td> <p>Allinea in alto il testo nella casella di testo. </p> </td> 
   <td> <p>Predefinito </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \vertalb  </span> </td> 
   <td> <p>Allinea in basso il testo nella casella di testo. </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \vertalc  </span> </td> 
   <td> <p>Centra il testo nella casella di testo. </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \stextflow  <span class="varname"> N  </span> </span> </td> 
   <td> <p>Orientamento del flusso di testo. </p> </td> 
   <td> <p>Flusso di testo specifico per la lingua; <span class="codeph"> textPs= </span> solo 0 (predefinito) sinistro, superiore inferiore (europeo) 1 superiore inferiore, destro (Far Eastern) </p> </td> 
  </tr> 
 </tbody> 
</table>

