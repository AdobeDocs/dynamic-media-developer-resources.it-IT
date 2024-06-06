---
description: Le opzioni seguenti controllano l'elaborazione dei file di vignettatura. Vengono ignorati se sourceFile non è una vignettatura.
solution: Experience Manager
title: Opzioni per le vignettature
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 7f9c2b43-9264-46a4-9519-64148aebf258
source-git-commit: 97fbf820590b53de5a1e6ce904e44d6b0ef9a214
workflow-type: tm+mt
source-wordcount: '461'
ht-degree: 0%

---

# Opzioni per le vignettature{#options-for-vignettes}

Le opzioni seguenti controllano l&#39;elaborazione dei file di vignettatura. Vengono ignorati se sourceFile non è una vignettatura.

<table id="simpletable_6D0C967EB84947FBAC34B46C4BB23AF0"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> -content</span> </p></td> 
  <td class="stentry"> <p>Crea un file XML che rappresenta la gerarchia degli oggetti e include gli attributi degli oggetti selezionati. Il contenuto del file è uguale a quello restituito da <span class="codeph"> req=content</span> comando. Il file ha lo stesso nome del file di origine, ma con <span class="filepath"> .xml</span> suffisso. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">-crop <span class="varname"> x</span><span class="varname"> y</span><span class="varname"> wid</span><span class="varname"> hei</span></span> </p></td> 
  <td class="stentry"> <p>Ritaglia la vignettatura prima del ridimensionamento. </p> <p><span class="codeph"><span class="varname"> x</span>,<span class="varname"> y</span></span> è l’angolo superiore sinistro del rettangolo di ritaglio e <span class="codeph"><span class="varname"> wid</span>,<span class="varname"> hei</span></span> è la dimensione del rettangolo di ritaglio. I valori sono coordinate in pixel relative all'immagine di visualizzazione a risoluzione completa della vignettatura sorgente. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">-cropn <span class="varname"> xn</span><span class="varname"> yn</span><span class="varname"> larghezza</span><span class="varname"> manicomio</span></span> </p> </td> 
  <td class="stentry"> <p>Ritaglia la vignettatura prima del ridimensionamento. </p> <p><span class="codeph"><span class="varname"> xn</span>,<span class="varname"> yn</span></span> è l’angolo superiore sinistro del rettangolo di ritaglio e <span class="codeph"><span class="varname"> larghezza</span>,<span class="varname"> manicomio</span></span> è la dimensione del rettangolo di ritaglio. I valori vengono normalizzati rispetto all'immagine di visualizzazione della vignettatura di origine e devono essere compresi tra 0,0...1,0. </p> <p><span class="codeph"><span class="varname"> xn</span></span>+<span class="codeph"><span class="varname"> larghezza</span></span> e <span class="codeph"><span class="varname"> yn</span></span>+<span class="codeph"><span class="varname"> manicomio</span></span> non deve essere maggiore di 1,0. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> -materiali incorporati</span> </p></td> 
  <td class="stentry"> <p>Mantieni i materiali incorporati nella vignettatura di output. Per impostazione predefinita, i materiali vengono rimossi dalla vignettatura di output. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">-height <span class="varname"> fiala</span></span> </p></td> 
  <td class="stentry"> <p>Una o più altezze di vignettatura di output in pixel. Ignorato se si specifica -info. <span class="varname"> fiala</span> può essere 0, che indica la larghezza della vignettatura di input. Consulta <a href="../../../../ir-api/vntc/utilities/c-ir-vignette-converter-vntc/c-ir-vignette-scaling.md#concept-e373a29c2f954df98d704c7723804585" type="concept" format="dita" scope="local"> Ridimensionamento vignettatura</a> per informazioni dettagliate. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> -mappa immagine</span> </p></td> 
  <td class="stentry"> <p>Abilita l'estrazione del file di mappa immagine dalla vignettatura. I dati della mappa vengono scritti in un file HTML che contiene solo <span class="codeph"> &lt;map&gt;</span> elemento. Il file di output è denominato come il file di immagine di output, ma con un <span class="filepath"> .htm</span> suffisso. Viene generato un messaggio di avviso e non viene creato alcun file se il comando è specificato ma non sono presenti dati di mappa nella vignettatura. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> -profile</span> </p></td> 
  <td class="stentry"> <p>Salva in un file una copia del profilo ICC incorporato nella vignettatura. Viene generato un messaggio di avviso e non viene creato alcun file di profilo ICC se il comando è specificato ma non è presente alcun profilo ICC nella vignettatura. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> -piramide</span> </p></td> 
  <td class="stentry"> <p>Crea una vignettatura piramidale. Obbligatorio quando le immagini sottoposte a rendering devono essere visualizzate con i visualizzatori zoom di Dynamic Medie. Consulta <a href="../../../../ir-api/vntc/utilities/c-ir-vignette-converter-vntc/c-ir-vignette-scaling.md#concept-e373a29c2f954df98d704c7723804585" type="concept" format="dita" scope="local"> Ridimensionamento vignettatura</a> per ulteriori informazioni. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">-thumbwidth <span class="varname"> fiala</span></span> </p></td> 
  <td class="stentry"> <p>Vincolo di larghezza e altezza pixel per l'immagine miniatura. Se è specificata, un'immagine JPEG che non è più larga e non è più alta di <span class="varname"> fiala</span> viene generata dall'immagine di visualizzazione vignettatura, da un'immagine del pannello del file di stile dell'archivio o dalla mappa di illuminazione del primo stile nel file di stile dei rivestimenti delle finestre. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">-larghezza <span class="varname"> fiala</span> *[,<span class="varname"> fiala</span>]</span> </p></td> 
  <td class="stentry"> <p>Una o più larghezze di vignettatura di output in pixel. Ignorato se <span class="codeph"> -info</span> è specificato. <span class="varname"> fiala</span> può essere 0, che indica l'altezza della vignettatura di input. Consulta <a href="../../../../ir-api/vntc/utilities/c-ir-vignette-converter-vntc/c-ir-vignette-scaling.md#concept-e373a29c2f954df98d704c7723804585" type="concept" format="dita" scope="local"> Ridimensionamento vignettatura</a> per informazioni dettagliate. </p></td> 
 </tr> 
</table>
