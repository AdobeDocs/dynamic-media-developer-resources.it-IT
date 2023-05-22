---
title: Catalogo sessione
description: Il catalogo delle sessioni è il catalogo dei materiali che fornisce gli attributi di sessione per la richiesta e un valore catId predefinito per tutti i comandi src=, vignette= e icc=.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 36e0571e-7451-423f-a1df-540680381902
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '233'
ht-degree: 0%

---

# Catalogo sessione{#session-catalog}

Il catalogo delle sessioni è il catalogo dei materiali che fornisce gli attributi di sessione per la richiesta e un valore catId predefinito per tutti `src=`, `vignette=`, e `icc=` comandi.

Il catalogo di sessione viene specificato come primo elemento percorso del percorso della richiesta HTTP (immediatamente successivo al nome del server). Se il primo elemento percorso non corrisponde all&#39;attributo::RootId di alcun catalogo, il catalogo predefinito viene utilizzato come catalogo di sessione.

Il catalogo di sessione fornisce i seguenti valori predefiniti di sessione:

<table id="table_DB5E0DD8E9B440A4964A1326433597C8"> 
 <thead> 
  <tr> 
   <th class="entry"> <p>Attributo </p> </th> 
   <th class="entry"> <p>Note </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> attribute::RootPath</span> </p> </td> 
   <td> <p> Percorso principale per i file di dati dei materiali </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> attribute::VignettePath</span> </p> </td> 
   <td> <p> Percorso directory principale per i file di vignettatura </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> attribute::IccProfileRgb</span> </p> </td> 
   <td> <p> Spazio colore di lavoro predefinito se una vignettatura non incorpora un profilo ICC </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> attribute::RootUrl</span> </p> </td> 
   <td> <p> URL principale per i percorsi relativi dei file HTTP in <span class="codeph"> src=</span> comandi </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> attribute::ShowOverlapObjs</span> </p> </td> 
   <td> <p> Stato iniziale per mostrare/nascondere gli oggetti sovrapposti </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> attribute::Scadenza</span> </p> </td> 
   <td> <p> Valore time-to-live dell'immagine di risposta per il server proxy e le cache del browser </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> attribute::MaxPix</span> </p> </td> 
   <td> <p> Larghezza e altezza massime consentite per l’immagine di risposta </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> attribute::DefaultPix</span> </p> </td> 
   <td> <p> Valori predefiniti per <span class="codeph"> wid=</span> e <span class="codeph"> hei=</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> attribute::Format</span> </p> </td> 
   <td> <p> Valore predefinito per <span class="codeph"> fmt=</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> attributo::JpegQuality</span> </p> </td> 
   <td> <p> Valore predefinito per <span class="codeph"> qlt=</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> attribute::CodificaTiff</span> </p> </td> 
   <td> <p> Tipo di compressione per l’output dell’immagine del TIFF </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> attributo::Nitidezza</span> </p> </td> 
   <td> <p> Valore predefinito per <span class="codeph"> sharpen= nitidezza</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> attribute::OnFailSel</span> </p> </td> 
   <td> <p> Specifica il comportamento quando un <span class="codeph"> sel=</span> comando non riuscito </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> attribute::OnFailObj</span> </p> </td> 
   <td> <p> Specifica il comportamento quando un <span class="codeph"> obj=</span> comando non riuscito </p> </td> 
  </tr> 
 </tbody> 
</table>
