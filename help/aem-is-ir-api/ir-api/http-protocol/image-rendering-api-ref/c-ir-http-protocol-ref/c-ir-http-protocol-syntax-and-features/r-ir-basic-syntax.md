---
title: Sintassi di base del protocollo HTTP Image Rendering
description: Questa sezione descrive la sintassi di base del protocollo HTTP Dynamic Media Image Rendering.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 8bf5920a-7ada-4db5-9796-05c5a17532c8
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '224'
ht-degree: 1%

---

# Sintassi di base del protocollo HTTP Image Rendering{#image-rendering-http-protocol-basic-syntax}

Questa sezione descrive la sintassi di base del protocollo HTTP Dynamic Media Image Rendering.

<table id="table_0A7D7207EE6D4B08B62BE8620EBE0B25"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Elemento </p> </th> 
   <th colname="col2" class="entry"> <p>Definizione </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> richiesta</span> </p> </td> 
   <td colname="col2"> <p>http://<span class="varname"> server</span>/ir/render[/<span class="varname"> vignetta</span> ] [ ?<span class="varname"> modificatori</span> ] </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> server </span> </p> </td> 
   <td colname="col2"> <p><span class="varname"> indirizzo_server</span> [ :<span class="varname"> porta</span> ] </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> vignetta </span> </p> </td> 
   <td colname="col2"> <p>Identificatore di vignetta (percorso relativo del file o voce di catalogo di vignetta). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> modificatori </span> </p> </td> 
   <td colname="col2"> <p><span class="varname"> modifier</span> *[ &amp; <span class="varname"> modifier</span> ] </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> modificatore </span> </p> </td> 
   <td colname="col2"> <p><span class="varname"> command</span> | { $ <span class="varname"> macro</span> $ } | { .<span class="varname"> commento</span> } </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> command </span> </p> </td> 
   <td colname="col2"> <p>{ <span class="varname"> cmdName</span> | { $<span class="varname"> var</span> } [ = <span class="varname"> value</span> ] </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> macro </span> </p> </td> 
   <td colname="col2"> <p>Nome di una macro di comando. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> commento </span> </p> </td> 
   <td colname="col2"> <p>Stringa di commento (ignorata dal server). </p> </td> 
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
   <td colname="col2"> <p>Valore di comando o variabile. </p> </td> 
  </tr> 
 </tbody> 
</table>

*`server`*, *`cmdName`*, *`macro`* e *`var`* sono senza distinzione tra maiuscole e minuscole. Il server conserva il caso di tutti gli altri valori di stringa.

**Identificatore server**

Il `/ir/render`Il contesto radice ?? necessario per tutte le richieste HTTP al rendering delle immagini.

**Commenti**

I commenti possono essere incorporati nelle stringhe di richiesta in qualsiasi punto e sono identificati da un punto (.) subito dopo il separatore di comando (&amp;). Il commento viene terminato dall&#39;occorrenza successiva di un separatore di comando (non codificato). Questa funzione pu?? essere utilizzata per aggiungere informazioni alla richiesta che non sono per l???uso di Image Serving, ad esempio timestamp e ID del database.

**decodifica HTTP**

Rendering immagine - primi estratti *`object`* e *`modifiers`* dalla richiesta in arrivo. La *`object`* viene quindi separato in elementi di percorso che sono singolarmente decodificati tramite HTTP. La *`modifiers`* stringa separata in *`command`*= *`value`* coppie, e *`value`* viene quindi decodificato per HTTP prima dell&#39;elaborazione specifica del comando.
