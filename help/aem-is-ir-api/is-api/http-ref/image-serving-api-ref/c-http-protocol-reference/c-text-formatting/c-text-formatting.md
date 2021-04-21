---
description: Image Serving fornisce diverse alternative per il rendering del testo, accessibili con i comandi text= e textPs=.
solution: Experience Manager
title: Formattazione testo
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '565'
ht-degree: 0%

---


# Formattazione testo{#text-formatting}

Image Serving fornisce diverse alternative per il rendering del testo, accessibili con i comandi text= e textPs=.

`textPs=` fornisce un alto livello di somiglianza con il testo di cui è stato eseguito il rendering con Adobe Photoshop e Illustrator. `text=` è ragionevolmente compatibile con il testo di cui è stato eseguito il rendering con Windows Wordpad.

>[!NOTE]
>
>Oltre alle differenze elencate altrove, `text=` produce sottili differenze nel testo sottoposto a rendering rispetto a `textPs=`. Ad esempio, le sottolineature non hanno lo stesso spessore e posizione e il corsivo sintetizzato viene riprodotto con un angolo leggermente diverso. Se il testo non rientra nello spazio disponibile, `text=` può ritagliare parzialmente l’ultima riga, mentre `textPs=` esegue il rendering solo delle linee complete.

Tutti i comandi di testo accettano testo formattato in base a un sottoinsieme della specifica RTF (Rich Text Format). Ogni livello di testo può specificare un comando di testo diverso.

Nella tabella seguente sono elencate le funzioni chiave disponibili per ogni comando di testo:

<table id="table_9C41CBDA94C24805B538E5049B0137C6"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> Funzione</b> </th> 
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
   <td> <p>Flusso del testo in forme arbitrarie </p> </td> 
   <td> <p>no </p> </td> 
   <td> <p>sì </p> </td> 
   <td> <p>textFlowPath=, textFlowXPath= </p> </td> 
  </tr> 
  <tr> 
   <td> <p>Flusso del testo lungo percorsi arbitrari </p> </td> 
   <td> <p>no </p> </td> 
   <td> <p>sì </p> </td> 
   <td> <p>textPath= </p> </td> 
  </tr> 
  <tr> 
   <td> <p>Adattamento copia </p> </td> 
   <td> <p>no </p> </td> 
   <td> <p>sì </p> </td> 
   <td> Adattamento copia <p>, <pre>\copyfit</pre>, <pre>\copyfitlines</pre>, <pre>\copyfitmaxlines</pre> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>Margini casella di testo </p> </td> 
   <td> <p>no </p> </td> 
   <td> <p>sì </p> </td> 
   <td> <p><pre>\margl</pre>, <pre>\margr</pre>, <pre>\margt</pre>, <pre>\margb</pre> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>Giustificazione completa del paragrafo </p> </td> 
   <td> <p>no </p> </td> 
   <td> <p>sì </p> </td> 
   <td> <p><pre>\qj</pre> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>giustificazione dell'ultima riga </p> </td> 
   <td> <p>no </p> </td> 
   <td> <p>sì </p> </td> 
   <td> <p>\lastql, \lastqr, \lastqc, \lastqj </p> </td> 
  </tr> 
  <tr> 
   <td> <p>Rientro paragrafo </p> </td> 
   <td> <p>no </p> </td> 
   <td> <p>sì </p> </td> 
   <td> <p>\fi, \li, \ri </p> </td> 
  </tr> 
  <tr> 
   <td> <p>Testo maiuscoletto e maiuscoletto </p> </td> 
   <td> <p>no </p> </td> 
   <td> <p>sì </p> </td> 
   <td> <p>\caps, \scaps </p> </td> 
  </tr> 
  <tr> 
   <td> <p>Colori Image Serving </p> </td> 
   <td> <p>no </p> </td> 
   <td> <p>sì </p> </td> 
   <td> <p>\*\iscolortbl </p> </td> 
  </tr> 
  <tr> 
   <td> <p>Modalità anti-aliasing multiple </p> </td> 
   <td> <p>no </p> </td> 
   <td> <p>sì </p> </td> 
   <td> <p>textAttr= </p> </td> 
  </tr> 
  <tr> 
   <td> <p>flusso di testo in alto a sinistra/in basso a destra </p> </td> 
   <td> <p>no </p> </td> 
   <td> <p>sì </p> </td> 
   <td> <p>\stextFlow </p> </td> 
  </tr> 
  <tr> 
   <td> <p>Supporto di Photofont® </p> </td> 
   <td> <p>no </p> </td> 
   <td> <p>sì </p> </td> 
   <td> Gestione font </td> 
  </tr> 
  <tr> 
   <td> <p>Ridimensionamento automatico del livello per adattare il testo </p> </td> 
   <td> <p>sì </p> </td> 
   <td> <p>sì </p> </td> 
   <td> <p>text=, textId=, size= </p> </td> 
  </tr> 
  <tr> 
   <td> <p>Supporto CMYK </p> </td> 
   <td> <p>sì </p> </td> 
   <td> <p>sì </p> </td> 
   <td> <p>\cmykcolortbl, \*\iscolortbl </p> </td> 
  </tr> 
  <tr> 
   <td> <p>Flusso dei caratteri da destra a sinistra </p> </td> 
   <td> <p>sì </p> </td> 
   <td> <p>no </p> </td> 
   <td> <p>\rtlch </p> </td> 
  </tr> 
  <tr> 
   <td> <p>Disattiva ritorno a capo automatico </p> </td> 
   <td> <p>sì </p> </td> 
   <td> <p>no </p> </td> 
   <td> <p>textAttr= </p> </td> 
  </tr> 
  <tr> 
   <td> <p>Scala automatica del testo per adattarlo al livello (con risoluzione variabile) </p> </td> 
   <td> <p>sì </p> </td> 
   <td> <p>no </p> </td> 
   <td> <p>textAttr= </p> </td> 
  </tr> 
 </tbody> 
