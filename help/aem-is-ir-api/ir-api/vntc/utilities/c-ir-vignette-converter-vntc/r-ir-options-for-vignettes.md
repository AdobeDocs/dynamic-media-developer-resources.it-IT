---
description: Le seguenti opzioni controllano l'elaborazione dei file di vignetta. Vengono ignorati se sourceFile non è una vignetta.
solution: Experience Manager
title: Opzioni per le vignette
feature: Dynamic Media Classic, SDK/API
role: Developer,Business Practitioner
exl-id: 7f9c2b43-9264-46a4-9519-64148aebf258
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '460'
ht-degree: 0%

---

# Opzioni per le vignette{#options-for-vignettes}

Le seguenti opzioni controllano l&#39;elaborazione dei file di vignetta. Vengono ignorati se sourceFile non è una vignetta.

<table id="simpletable_6D0C967EB84947FBAC34B46C4BB23AF0"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> -content</span> </p></td> 
  <td class="stentry"> <p>Crea un file XML che rappresenta la gerarchia degli oggetti e include gli attributi degli oggetti selezionati. Il contenuto del file è lo stesso restituito dal comando <span class="codeph"> req=content</span> . Il file ha lo stesso nome del file di origine, ma con un suffisso <span class="filepath"> .xml</span>. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">-  <span class="varname"> </span><span class="varname"> </span><span class="varname"> </span><span class="varname"> xywidhei di ritaglio</span></span> </p></td> 
  <td class="stentry"> <p>Ritaglia la vignetta prima del ridimensionamento. </p> <p><span class="codeph"><span class="varname"> x</span>, <span class="varname"> </span></span> yè l’angolo in alto a sinistra del rettangolo di ritaglio, e  <span class="codeph"><span class="varname"> wid</span>, <span class="varname"> </span></span> corrisponde alle dimensioni del rettangolo di ritaglio. I valori sono coordinate pixel relative all'immagine di visualizzazione a risoluzione piena della vignetta sorgente. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">-cropn  <span class="varname"> </span><span class="varname"> </span><span class="varname"> </span><span class="varname"> xnynwidnhein</span></span> </p> </td> 
  <td class="stentry"> <p>Ritaglia la vignetta prima del ridimensionamento. </p> <p><span class="codeph"><span class="varname"> xn</span>, <span class="varname"> </span></span> ynis l'angolo superiore sinistro del rettangolo di ritaglio e  <span class="codeph"><span class="varname"> widn</span>, <span class="varname"> </span></span> considera le dimensioni del rettangolo di ritaglio. I valori vengono normalizzati rispetto all’immagine di visualizzazione della vignetta sorgente e devono essere compresi tra 0,0...1.0. </p> <p><span class="codeph"><span class="varname"> xn</span></span>+<span class="codeph"><span class="varname"> </span></span> widnand  <span class="codeph"><span class="varname"> yn</span></span>+<span class="codeph"><span class="varname"> </span></span> heindeve essere non maggiore di 1.0. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> -materiali da incorporamento</span> </p></td> 
  <td class="stentry"> <p>Mantenere i materiali incorporati nella vignetta di uscita. Per impostazione predefinita i materiali vengono rimossi dalla vignetta di output. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">-  <span class="varname"> Festival in altezza</span></span> </p></td> 
  <td class="stentry"> <p>Una o più altezze della vignetta di uscita in pixel. Ignorato se è specificato -info. <span class="varname"> </span> ivalmay be 0, che denota la larghezza della vignetta di input. Per informazioni dettagliate, consulta <a href="../../../../ir-api/vntc/utilities/c-ir-vignette-converter-vntc/c-ir-vignette-scaling.md#concept-e373a29c2f954df98d704c7723804585" type="concept" format="dita" scope="local"> Ridimensionamento vignetta</a> . </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> -imagemap</span> </p></td> 
  <td class="stentry"> <p>Abilita l’estrazione del file di mappa immagine dalla vignetta. I dati della mappa vengono scritti in un file HTML contenente solo un elemento <span class="codeph"> &lt;map&gt;</span>. Il file di output viene denominato come file immagine di output, ma con un suffisso <span class="filepath"> .htm</span>. Viene generato un messaggio di avviso e non viene creato alcun file se il comando è specificato ma non sono presenti dati mappa nella vignetta. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> -profile</span> </p></td> 
  <td class="stentry"> <p>Salva in un file una copia del profilo ICC incorporato nella vignetta. Viene generato un messaggio di avviso e non viene creato alcun file di profilo ICC se il comando è specificato ma nella vignetta non è presente alcun profilo ICC. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> -piramide</span> </p></td> 
  <td class="stentry"> <p>Crea una vignetta piramidale. Richiesto quando le immagini riprodotte devono essere visualizzate con visualizzatori zoom Dynamic Media. Per ulteriori informazioni, consulta <a href="../../../../ir-api/vntc/utilities/c-ir-vignette-converter-vntc/c-ir-vignette-scaling.md#concept-e373a29c2f954df98d704c7723804585" type="concept" format="dita" scope="local"> Ridimensionamento vignetta</a> . </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">-thumbwidth  <span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p>Vincolo di larghezza e altezza dei pixel per l'immagine in miniatura. Se specificato, un'immagine JPEG che non è più larga e non più alta di <span class="varname"> ival</span> viene generata dall'immagine di visualizzazione della vignetta, da un'immagine a pannello del file di stile dell'archivio o dalla mappa di illuminazione del primo stile nel file di stile dei rivestimenti delle finestre. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">-width  <span class="varname"> ival</span> *[,<span class="varname"> ival</span>]</span> </p></td> 
  <td class="stentry"> <p>Una o più larghezze di vignetta di uscita in pixel. Ignorato se è specificato <span class="codeph"> -info</span> . <span class="varname"> </span> ivalmay be 0, che denota l'altezza della vignetta di input. Per informazioni dettagliate, consulta <a href="../../../../ir-api/vntc/utilities/c-ir-vignette-converter-vntc/c-ir-vignette-scaling.md#concept-e373a29c2f954df98d704c7723804585" type="concept" format="dita" scope="local"> Ridimensionamento vignetta</a> . </p></td> 
 </tr> 
</table>
