---
description: Questa sezione descrive la sintassi di base del protocollo HTTP Scene7 Image Rendering.
seo-description: Questa sezione descrive la sintassi di base del protocollo HTTP Scene7 Image Rendering.
seo-title: Sintassi di base del protocollo HTTP Image Rendering
solution: Experience Manager
title: Sintassi di base del protocollo HTTP Image Rendering
topic: Scene7 Image Serving - Image Rendering API
uuid: e01314f0-6aaa-41ca-8c05-d5db3148a071
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Sintassi di base del protocollo HTTP Image Rendering{#image-rendering-http-protocol-basic-syntax}

Questa sezione descrive la sintassi di base del protocollo HTTP Scene7 Image Rendering.

<table id="table_0A7D7207EE6D4B08B62BE8620EBE0B25"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Elemento </p> </th> 
   <th colname="col2" class="entry"> <p>Definizione </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> request</span> </p> </td> 
   <td colname="col2"> <p>http://<span class="varname"> server</span>/ir/rendering[/<span class="varname"> vignettatura</span> ] [ ?<span class="varname"> modificatori</span> ] </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> server </span> </p> </td> 
   <td colname="col2"> <p><span class="varname"> server_address</span> [ :<span class="varname"> porta</span> ] </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> vignettatura </span> </p> </td> 
   <td colname="col2"> <p>Identificatore di vignettatura (percorso relativo del file o voce del catalogo di vignettatura). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> modificatori </span> </p> </td> 
   <td colname="col2"> <p><span class="varname"> modificatore</span> *[ &amp; <span class="varname"> modificatore</span> ] </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> modificatore </span> </p> </td> 
   <td colname="col2"> <p><span class="varname"> command</span> | { $ <span class="varname"> macro</span> $ }| { .<span class="varname"> comment</span> } </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> command </span> </p> </td> 
   <td colname="col2"> <p>{ <span class="varname"> cmdName</span> | { $<span class="varname"> var</span> } [ = <span class="varname"> valore</span> ] </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> macro </span> </p> </td> 
   <td colname="col2"> <p>Nome di una macro di comandi. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> commento </span> </p> </td> 
   <td colname="col2"> <p>Stringa commento (ignorata dal server). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> cmdName </span> </p> </td> 
   <td colname="col2"> <p>Nome di un comando o di un attributo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> var </span> </p> </td> 
   <td colname="col2"> <p>Nome di una variabile personalizzata. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> value </span> </p> </td> 
   <td colname="col2"> <p>Comando o valore variabile. </p> </td> 
  </tr> 
 </tbody> 
</table>

*`server`*, *`cmdName`*, *`macro`* e *`var`* non fa distinzione tra maiuscole e minuscole. Il server conserva le maiuscole e le minuscole di tutti gli altri valori stringa.

**Identificatore server**

Il contesto principale &#39; `/ir/render`&#39; è richiesto per tutte le richieste HTTP al rendering immagine.

**Commenti**

I commenti possono essere incorporati nelle stringhe di richiesta ovunque e sono identificati da un punto (.) subito dopo il separatore di comando (&amp;). Il commento viene terminato dall&#39;occorrenza successiva di un separatore di comando (non codificato). Questa funzione può essere utilizzata per aggiungere informazioni alla richiesta che non sono utilizzabili per Image Server, come marche temporali, ID del database, ecc.

**decodifica HTTP**

Il rendering delle immagini viene eseguito prima *`object`* e *`modifiers`* dalla richiesta in entrata. *`object`* viene quindi separato in elementi di percorso che sono singolarmente decodificati HTTP. La *`modifiers`* stringa è separata in *`command`*= *`value`* coppie, quindi *`value`* viene decodificata HTTP prima dell&#39;elaborazione specifica per il comando.
