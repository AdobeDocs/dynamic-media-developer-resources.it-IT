---
description: vntc genera i dati di testo che vengono inviati a store o al file di registro.
seo-description: vntc genera i dati di testo che vengono inviati a store o al file di registro.
seo-title: Uscita
solution: Experience Manager
title: Uscita
topic: Scene7 Image Serving - Image Rendering API
uuid: f2041600-408f-481c-95fc-3c112def7b8a
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '688'
ht-degree: 0%

---


# Output{#output}

vntc genera i dati di testo che vengono inviati a store o al file di registro.

I dati vengono formattati come una proprietà `name=value` per record di testo. I valori stringa non sono citati. I messaggi di avviso e di errore vengono sempre inviati a `stderr`, anche se è specificato `-log`.

Alcune proprietà possono verificarsi più volte nello stesso output. Un numero di sequenza, a partire da 0, viene aggiunto al nome di queste proprietà, separato da un punto. Tali proprietà sono identificate di seguito con un suffisso `. *`n`*` dopo il nome della proprietà.

Vengono generate le seguenti proprietà:

<table id="simpletable_32AAA1A2DDB04BC6B86885E6223BF609"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">bgc=<span class="varname"> ival</span>,<span class="varname"> ival</span>,<span class="varname"> ival</span></span> </p> </td> 
  <td class="stentry"> <p>Colore di sfondo RGB dello stile del cabinet. Solo stili di archivio. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">defaultFileVersion=<span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p>La versione predefinita del file di output. Anche la versione più alta di questo rilascio di <span class="filepath"> vntc</span> può generare. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">error.<span class="varname"> n</span>=<span class="varname"> string</span></span> </p></td> 
  <td class="stentry"> <p>Messaggio di errore. In genere, la presenza di messaggi di errore indica che non viene creato alcun file di output o che non è adatto per l’utilizzo con il rendering delle immagini. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">file.<span class="varname"> n</span>=<span class="varname"> string</span></span> </p></td> 
  <td class="stentry"> <p>Percorso/nome completo di tutti i file di output, inclusi vignettature, file di stile cabinet, immagini a risoluzione piena e immagini in miniatura. Per ciascun file generato è presente un attributo di file (ad eccezione del file di registro). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">glass=<span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p><span class="varname"> </span> ivalis 1 se l'armadio include porte in vetro, 0 in caso contrario. Solo stili di archivio. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">iccProfile=<span class="varname"> string</span></span> </p></td> 
  <td class="stentry"> <p>Il nome dell'iccProfile incorporato in <span class="varname"> sourceFile</span>. </p> <p>Vuoto se <span class="varname"> sourceFile</span> non è gestito dal colore. Solo vignettature. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">info.<span class="varname"> n</span>=<span class="varname"> string</span></span> </p></td> 
  <td class="stentry"> <p>Messaggio informativo, ad esempio informazioni sullo stato di avanzamento. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">sourceIsMaster=<span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p><span class="varname"> </span> ivalis 1 se  <span class="varname"> </span> sourceFileè una vignettatura master, 0 se è stata elaborata in precedenza con  <span class="filepath"> </span> vnUpdateor  <span class="filepath"> vntc</span>. Solo vignettature. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">master=<span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p><span class="varname"> </span> ivalis 0 se  <span class="varname"> </span> sourceFileè uno stile cabinet contenente dati immagine JPEG (in questo caso viene emesso anche un avviso), 1 in caso contrario. Archivio e finestra che coprono solo i file di stile. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">maxMem=<span class="varname"> string</span></span> </p></td> 
  <td class="stentry"> <p>Limite massimo di memoria applicabile al processo <span class="filepath"> vntc</span> in esecuzione. <span class="varname"> </span> stringis è  <span class="varname"> festival</span>,  <span class="varname"> ivalK</span>,  <span class="varname"> ivalM</span>,  <span class="varname"> ivalG</span> o  <span class="codeph">  </span> 0(disattivato). Dove <span class="varname"> K</span>, <span class="varname"> M</span> e <span class="varname"> G</span> si riferiscono a kilobyte (1024 byte), Megabyte (1048576 byte) e Gigabyte (1073741824 byte) . </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">maxScl=<span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p>Scala del livello della piramide di risoluzione più basso nella vignettatura di output. Presente solo se è specificato <span class="codeph"> -piramide</span>. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">numMaterials=<span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p>Il numero di materiali salvati in <span class="varname"> sourceFile</span>. Solo vignettature. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">numPanels=<span class="codeph"> ival</span></span> </p></td> 
  <td class="stentry"> <p>Il numero di immagini del pannello nel file di stile del cabinet. Solo stili di archivio. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">numViews=<span class="codeph"> ival</span></span> </p></td> 
  <td class="stentry"> <p>Numero di livelli piramidali nella vignettatura di output. Presente solo se è specificato -piramide. Solo vignettature. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">piramide=<span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p>0 se la vignettatura di origine o di destinazione ha una struttura a piramide. Solo vignettature. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">resolution=<span class="varname"> val</span></span> </p></td> 
  <td class="stentry"> <p>Per gli stili di archivio, la risoluzione dell'oggetto del file <span class="varname"> sourceFile</span>. Per le vignettature, si tratta della risoluzione materiale consigliata per ottenere risultati di rendering di qualità ottimale durante il rendering della vignettatura di output. Pixel/pollice (ppi). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">resolution.min=<span class="varname"> val</span></span> </p></td> 
  <td class="stentry"> <p>La risoluzione dell'oggetto più piccola nella vignettatura di output. Solo vignettature. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">resolution.avg=<span class="varname"> val</span></span> </p></td> 
  <td class="stentry"> <p>La risoluzione media dell'oggetto nella vignettatura di output. Solo vignettature. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">sourceFile=<span class="varname"> string</span></span> </p></td> 
  <td class="stentry"> <p>Percorso <span class="varname"> sourceFile</span> completo. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">sourceFileVersion=<span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p>La versione del file di <span class="varname"> sourceFile</span>. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">sourceSize=<span class="varname"> ival</span>,<span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p>La dimensione in pixel della vignettatura di input, l'immagine predefinita del pannello in un file di stile del cabinet o la prima immagine di opacità di un file di stile della finestra che copre il file. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">style=<span class="varname"> string</span></span> </p></td> 
  <td class="stentry"> <p>Tipo di copertura della finestra (solo stili di copertura della finestra): </p> <p> 
    <ul id="ul_51AECE556B8B40109FFAD2B315D0695C"> 
     <li id="li_3D3B9211C7AF4810883AE815BEBD4228">0=ombreggiatura orizzontale o persiane </li> 
     <li id="li_DE88052467D64ECDAEB29264FC3904E4">1 = persiane verticali </li> 
     <li id="li_6F976CABF7244B20A471391A685ED05F"> 2=tende corte a larghezza intera </li> 
     <li id="li_E8D2B0B9189F4BDBB70E145E9196C1CD">3 = drappi brevi sinistro/destro </li> 
     <li id="li_026F043A50D34C8AB850D9832F375DB7"> 4=tende a larghezza intera </li> 
     <li id="li_283A2E5BFF75461B8F697FFF0796361F"> 5 = drappi di lunghezza intera sinistra/destra </li> 
     <li id="li_E175BA9EAE1F46B89109F4892FF54656"> 6=tenda del caffè </li> 
     <li id="li_79D2F7F68C4746F3B6742EFECD01BDD9"> 7=valore </li> 
    </ul> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">suffix=<span class="varname"> string</span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> </span> vntif  <span class="varname"> </span> sourceFileè una vignettatura,  <span class="codeph"> </span> vncif  <span class="varname"> </span> sourceFileè uno stile cabinet o  <span class="codeph"> </span> vnwif  <span class="varname"> </span> sourceFileè uno stile di copertura della finestra. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">targetFileVersion=<span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p>Il valore specificato con <span class="codeph"> -version</span> o con il valore di<span class="codeph"> defaultFileVersion</span> se non è stato specificato <span class="codeph"> -version</span>. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">targetSises=<span class="varname"> ival</span>,<span class="varname"> ival</span>*[,<span class="varname"> ival</span>,<span class="varname"> ival</span>]</span> </p></td> 
  <td class="stentry"> <p>Elenco separato da virgole delle dimensioni in pixel di tutte le viste nella vignettatura di output (la visualizzazione a risoluzione completa per le vignettature a piramide), dell’immagine del pannello predefinita in un file di stile cabinet o della prima immagine di opacità di un file di stile di una finestra che copre le finestre. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">texturable=<span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p><span class="varname"> </span> ivalis 1 se lo stile del cabinet è texturable, 0 in caso contrario. Non presente per i file di stile vignettature e rivestimenti finestre. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">alert.<span class="varname"> n</span>=<span class="varname"> string</span></span> </p></td> 
  <td class="stentry"> <p>Messaggio di avviso (ad esempio quando <span class="codeph"> -imagemap</span> è specificato ma non sono presenti dati mappa nella vignettatura). </p></td> 
 </tr> 
</table>

