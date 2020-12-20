---
description: Il catalogo di sessione è il catalogo di materiali che fornisce gli attributi di sessione per la richiesta, nonché un valore catId predefinito per tutti i comandi src=, vignette= e icc=.
seo-description: Il catalogo di sessione è il catalogo di materiali che fornisce gli attributi di sessione per la richiesta, nonché un valore catId predefinito per tutti i comandi src=, vignette= e icc=.
seo-title: Catalogo delle sessioni
solution: Experience Manager
title: Catalogo delle sessioni
topic: Scene7 Image Serving - Image Rendering API
uuid: 69c0f6cd-dfaf-47bf-bdd9-7abb4e6f7465
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '270'
ht-degree: 0%

---


# Catalogo delle sessioni{#session-catalog}

Il catalogo di sessione è il catalogo di materiali che fornisce gli attributi di sessione per la richiesta, nonché un valore catId predefinito per tutti i comandi src=, vignette= e icc=.

Il catalogo delle sessioni è specificato come primo elemento del percorso del percorso di richiesta HTTP (subito dopo il nome del server). Se il primo elemento del percorso non corrisponde ad attribute::RootId di alcun catalogo, il catalogo predefinito viene utilizzato come catalogo di sessioni.

Il catalogo delle sessioni contiene i seguenti valori predefiniti di sessione:

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
   <td> <p> Percorso principale per i file di dati dei materiali </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> attributo::VignettePath</span> </p> </td> 
   <td> <p> Percorso radice per i file di vignettatura </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> attributo::IccProfileRgb</span> </p> </td> 
   <td> <p> Spazio colore di lavoro predefinito se una vignettatura non incorpora un profilo ICC </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> attributo::RootUrl</span> </p> </td> 
   <td> <p> URL principale per percorsi di file HTTP relativi nei comandi <span class="codeph"> src=</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> attribute::ShowOverlapObjs</span> </p> </td> 
   <td> <p> Stato iniziale di visualizzazione/nascondi per gli oggetti sovrapposti </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> attributo::Scadenza</span> </p> </td> 
   <td> <p> Valore temporale del flusso di lavoro dell'immagine di risposta per le cache del server proxy e del browser </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> attributo::MaxPix</span> </p> </td> 
   <td> <p> Larghezza e altezza massime consentite per l’immagine di risposta </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> attribute::DefaultPix</span> </p> </td> 
   <td> <p> Valori predefiniti per <span class="codeph"> wid=</span> e <span class="codeph"> hei=</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> attribute:Format</span> </p> </td> 
   <td> <p> Valore predefinito per <span class="codeph"> fmt=</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> attribute::JpegQuality</span> </p> </td> 
   <td> <p> Valore predefinito per <span class="codeph"> qlt=</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> attribute::TiffEncoding</span> </p> </td> 
   <td> <p> Tipo di compressione per l'output di immagini TIFF </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> attributo::Nitidezza</span> </p> </td> 
   <td> <p> Valore predefinito per <span class="codeph"> sharpen=</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> attributo::OnFailSel</span> </p> </td> 
   <td> <p> Specifica il comportamento quando un comando <span class="codeph"> sel=</span> ha esito negativo </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> attributo::OnFailObj</span> </p> </td> 
   <td> <p> Specifica il comportamento quando un comando <span class="codeph"> obj=</span> ha esito negativo </p> </td> 
  </tr> 
 </tbody> 
</table>