</table>

Le stringhe conformi a RTF possono essere assemblate manualmente o formattando il testo desiderato in un editor di testo o un elaboratore di testi in grado di salvare file RTF. Il file RTF può quindi essere aperto in un editor di testo normale e il relativo contenuto RTF non elaborato del file copiato nell&#39;URL della richiesta.

Alcuni elaboratori di testi generano file piuttosto grandi, che includono prerequisiti sostanziali che non vengono utilizzati da Dynamic Media Image Serving. Si consiglia di rimuovere gli elementi RTF non utilizzati dalla stringa prima di passare la stringa ai comandi di testo.

La codifica della lingua basata sugli standard UTF-8 e ISO è supportata nelle stringhe RTF come alternativa ai meccanismi standard di codifica dei caratteri RTF. Questo consente alle applicazioni di inviare testo non inglese al server senza conoscere la codifica RTF.

Tutti i caratteri non conformi a HTTP devono essere correttamente preceduti dalla sequenza di escape se la stringa deve essere trasmessa tramite http. È necessario eseguire l’escape solo &#39;=&#39;, &#39;&amp;&#39; e &#39;%&#39; se la stringa è incorporata nel campo `catalog::Modifiers` di un record di catalogo immagini. I caratteri di controllo, compresi `<CR>`, `<LF>` e `<TAB>`, devono sempre essere rimossi.

I motori di testo Image Serving interpretano un sottoinsieme di comandi definiti dalla specifica Rich Text Format (RTF), versione 1.6. Questo sottoinsieme si concentra sulla formattazione di font/caratteri, la formattazione semplice dei paragrafi e il supporto per i font e i set di caratteri internazionali. Al momento non sono supportati i costrutti di formattazione più avanzati, ad esempio fogli di stile e tabelle.

La familiarità con la specifica RTF (Rich Text Format), come pubblicata da Microsoft, è necessaria quando si tenta di creare manualmente stringhe di testo codificate in RTF.

* [Gestione dei font](r-font-handling.md)
* [Trattamento del colore](r-color-handling.md)
* [Adattamento copia](r-copy-fitting.md)
* [Livelli di testo](r-text-layers.md)
* [Posizionamento del testo](r-text-positioning.md)
* [Caratteri riservati](r-reserved-characters.md)
* [Comandi e parole chiave RTF supportati](c-supported-rtf-commands-and-keywords/c-supported-rtf-commands-and-keywords.md)
* [Esempi di codifica RTF](r-rtf-encoding-examples.md)
