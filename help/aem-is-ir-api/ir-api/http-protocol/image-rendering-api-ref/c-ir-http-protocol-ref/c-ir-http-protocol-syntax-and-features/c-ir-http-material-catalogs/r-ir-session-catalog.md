---
description: Il catalogo di sessione è il catalogo dei materiali che fornisce gli attributi di sessione per la richiesta, nonché un valore catId predefinito per tutti i comandi src=, vignette= e icc=.
solution: Experience Manager
title: Catalogo delle sessioni
feature: Dynamic Media Classic, SDK/API
role: Sviluppatore, Business Practices
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '248'
ht-degree: 0%

---


# Catalogo sessione{#session-catalog}

Il catalogo di sessione è il catalogo dei materiali che fornisce gli attributi di sessione per la richiesta, nonché un valore catId predefinito per tutti i comandi src=, vignette= e icc=.

Il catalogo di sessione è specificato come primo elemento del percorso della richiesta HTTP (subito dopo il nome del server). Se il primo elemento del percorso non corrisponde all’attributo::RootId di qualsiasi catalogo, il catalogo predefinito viene utilizzato come catalogo di sessione.

Il catalogo delle sessioni fornisce i seguenti valori predefiniti di sessione:

<table id="table_DB5E0DD8E9B440A4964A1326433597C8"> 
 <thead> 
  <tr> 
   <th class="entry"> <p>Attributo </p> </th> 
   <th class="entry"> <p>Note </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> attributo::RootPath</span> </p> </td> 
   <td> <p> Percorso principale per i file di dati di materiale </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> attributo::VignettePath</span> </p> </td> 
   <td> <p> Percorso principale per i file vignetta </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> attributo::IccProfileRgb</span> </p> </td> 
   <td> <p> Spazio colore di lavoro predefinito se una vignetta non incorpora un profilo ICC </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> attributo::RootUrl</span> </p> </td> 
   <td> <p> URL principale per percorsi di file HTTP relativi nei comandi <span class="codeph"> src=</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> attributo::ShowOverlapObjs</span> </p> </td> 
   <td> <p> Stato iniziale di visualizzazione/nascondi per gli oggetti sovrapposti </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> attributo::Scadenza</span> </p> </td> 
   <td> <p> Valore "time-to-live" dell'immagine di risposta per le cache del server proxy e del browser </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> attributo::MaxPix</span> </p> </td> 
   <td> <p> Larghezza e altezza massima dell'immagine di risposta consentita </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> attributo::DefaultPix</span> </p> </td> 
   <td> <p> Valori predefiniti per <span class="codeph"> wid=</span> e <span class="codeph"> hei=</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> attributo::Format</span> </p> </td> 
   <td> <p> Valore predefinito per <span class="codeph"> fmt=</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> attributo::JpegQuality</span> </p> </td> 
   <td> <p> Valore predefinito per <span class="codeph"> qlt=</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> attributo::TiffEncoding</span> </p> </td> 
   <td> <p> Tipo di compressione per l'uscita immagine TIFF </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> attributo::Sharpen</span> </p> </td> 
   <td> <p> Valore predefinito per <span class="codeph"> sharpen=</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> attributo::OnFailSel</span> </p> </td> 
   <td> <p> Specifica il comportamento quando un comando <span class="codeph"> sel=</span> non riesce </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> attributo::OnFailObj</span> </p> </td> 
   <td> <p> Specifica il comportamento quando un comando <span class="codeph"> obj=</span> non riesce </p> </td> 
  </tr> 
 </tbody> 
</table>

