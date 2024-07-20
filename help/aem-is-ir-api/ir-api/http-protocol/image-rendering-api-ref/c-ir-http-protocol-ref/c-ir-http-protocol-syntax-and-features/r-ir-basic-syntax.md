---
title: Sintassi di base del protocollo HTTP Image Rendering
description: In questa sezione viene descritta la sintassi di base del protocollo HTTP Dynamic Medie Image Rendering.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 8bf5920a-7ada-4db5-9796-05c5a17532c8
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '226'
ht-degree: 0%

---

# Sintassi di base del protocollo HTTP Image Rendering{#image-rendering-http-protocol-basic-syntax}

In questa sezione viene descritta la sintassi di base del protocollo HTTP Dynamic Medie Image Rendering.

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
   <td colname="col2"> <p>http://<span class="varname"> server</span>/ir/render[/<span class="varname"> vignettatura</span> ] [ ?<span class="varname"> modificatori</span> ] </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> server </span> </p> </td> 
   <td colname="col2"> <p><span class="varname"> indirizzo_server</span> [ :<span class="varname"> porta</span> ] </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> vignettatura </span> </p> </td> 
   <td colname="col2"> <p>Identificatore vignettatura (percorso relativo del file o voce del catalogo vignettatura). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> modificatori </span> </p> </td> 
   <td colname="col2"> <p><span class="varname"> modificatore</span> *[ &amp; <span class="varname"> modificatore</span> ] </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Modificatore <span class="varname"> </span> </p> </td> 
   <td colname="col2"> <p>Comando <span class="varname"></span> | { $ <span class="varname"> macro</span> $ } | { .<span class="varname"> commento</span> } </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Comando <span class="varname"> </span> </p> </td> 
   <td colname="col2"> <p>{ <span class="varname"> cmdName</span> | { $<span class="varname"> var</span> } } [ = <span class="varname"> valore</span> ] </p> </td> 
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
   <td colname="col2"> <p>Nome di un comando o attributo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> var </span> </p> </td> 
   <td colname="col2"> <p>Nome di una variabile personalizzata. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> valore </span> </p> </td> 
   <td colname="col2"> <p>Valore del comando o della variabile. </p> </td> 
  </tr> 
 </tbody> 
</table>

*`server`*, *`cmdName`*, *`macro`* e *`var`* non distinguono tra maiuscole e minuscole. Il server mantiene le maiuscole e minuscole di tutti gli altri valori stringa.

**Identificatore server**

Il contesto radice &#39;`/ir/render`&#39; è necessario per tutte le richieste HTTP a Image Rendering.

**Commenti**

I commenti possono essere incorporati nelle stringhe di richiesta ovunque e sono identificati da un punto (.) immediatamente dopo il separatore di comandi (&amp;). Il commento viene terminato dall&#39;occorrenza successiva di un separatore di comando (non codificato). Questa funzione può essere utilizzata per aggiungere informazioni alla richiesta che non sono destinate all’utilizzo in Image Server, ad esempio timestamp e ID di database.

**Decodifica HTTP**

Image Rendering estrae prima *`object`* e *`modifiers`* dalla richiesta in ingresso. *`object`* è quindi separato in elementi percorso che sono singolarmente decodificati HTTP. La stringa *`modifiers`* è separata in *`command`*= *`value`* coppie e *`value`* viene quindi decodificato HTTP prima dell&#39;elaborazione specifica del comando.
