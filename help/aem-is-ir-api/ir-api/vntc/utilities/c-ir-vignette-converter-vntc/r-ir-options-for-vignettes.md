---
description: Le seguenti opzioni controllano l'elaborazione dei file di vignettatura. Vengono ignorate se sourceFile non è una vignettatura.
seo-description: Le seguenti opzioni controllano l'elaborazione dei file di vignettatura. Vengono ignorate se sourceFile non è una vignettatura.
seo-title: Opzioni per le vignettature
solution: Experience Manager
title: Opzioni per le vignettature
topic: Scene7 Image Serving - Image Rendering API
uuid: 0cb40314-07ce-496b-a27b-560d7bb4fa8e
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Opzioni per le vignettature{#options-for-vignettes}

Le seguenti opzioni controllano l&#39;elaborazione dei file di vignettatura. Vengono ignorate se sourceFile non è una vignettatura.

<table id="simpletable_6D0C967EB84947FBAC34B46C4BB23AF0"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> -contents</span> </p></td> 
  <td class="stentry"> <p>Crea un file XML che rappresenta la gerarchia degli oggetti e include gli attributi degli oggetti selezionati. Il contenuto del file è lo stesso restituito dal comando <span class="codeph"> req=contents</span> . Il file ha lo stesso nome del file di origine, ma con un suffisso <span class="filepath"> .xml</span> . </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">-ritaglio <span class="varname"> x</span><span class="varname"> y</span><span class="varname"> wid</span><span class="varname"> hei</span></span> </p></td> 
  <td class="stentry"> <p>Ritagliare la vignettatura prima del ridimensionamento. </p> <p><span class="codeph"><span class="varname"> x</span>,<span class="varname"> y è l’angolo superiore sinistro del rettangolo di ritaglio e</span></span> wid <span class="codeph"><span class="varname"> ,</span>hei<span class="varname"></span></span> è la dimensione del rettangolo di ritaglio. I valori sono coordinate in pixel relative all’immagine di visualizzazione a risoluzione piena della vignettatura sorgente. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">-cropn <span class="varname"> xn</span><span class="varname"> yn</span><span class="varname"> wien hein</span><span class="varname"></span></span> </p> </td> 
  <td class="stentry"> <p>Ritagliare la vignettatura prima del ridimensionamento. </p> <p><span class="codeph"><span class="varname"> xn</span>,<span class="varname"> yn</span></span> è l'angolo superiore sinistro del rettangolo di ritaglio e <span class="codeph"><span class="varname"> widn</span>,<span class="varname"> hein</span></span> è la dimensione del rettangolo di ritaglio. I valori vengono normalizzati rispetto all’immagine di visualizzazione della vignettatura sorgente e devono essere compresi tra 0,0...1.0. </p> <p><span class="codeph"><span class="varname"> xn</span></span>+<span class="codeph"><span class="varname"> widn</span></span> e <span class="codeph"><span class="varname"> yn</span></span>+<span class="codeph"><span class="varname"> hein</span></span> non devono essere maggiori di 1,0. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> -embedmateriali</span> </p></td> 
  <td class="stentry"> <p>Mantenere i materiali incorporati nella vignettatura di output. Per impostazione predefinita, i materiali vengono rimossi dalla vignettatura di output. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">-height <span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p>Una o più altezze di vignettatura in pixel. Ignorato se è specificato -info. <span class="varname"> ival</span> può essere 0, che indica la larghezza della vignettatura di input. Per informazioni dettagliate, consultate <a href="../../../../ir-api/vntc/utilities/c-ir-vignette-converter-vntc/c-ir-vignette-scaling.md#concept-e373a29c2f954df98d704c7723804585" type="concept" format="dita" scope="local"> Ridimensionamento</a> vignettatura. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> -imagemap</span> </p></td> 
  <td class="stentry"> <p>Abilita l’estrazione del file della mappa immagine dalla vignettatura. I dati della mappa vengono scritti in un file HTML contenente solo un elemento <span class="codeph"> &lt;map&gt;</span> . Il file di output ha lo stesso nome del file immagine di output, ma con un suffisso <span class="filepath"> .htm</span> . Viene generato un messaggio di avviso e non viene creato alcun file se il comando è specificato ma non sono presenti dati mappa nella vignettatura. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> -profile</span> </p></td> 
  <td class="stentry"> <p>Salva in un file una copia del profilo ICC incorporato nella vignettatura. Viene generato un messaggio di avviso e non viene creato alcun file di profilo ICC se il comando è specificato ma nella vignettatura non è presente alcun profilo ICC. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> -piramide</span> </p></td> 
  <td class="stentry"> <p>Crea una vignettatura piramidale. Richiesto quando le immagini di cui è stato eseguito il rendering devono essere visualizzate con i visualizzatori zoom di Scene7. Per ulteriori informazioni, consultate <a href="../../../../ir-api/vntc/utilities/c-ir-vignette-converter-vntc/c-ir-vignette-scaling.md#concept-e373a29c2f954df98d704c7723804585" type="concept" format="dita" scope="local"> Ridimensionamento</a> vignettatura. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">-thumbnail <span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p>Limite di larghezza e altezza in pixel per l’immagine in miniatura. Se specificata, un'immagine JPEG che non sia più larga e non <span class="varname"> più alta del</span> cicloviene generata dall'immagine della vista vignettatura, da un'immagine del pannello del file di stile del cabinet o dalla mappa di illuminazione del primo stile nel file di stile dei rivestimenti delle finestre. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">-width <span class="varname"> ival</span> *[,<span class="varname"> ival</span>]</span> </p></td> 
  <td class="stentry"> <p>Una o più larghezze di vignettatura di output, in pixel. Ignorato se è specificato <span class="codeph"> -info</span> . <span class="varname"> ival</span> può essere 0, che indica l'altezza della vignettatura di input. Per informazioni dettagliate, consultate <a href="../../../../ir-api/vntc/utilities/c-ir-vignette-converter-vntc/c-ir-vignette-scaling.md#concept-e373a29c2f954df98d704c7723804585" type="concept" format="dita" scope="local"> Ridimensionamento</a> vignettatura. </p></td> 
 </tr> 
</table>

