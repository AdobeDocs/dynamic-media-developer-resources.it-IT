---
title: Catalogo sessione
description: Il catalogo delle sessioni è il catalogo dei materiali che fornisce gli attributi di sessione per la richiesta e un valore catId predefinito per tutti i comandi src=, vignette= e icc=.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 36e0571e-7451-423f-a1df-540680381902
TQID: 'https://experienceleague.adobe.com/--3F69i8XdliFxf5IhMPbUThRzMNyIDjtW4-Y-SBCFE'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 235
ht-degree: 0%

---

# Catalogo sessione{#session-catalog}

Il catalogo delle sessioni è il catalogo dei materiali che fornisce gli attributi di sessione per la richiesta e un valore catId predefinito per tutti i comandi `src=`, `vignette=` e `icc=`.

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
   <td> <p> Attributo <span class="codeph">::RootPath</span> </p> </td> 
   <td> <p> Percorso principale per i file di dati dei materiali </p> </td> 
  </tr> 
  <tr> 
   <td> <p> Attributo <span class="codeph">::VignettePath</span> </p> </td> 
   <td> <p> Percorso directory principale per i file di vignettatura </p> </td> 
  </tr> 
  <tr> 
   <td> <p> Attributo <span class="codeph">::IccProfileRgb</span> </p> </td> 
   <td> <p> Spazio colore di lavoro predefinito se una vignettatura non incorpora un profilo ICC </p> </td> 
  </tr> 
  <tr> 
   <td> <p> Attributo <span class="codeph">::RootUrl</span> </p> </td> 
   <td> <p> URL principale per i percorsi relativi dei file HTTP nei comandi <span class="codeph"> src=</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> Attributo <span class="codeph">::ShowOverlapObjs</span> </p> </td> 
   <td> <p> Stato iniziale per mostrare/nascondere gli oggetti sovrapposti </p> </td> 
  </tr> 
  <tr> 
   <td> <p> Attributo <span class="codeph">::Scadenza</span> </p> </td> 
   <td> <p> Valore time-to-live dell'immagine di risposta per il server proxy e le cache del browser </p> </td> 
  </tr> 
  <tr> 
   <td> <p> Attributo <span class="codeph">::MaxPix</span> </p> </td> 
   <td> <p> Larghezza e altezza massime consentite per l’immagine di risposta </p> </td> 
  </tr> 
  <tr> 
   <td> <p> Attributo <span class="codeph">::DefaultPix</span> </p> </td> 
   <td> <p> Valori predefiniti per <span class="codeph"> wid=</span> e <span class="codeph"> hei=</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> Attributo <span class="codeph">::Format</span> </p> </td> 
   <td> <p> Valore predefinito per <span class="codeph"> fmt=</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> Attributo <span class="codeph">::JpegQuality</span> </p> </td> 
   <td> <p> Valore predefinito per <span class="codeph"> qlt=</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> Attributo <span class="codeph">::TiffEncoding</span> </p> </td> 
   <td> <p> Tipo di compressione per l'output dell'immagine TIFF </p> </td> 
  </tr> 
  <tr> 
   <td> <p> Attributo <span class="codeph">::Sharpen</span> </p> </td> 
   <td> <p> Valore predefinito per la nitidezza <span class="codeph">=</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> Attributo <span class="codeph">::OnFailSel</span> </p> </td> 
   <td> <p> Specifica il comportamento quando un comando <span class="codeph"> sel=</span> non riesce </p> </td> 
  </tr> 
  <tr> 
   <td> <p> Attributo <span class="codeph">::OnFailObj</span> </p> </td> 
   <td> <p> Specifica il comportamento quando un comando <span class="codeph"> obj=</span> ha esito negativo </p> </td> 
  </tr> 
 </tbody> 
</table>
