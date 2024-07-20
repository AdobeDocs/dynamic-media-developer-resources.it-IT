---
description: vntc genera dati di testo che vengono inviati a stderr o al file di log.
solution: Experience Manager
title: Output
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 48b15fc2-19c2-4ff8-8059-ba3478a4eec2
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '695'
ht-degree: 0%

---

# Output{#output}

vntc genera dati di testo che vengono inviati a stderr o al file di log.

I dati vengono formattati come una proprietà `name=value` per record di testo. I valori stringa non sono tra virgolette. I messaggi di avviso e di errore vengono sempre inviati a `stderr`, anche se è specificato `-log`.

Alcune proprietà possono verificarsi più volte nello stesso output. Al nome di queste proprietà viene aggiunto un numero di sequenza che inizia con 0, separato da un punto. Tali proprietà sono identificate di seguito con un suffisso `. *`n`*` dopo il nome della proprietà.

Vengono generate le seguenti proprietà:

<table id="simpletable_32AAA1A2DDB04BC6B86885E6223BF609"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">bgc=<span class="varname"> ival</span>,<span class="varname"> ival</span>,<span class="varname"> ival</span></span> </p> </td> 
  <td class="stentry"> <p>Colore di sfondo RGB dello stile dell'archivio. Solo stili di scaffale. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">defaultFileVersion=<span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p>Versione predefinita del file di output. Inoltre, il numero di versione più alto che questa versione di <span class="filepath"> vntc</span> può generare. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> errore.<span class="varname"> n</span>=<span class="varname"> stringa</span></span> </p></td> 
  <td class="stentry"> <p>Messaggio di errore La presenza di messaggi di errore indica in genere che non vengono creati file di output o che non sono adatti per il rendering immagini. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> file.<span class="varname"> n</span>=<span class="varname"> stringa</span></span> </p></td> 
  <td class="stentry"> <p>Percorso/nome completo di tutti i file di output, inclusi vignettature, file di stile archivio, immagini a risoluzione completa e miniature. È presente un attributo di file per ciascun file generato (eccetto il file di registro). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">vetro=<span class="varname"> flaconcino</span></span> </p></td> 
  <td class="stentry"> <p><span class="varname"> ival</span> è 1 se il cabinet include porte di vetro, 0 in caso contrario. Solo stili di scaffale. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">iccProfile=<span class="varname"> stringa</span></span> </p></td> 
  <td class="stentry"> <p>Il nome del iccProfile incorporato nel file di origine <span class="varname"></span>. </p> <p>Vuoto se <span class="varname"> sourceFile</span> non è gestito tramite colore. Solo per le vignette. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">informazioni.<span class="varname"> n</span>=<span class="varname"> stringa</span></span> </p></td> 
  <td class="stentry"> <p>Messaggio informativo, ad esempio informazioni sull’avanzamento. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">sourceIsMaster=<span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p><span class="varname"> ival</span> è 1 se <span class="varname"> sourceFile</span> è una vignettatura principale, 0 se è stata elaborata in precedenza con <span class="filepath"> vnUpdate</span> o <span class="filepath"> vntc</span>. Solo per le vignette. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">master=<span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p><span class="varname"> ival</span> è 0 se <span class="varname"> sourceFile</span> è uno stile di archivio contenente i dati dell'immagine JPEG (in questo caso viene generato anche un avviso), in caso contrario 1. Archivio e finestra che coprono solo i file di stile. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">maxMem=<span class="varname"> stringa</span></span> </p></td> 
  <td class="stentry"> <p>Limite massimo di memoria applicabile al processo <span class="filepath"> vntc</span> in esecuzione. <span class="varname"> stringa</span> è <span class="varname"> ival</span>, <span class="varname"> ivalK</span>, <span class="varname"> ivalM</span>, <span class="varname"> ivalG</span> o <span class="codeph"> 0</span> (disabilitato). Dove <span class="varname"> K</span>, <span class="varname"> M</span> e <span class="varname"> G</span> fanno riferimento a Kilobyte (1024 byte), Megabyte (1048576 byte) e Gigabyte (1073741824 byte). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">maxScl=<span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p>Scala del livello piramidale a risoluzione più bassa nella vignettatura di output. Presente solo se è specificato <span class="codeph"> -pyramid</span>. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">numMaterials=<span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p>Numero di materiali salvati nel file di origine <span class="varname"></span>. Solo per le vignette. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">numPanels=<span class="codeph"> ival</span></span> </p></td> 
  <td class="stentry"> <p>Il numero di immagini del pannello in questo file di stile archivio. Solo stili di scaffale. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">numViews=<span class="codeph"> ival</span></span> </p></td> 
  <td class="stentry"> <p>Il numero di livelli piramidali nella vignettatura di output. Presente solo se si specifica -pyramid. Solo per le vignette. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">piramide=<span class="varname"> flaconcino</span></span> </p></td> 
  <td class="stentry"> <p>0 se la vignettatura di origine o di destinazione ha una struttura piramidale. Solo per le vignette. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">risoluzione=<span class="varname"> valore</span></span> </p></td> 
  <td class="stentry"> <p>Per gli stili di archivio, la risoluzione dell'oggetto dell'elemento sourceFile</span> <span class="varname">. Per le vignettature, questa è la risoluzione del materiale consigliata per ottenere risultati di rendering di qualità migliore durante il rendering della vignettatura di output. Pixel/pollici (ppi). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">resolution.min=<span class="varname"> val</span></span> </p></td> 
  <td class="stentry"> <p>La risoluzione dell'oggetto più piccola nella vignettatura di output. Solo per le vignette. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">resolution.avg=<span class="varname"> val</span></span> </p></td> 
  <td class="stentry"> <p>Risoluzione media dell'oggetto nella vignettatura di output. Solo per le vignette. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">sourceFile=<span class="varname"> stringa</span></span> </p></td> 
  <td class="stentry"> <p>Percorso completo di <span class="varname"> sourceFile</span>. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">sourceFileVersion=<span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p>Versione del file di <span class="varname"> sourceFile</span>. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">sourceSize=<span class="varname"> ival</span>,<span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p>La dimensione in pixel della vignettatura di input, l'immagine predefinita del pannello in un file di stile archivio o la prima immagine di opacità di una finestra che copre un file di stile. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">stile=<span class="varname"> stringa</span></span> </p></td> 
  <td class="stentry"> <p>Tipo di copertina della finestra (solo per gli stili): </p> <p> 
    <ul id="ul_51AECE556B8B40109FFAD2B315D0695C"> 
     <li id="li_3D3B9211C7AF4810883AE815BEBD4228">0=ombreggiatura orizzontale o persiane </li> 
     <li id="li_DE88052467D64ECDAEB29264FC3904E4">1=tende verticali </li> 
     <li id="li_6F976CABF7244B20A471391A685ED05F"> 2=tende corte a larghezza intera </li> 
     <li id="li_E8D2B0B9189F4BDBB70E145E9196C1CD">3=drappi brevi sinistra/destra </li> 
     <li id="li_026F043A50D34C8AB850D9832F375DB7"> 4=tende a lunghezza intera larghezza intera </li> 
     <li id="li_283A2E5BFF75461B8F697FFF0796361F"> 5=drappi a tutta lunghezza sinistra/destra </li> 
     <li id="li_E175BA9EAE1F46B89109F4892FF54656"> 6=tenda del caffè </li> 
     <li id="li_79D2F7F68C4746F3B6742EFECD01BDD9"> 7=valore </li> 
    </ul> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">suffisso=<span class="varname"> stringa</span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> vnt</span> se <span class="varname"> sourceFile</span> è una vignettatura, <span class="codeph"> vnc</span> se <span class="varname"> sourceFile</span> è uno stile di archivio o <span class="codeph"> vnw</span> se <span class="varname"> sourceFile</span> è una finestra che copre lo stile. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">targetFileVersion=<span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p>Il valore specificato con <span class="codeph"> -version</span> o il valore di <span class="codeph"> defaultFileVersion</span> se<span class="codeph"> -version</span> non è stato specificato. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">targetSizes=<span class="varname"> ival</span>,<span class="varname"> ival</span>*[,<span class="varname"> ival</span>,<span class="varname"> ival</span>]</span> </p></td> 
  <td class="stentry"> <p>Elenco separato da virgole delle dimensioni in pixel di tutte le visualizzazioni nella vignettatura di output (la visualizzazione a risoluzione completa per le vignettature piramidali), dell'immagine del pannello predefinita in un file di stile archivio o della prima immagine di opacità di una finestra che copre un file di stile. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">texturable=<span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p><span class="varname"> ival</span> è 1 se lo stile dell'archivio è testurizzabile, 0 in caso contrario. Non presente per i file di stile delle vignettature e delle copertine di finestre. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> avviso.<span class="varname"> n</span>=<span class="varname"> stringa</span></span> </p></td> 
  <td class="stentry"> <p>Messaggio di avviso (ad esempio, quando è specificato <span class="codeph"> -imagemap</span> ma non sono stati trovati dati mappa nella vignettatura). </p></td> 
 </tr> 
</table>
