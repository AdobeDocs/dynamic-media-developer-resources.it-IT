---
description: Image Server offre diverse alternative per il rendering del testo, accessibili con i comandi text= e textPs=.
solution: Experience Manager
title: Formattazione testo
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 2c120ed1-b556-4caf-a30e-63ae48cc2104
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '557'
ht-degree: 0%

---

# Formattazione testo{#text-formatting}

Image Server offre diverse alternative per il rendering del testo, accessibili con i comandi text= e textPs=.

`textPs=` offre un livello elevato di somiglianza con il testo renderizzato con Adobe Photoshop e Illustrator. `text=` è ragionevolmente compatibile con il testo sottoposto a rendering con Windows Wordpad.

>[!NOTE]
>
>Oltre alle differenze elencate altrove, `text=` produce lievi differenze nel testo sottoposto a rendering quando confrontato con `textPs=`. Ad esempio, le sottolineature non hanno lo stesso spessore e la stessa posizione e il corsivo sintetizzato viene visualizzato con un angolo leggermente diverso. Se il testo non rientra nello spazio disponibile, `text=` può ritagliare parzialmente l’ultima riga, mentre `textPs=` eseguirà il rendering solo delle righe complete.

Tutti i comandi di testo accettano testo formattato in base a un sottoinsieme della specifica RTF (Rich Text Format). Ogni livello di testo può specificare un comando di testo diverso.

Nella tabella seguente sono elencate le funzioni chiave disponibili per ogni comando di testo:

<table id="table_9C41CBDA94C24805B538E5049B0137C6"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> Funzionalità</b> </th> 
   <th class="entry"> <b> text= Testo</b> </th> 
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
   <td> <p>Trasferisci il testo in forme arbitrarie </p> </td> 
   <td> <p>no </p> </td> 
   <td> <p>sì </p> </td> 
   <td> <p>textFlowPath=, textFlowXPath= </p> </td> 
  </tr> 
  <tr> 
   <td> <p>Spostamento del testo lungo percorsi arbitrari </p> </td> 
   <td> <p>no </p> </td> 
   <td> <p>sì </p> </td> 
   <td> <p>textPath= </p> </td> 
  </tr> 
  <tr> 
   <td> <p>Raccordo </p> </td> 
   <td> <p>no </p> </td> 
   <td> <p>sì </p> </td> 
   <td> Raccordo di copia <p>, <pre>\copyfit</pre>, <pre>\copyfitlines</pre>, <pre>\copyfitmaxlines</pre> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>Margini casella di testo </p> </td> 
   <td> <p>no </p> </td> 
   <td> <p>sì </p> </td> 
   <td> <p><pre>\margl</pre>, <pre>\margr</pre>, <pre>\margt</pre>, <pre>\margb</pre> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>Motivazione paragrafo completa </p> </td> 
   <td> <p>no </p> </td> 
   <td> <p>sì </p> </td> 
   <td> <p><pre>\qj</pre> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>giustificazione dell’ultima riga </p> </td> 
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
   <td> <p>Testo in maiuscoletto e maiuscoletto </p> </td> 
   <td> <p>no </p> </td> 
   <td> <p>sì </p> </td> 
   <td> <p>\caps, \scaps </p> </td> 
  </tr> 
  <tr> 
   <td> <p>Colori Image Server </p> </td> 
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
   <td> <p>flusso di testo in alto-basso/destra-sinistra </p> </td> 
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
   <td> <p>Adatta automaticamente il livello al testo </p> </td> 
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
   <td> <p>Flusso di caratteri da destra a sinistra </p> </td> 
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
   <td> <p>Ridimensiona automaticamente il testo per adattarlo al livello (variando la risoluzione) </p> </td> 
   <td> <p>sì </p> </td> 
   <td> <p>no </p> </td> 
   <td> <p>textAttr= </p> </td> 
  </tr> 
 </tbody> 
</table>

Le stringhe compatibili con RTF possono essere assemblate manualmente o formattando il testo desiderato in un editor di testo o un elaboratore di testi in grado di salvare file RTF. Il file RTF può quindi essere aperto in un editor di testo normale e il relativo contenuto RTF non elaborato del file copiato nell’URL della richiesta.

Alcuni elaboratori di testi generano file piuttosto grandi, che includono preamboli sostanziali che non vengono utilizzati da Dynamic Media Image Server. Si consiglia di rimuovere dalla stringa gli elementi RTF inutilizzati prima di passare la stringa ai comandi di testo.

La codifica del linguaggio basata sugli standard UTF-8 e ISO è supportata nelle stringhe RTF in alternativa ai meccanismi di codifica dei caratteri RTF standard. Ciò consente alle applicazioni di inviare al server testo non in inglese senza conoscere la codifica RTF.

Se la stringa deve essere trasmessa tramite HTTP, tutti i caratteri non conformi HTTP devono avere un escape corretto. Solo &#39;=&#39;, &#39;&amp;&#39; e &#39;%&#39; devono avere un escape se la stringa è incorporata nel `catalog::Modifiers` di un record di catalogo immagini. Caratteri di controllo, inclusi `<CR>`, `<LF>`, e `<TAB>` devono essere sempre rimossi.

I motori di testo Image Server interpretano un sottoinsieme di comandi definiti dalle specifiche RTF (Rich Text Format), versione 1.6. Questo sottoinsieme si concentra sulla formattazione di font/caratteri, sulla formattazione di paragrafo semplice e sul supporto di font e set di caratteri internazionali. I costrutti di formattazione più avanzati, ad esempio i fogli di stile e le tabelle, non sono attualmente supportati.

Quando si tenta di creare manualmente stringhe di testo con codifica RTF, è necessaria la familiarità con la specifica RTF (Rich Text Format) pubblicata da Microsoft.

* [Gestione caratteri](r-font-handling.md)
* [Trattamento del colore](r-color-handling.md)
* [Raccordo](r-copy-fitting.md)
* [Livelli di testo](r-text-layers.md)
* [Posizionamento testo](r-text-positioning.md)
* [Caratteri riservati](r-reserved-characters.md)
* [Comandi e parole chiave RTF supportati](c-supported-rtf-commands-and-keywords/c-supported-rtf-commands-and-keywords.md)
* [Esempi di codifica RTF](r-rtf-encoding-examples.md)
