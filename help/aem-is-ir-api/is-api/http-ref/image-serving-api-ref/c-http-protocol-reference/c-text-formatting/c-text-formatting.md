---
description: Image Server offre diverse alternative per il rendering del testo, accessibili con i comandi text= e textPs=.
seo-description: Image Server offre diverse alternative per il rendering del testo, accessibili con i comandi text= e textPs=.
seo-title: Formattazione del testo
solution: Experience Manager
title: Formattazione del testo
topic: Scene7 Image Serving - Image Rendering API
uuid: e67b6dd2-2a78-4014-9525-816d91c9e783
translation-type: tm+mt
source-git-commit: 94a26628ec619076f0942e9278165cc591f1c150

---


# Formattazione del testo{#text-formatting}

Image Server offre diverse alternative per il rendering del testo, accessibili con i comandi text= e textPs=.

`textPs=` offre un alto livello di similarità con il testo rappresentato con Adobe Photoshop e Illustrator. `text=` è ragionevolmente compatibile con il testo rappresentato con Windows Wordpad.

>[!NOTE]
>
>Oltre alle differenze elencate altrove, `text=` produce lievi differenze nel testo di cui è stato effettuato il rendering rispetto al testo `textPs=`. Ad esempio, le sottolineature non hanno lo stesso spessore e la stessa posizione e il corsivo sintetizzato viene rappresentato con un angolo leggermente diverso. Se il testo non rientra nello spazio disponibile, `text=` può ritagliare parzialmente l’ultima riga, mentre `textPs=` sarà possibile eseguire solo il rendering di righe complete.

Tutti i comandi di testo accettano testo formattato in base a un sottoinsieme della specifica RTF (Rich Text Format). Ogni livello di testo può specificare un comando di testo diverso.

Nella tabella seguente sono elencate le funzioni chiave disponibili per ciascun comando di testo:

<table id="table_9C41CBDA94C24805B538E5049B0137C6"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> Feature</b> </th> 
   <th class="entry"> <b> Testo=</b> </th> 
   <th class="entry"> <b> textPs=</b> </th> 
   <th class="entry"> <b> Consultate anche</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p> Compatibile con Adobe Photoshop </p> </td> 
   <td> <p> no </p> </td> 
   <td> <p> limitato </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>Convertire il testo in forme arbitrarie </p> </td> 
   <td> <p>no </p> </td> 
   <td> <p>yes </p> </td> 
   <td> <p>textFlowPath=, textFlowXPath= </p> </td> 
  </tr> 
  <tr> 
   <td> <p>Testo scorrevole lungo percorsi arbitrari </p> </td> 
   <td> <p>no </p> </td> 
   <td> <p>yes </p> </td> 
   <td> <p>textPath= </p> </td> 
  </tr> 
  <tr> 
   <td> <p>Adattamento copia </p> </td> 
   <td> <p>no </p> </td> 
   <td> <p>yes </p> </td> 
   <td> Adatta <p>, \copyfit, \copyfitlines, \copyfitmaxlines </p> </td> 
  </tr> 
  <tr> 
   <td> <p>Margini casella di testo </p> </td> 
   <td> <p>no </p> </td> 
   <td> <p>yes </p> </td> 
   <td> <p>\margl, \margr, \margt, \margb </p> </td> 
  </tr> 
  <tr> 
   <td> <p>Giustificazione completa del paragrafo </p> </td> 
   <td> <p>no </p> </td> 
   <td> <p>yes </p> </td> 
   <td> <p>\qj </p> </td> 
  </tr> 
  <tr> 
   <td> <p>ultima riga, giustificazione </p> </td> 
   <td> <p>no </p> </td> 
   <td> <p>yes </p> </td> 
   <td> <p>\lastql, \lastqr, \lastqc, \lastqj </p> </td> 
  </tr> 
  <tr> 
   <td> <p>Rientro paragrafo </p> </td> 
   <td> <p>no </p> </td> 
   <td> <p>yes </p> </td> 
   <td> <p>\fi, \li, \ri </p> </td> 
  </tr> 
  <tr> 
   <td> <p>Testo maiuscoletto e maiuscoletto </p> </td> 
   <td> <p>no </p> </td> 
   <td> <p>yes </p> </td> 
   <td> <p>\caps, \scaps </p> </td> 
  </tr> 
  <tr> 
   <td> <p>Image Serving Colour </p> </td> 
   <td> <p>no </p> </td> 
   <td> <p>yes </p> </td> 
   <td> <p>\*\iscolortbl </p> </td> 
  </tr> 
  <tr> 
   <td> <p>Modalità anti-alias multiple </p> </td> 
   <td> <p>no </p> </td> 
   <td> <p>yes </p> </td> 
   <td> <p>textAttr= </p> </td> 
  </tr> 
  <tr> 
   <td> <p>scorrimento del testo in alto in basso/a destra a sinistra </p> </td> 
   <td> <p>no </p> </td> 
   <td> <p>yes </p> </td> 
   <td> <p>\stextFlow </p> </td> 
  </tr> 
  <tr> 
   <td> <p>Supporto per Photofont® </p> </td> 
   <td> <p>no </p> </td> 
   <td> <p>yes </p> </td> 
   <td> Gestione dei font </td> 
  </tr> 
  <tr> 
   <td> <p>Ridimensionare automaticamente il livello per adattare il testo </p> </td> 
   <td> <p>yes </p> </td> 
   <td> <p>yes </p> </td> 
   <td> <p>text=, textId=, size= </p> </td> 
  </tr> 
  <tr> 
   <td> <p>Supporto CMYK </p> </td> 
   <td> <p>yes </p> </td> 
   <td> <p>yes </p> </td> 
   <td> <p>\cmykcolortbl, \*\iscolortbl </p> </td> 
  </tr> 
  <tr> 
   <td> <p>Flusso di caratteri da destra a sinistra </p> </td> 
   <td> <p>yes </p> </td> 
   <td> <p>no </p> </td> 
   <td> <p>\rtlch </p> </td> 
  </tr> 
  <tr> 
   <td> <p>Disattiva ritorno a capo automatico </p> </td> 
   <td> <p>yes </p> </td> 
   <td> <p>no </p> </td> 
   <td> <p>textAttr= </p> </td> 
  </tr> 
  <tr> 
   <td> <p>Scala automaticamente il testo per adattarlo al livello (con risoluzione variabile) </p> </td> 
   <td> <p>yes </p> </td> 
   <td> <p>no </p> </td> 
   <td> <p>textAttr= </p> </td> 
  </tr> 
 </tbody> 
