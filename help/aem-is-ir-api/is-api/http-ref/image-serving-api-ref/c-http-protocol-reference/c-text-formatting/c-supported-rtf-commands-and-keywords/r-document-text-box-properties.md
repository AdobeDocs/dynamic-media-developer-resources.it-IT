---
description: Le seguenti proprietà del documento sono supportate nelle caselle di testo.
solution: Experience Manager
title: Proprietà documento (casella di testo)
feature: Dynamic Media Classic, SDK/API
role: Developer,User
exl-id: e9d21a39-4d98-4115-8179-ab5acf713c80
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '214'
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
   <td> <p>Tabella dei caratteri. </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \fcharset  <span class="varname"> N  </span> </span> </td> 
   <td> <p>Set di caratteri per il carattere <i>N</i>. </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \colortbl  </span> </td> 
   <td> <p>Tavola colori RGB. </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \cmykcolortbl  </span> </td> 
   <td> <p>Tabella colori CMYK. </p> </td> 
   <td> <p>Estensione Dynamic Media. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \*\iscolortbl  </span> </td> 
   <td> <p>Tavola colori per i colori Image Serving. </p> </td> 
   <td> <p>estensione Dynamic Media; Solo <span class="codeph"> textPs= </span> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \red  <span class="varname"> N  </span> </span> </td> 
   <td> <p>Componente colore rosso. </p> </td> 
   <td> <p>Può essere visualizzato solo in <span class="codeph"> \colortbl </span>; 0...255 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \verde  <span class="varname"> N  </span> </span> </td> 
   <td> <p>Componente colore verde. </p> </td> 
   <td> <p>Può essere visualizzato solo in <span class="codeph"> \colortbl </span>; 0...255 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \blu  <span class="varname"> N  </span> </span> </td> 
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
   <td> <span class="codeph"> \giallo  <span class="varname"> N  </span> </span> </td> 
   <td> <p>Componente colore giallo. </p> </td> 
   <td> <p>estensione Dynamic Media; può essere visualizzato solo in <span class="codeph"> \cmykcolortbl </span>; 0...100 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \nero  <span class="varname"> N  </span> </span> </td> 
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
   <td> <p>Testo allineato in alto nella casella di testo. </p> </td> 
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
   <td> <p>Flusso di testo specifico per la lingua; <span class="codeph"> textPs= </span> solo 0 (predefinito) sinistro-destro, superiore-inferiore (europeo) 1 superiore-inferiore, destro-sinistro (Far Eastern) </p> </td> 
  </tr> 
 </tbody> 
</table>
