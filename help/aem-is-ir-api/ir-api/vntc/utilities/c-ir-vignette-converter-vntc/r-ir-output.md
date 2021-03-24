---
description: vntc genera dati di testo che vengono inviati a stderr o al file di log.
solution: Experience Manager
title: Uscita
feature: Dynamic Media Classic, SDK/API
role: Sviluppatore, Business Practices
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '681'
ht-degree: 0%

---


# Output{#output}

vntc genera dati di testo che vengono inviati a stderr o al file di log.

I dati vengono formattati come una proprietà `name=value` per record di testo. I valori stringa non sono tra virgolette. I messaggi di avviso e di errore vengono sempre inviati a `stderr`, anche se è specificato `-log`.

Alcune proprietà possono verificarsi più volte nello stesso output. Al nome di queste proprietà viene aggiunto un numero di sequenza, che inizia con 0, separato da un punto. Tali proprietà sono identificate di seguito con un suffisso `. *`n`*` dopo il nome della proprietà.

Vengono generate le seguenti proprietà:

<table id="simpletable_32AAA1A2DDB04BC6B86885E6223BF609"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">bgc=<span class="varname"> ival</span>, <span class="varname"> ival</span>, <span class="varname"> ival</span></span> </p> </td> 
  <td class="stentry"> <p>Colore di sfondo RGB dello stile del cabinet. Solo stili del cabinet. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">defaultFileVersion=<span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p>Versione predefinita del file di output. Anche la versione più alta del file può essere generata da questa versione di <span class="filepath"> vntc</span>. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">errore.<span class="varname"> n</span>=<span class="varname"> string</span></span> </p></td> 
  <td class="stentry"> <p>Messaggio di errore. In genere, la presenza di messaggi di errore indica che non viene creato alcun file di output o che non è adatto all’uso da parte di Image Rendering. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">file.<span class="varname"> n</span>=<span class="varname"> string</span></span> </p></td> 
  <td class="stentry"> <p>Il percorso/nome completo di tutti i file di output, compresi vignette, file di stile dell'archivio, immagini a risoluzione piena e immagini in miniatura. È presente un attributo di file per ogni file generato (ad eccezione del file di registro). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">glass=<span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p><span class="varname"> </span> ivalis 1 se l'armadio include porte in vetro, altrimenti 0. Solo stili del cabinet. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">iccProfile=<span class="varname"> string</span></span> </p></td> 
  <td class="stentry"> <p>Nome dell'iccProfile incorporato in <span class="varname"> sourceFile</span>. </p> <p>Vuoto se <span class="varname"> sourceFile</span> non è gestito dal colore. Solo vignette. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">info.<span class="varname"> n</span>=<span class="varname"> string</span></span> </p></td> 
  <td class="stentry"> <p>Messaggio informativo, ad esempio informazioni sullo stato di avanzamento. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">sourceIsMaster=<span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p><span class="varname"> </span> ivalis 1 se  <span class="varname"> </span> sourceFileè una vignetta master, 0 se è stata elaborata in precedenza con  <span class="filepath"> </span> vnUpdateor  <span class="filepath"> vntc</span>. Solo vignette. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">master=<span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p><span class="varname"> </span> ivalis 0 se  <span class="varname"> </span> sourceFileè uno stile di archivio contenente dati immagine JPEG (in questo caso viene emesso anche un avviso), 1 in caso contrario. Cabinet e finestra che coprono solo i file di stile. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">maxMem=<span class="varname"> string</span></span> </p></td> 
  <td class="stentry"> <p>Limite massimo di memoria applicabile al processo <span class="filepath"> vntc</span> in esecuzione. <span class="varname"> </span> stringis è  <span class="varname"> ival</span>,  <span class="varname"> ivalK</span>,  <span class="varname"> ivalM</span>,  <span class="varname"> ivalG</span> o  <span class="codeph"> 0</span> (disabilitato). Dove <span class="varname"> K</span>, <span class="varname"> M</span> e <span class="varname"> G</span> fanno riferimento a Kilobyte (1024 byte), Megabyte (1048576 byte) e Gigabyte (1073741824 byte) . </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">maxScl=<span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p>Scala del livello a piramide a risoluzione più bassa nella vignetta di uscita. Presente solo se è specificato <span class="codeph"> -pyramid</span>. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">numMaterials=<span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p>Il numero di materiali salvati in <span class="varname"> sourceFile</span>. Solo vignette. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">numPanels=<span class="codeph"> ival</span></span> </p></td> 
  <td class="stentry"> <p>Il numero di immagini del pannello nel file di stile dell'archivio. Solo stili del cabinet. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">numViews=<span class="codeph"> ival</span></span> </p></td> 
  <td class="stentry"> <p>Numero di livelli piramidali nella vignetta di output. Presente solo se è specificato -piramide. Solo vignette. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">piramide=<span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p>0 se la vignetta di origine o di destinazione ha una struttura a piramide. Solo vignette. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">resolution=<span class="varname"> val</span></span> </p></td> 
  <td class="stentry"> <p>Per gli stili dell'archivio, la risoluzione dell'oggetto di <span class="varname"> sourceFile</span>. Per le vignette, si tratta della risoluzione del materiale consigliata per ottenere risultati di rendering di migliore qualità durante il rendering della vignetta di output. Pixel/pollice (ppi). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">resolution.min=<span class="varname"> val</span></span> </p></td> 
  <td class="stentry"> <p>La risoluzione dell'oggetto più piccola nella vignetta di output. Solo vignette. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">resolution.avg=<span class="varname"> val</span></span> </p></td> 
  <td class="stentry"> <p>La risoluzione media dell'oggetto nella vignetta di output. Solo vignette. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">sourceFile=<span class="varname"> string</span></span> </p></td> 
  <td class="stentry"> <p>Percorso <span class="varname"> sourceFile</span> completo. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">sourceFileVersion=<span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p>Versione file di <span class="varname"> sourceFile</span>. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">sourceSize=<span class="varname"> ival</span>,<span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p>La dimensione in pixel della vignetta di input, l'immagine predefinita del pannello in un file di stile del cabinet o la prima immagine di opacità di una finestra che copre il file di stile. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">style=<span class="varname"> string</span></span> </p></td> 
  <td class="stentry"> <p>Tipo di copertura della finestra (solo per gli stili della finestra): </p> <p> 
    <ul id="ul_51AECE556B8B40109FFAD2B315D0695C"> 
     <li id="li_3D3B9211C7AF4810883AE815BEBD4228">0=ombreggiatura orizzontale o tende </li> 
     <li id="li_DE88052467D64ECDAEB29264FC3904E4">1=tende verticali </li> 
     <li id="li_6F976CABF7244B20A471391A685ED05F"> 2=tende corte a larghezza intera </li> 
     <li id="li_E8D2B0B9189F4BDBB70E145E9196C1CD">3=tende corte sinistra/destra </li> 
     <li id="li_026F043A50D34C8AB850D9832F375DB7"> 4=tende a tutta larghezza </li> 
     <li id="li_283A2E5BFF75461B8F697FFF0796361F"> 5=drappi a destra/a sinistra </li> 
     <li id="li_E175BA9EAE1F46B89109F4892FF54656"> 6=tenda di caffè </li> 
     <li id="li_79D2F7F68C4746F3B6742EFECD01BDD9"> 7=valance </li> 
    </ul> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">suffix=<span class="varname"> string</span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> </span> vntif  <span class="varname"> </span> sourceFileè una vignetta,  <span class="codeph"> </span> vncif  <span class="varname"> </span> sourceFileè uno stile di archivio o  <span class="codeph"> </span> vnwif  <span class="varname"> </span> sourceFileis una finestra che copre lo stile. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">targetFileVersion=<span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p>Il valore specificato con <span class="codeph"> -version</span> o il valore di<span class="codeph"> defaultFileVersion</span> se<span class="codeph"> -version</span> non è stato specificato. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">targetSize=<span class="varname"> ival</span>, <span class="varname"> ival</span>*[, <span class="varname"> ival</span>, <span class="varname"> ival</span>]</span> </p></td> 
  <td class="stentry"> <p>Elenco separato da virgole delle dimensioni dei pixel di tutte le visualizzazioni nella vignetta di output (la visualizzazione a risoluzione piena per le vignette a piramide), dell'immagine del pannello predefinita in un file di stile di archivio o della prima immagine di opacità di una finestra che copre file di stile. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">texturable=<span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p><span class="varname"> </span> ivalis 1 se lo stile dell'armadio è texture, 0 in caso contrario. Non presente per i file di stile vignette e rivestimenti finestre. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">avviso.<span class="varname"> n</span>=<span class="varname"> string</span></span> </p></td> 
  <td class="stentry"> <p>Messaggio di avviso (ad esempio se è specificato <span class="codeph"> -imagemap</span> ma non sono presenti dati mappa nella vignetta). </p></td> 
 </tr> 
</table>