</table>

Le stringhe compatibili con RTF possono essere assemblate manualmente o formattando il testo desiderato in un editor di testo o in un elaboratore di testi in grado di salvare i file RTF. Il file RTF può quindi essere aperto in un editor di testo normale e il contenuto RTF del file pertinente copiato nell&#39;URL della richiesta.

Alcuni elaboratori di testi generano file di dimensioni piuttosto grandi, che includono prerequisiti sostanziali non utilizzati da Scene7 Image Server. Si consiglia di rimuovere gli elementi RTF non utilizzati dalla stringa prima di passare la stringa ai comandi di testo.

La codifica della lingua basata sugli standard UTF-8 e ISO è supportata nelle stringhe RTF come alternativa ai meccanismi standard di codifica dei caratteri RTF. Questo consente alle applicazioni di inviare testo non in inglese al server senza conoscere la codifica RTF.

Tutti i caratteri non conformi a HTTP devono essere preceduti dalla corretta escape, se la stringa deve essere trasmessa tramite http. Solo &#39;=&#39;, &#39;&amp;&#39; e &#39;%&#39; devono essere preceduti da escape se la stringa è incorporata nel `catalog::Modifiers` campo di un record di catalogo immagini. I caratteri di controllo, inclusi `<CR>`, `<LF>`, e `<TAB>` devono sempre essere rimossi.

I motori di testo Image Server interpretano un sottoinsieme di comandi definiti dalla specifica Rich Text Format (RTF), versione 1.6. Questo sottoinsieme è incentrato sulla formattazione di font/caratteri, sulla semplice formattazione del paragrafo e sul supporto per font e set di caratteri internazionali. Al momento, costrutti di formattazione più avanzati, come fogli di stile e tabelle, non sono supportati.

Quando si tenta di creare manualmente stringhe di testo con codifica RTF, è necessario conoscere la specifica Rich Text Format (RTF) pubblicata da Microsoft.

* [Gestione dei font](r-font-handling.md)
* [Gestione del colore](r-color-handling.md)
* [Adattamento copia](r-copy-fitting.md)
* [Livelli di testo](r-text-layers.md)
* [Posizionamento del testo](r-text-positioning.md)
* [Caratteri riservati](r-reserved-characters.md)
* [Comandi e parole chiave RTF supportati](c-supported-rtf-commands-and-keywords/c-supported-rtf-commands-and-keywords.md)
* [Esempi di codifica RTF](r-rtf-encoding-examples.md)
