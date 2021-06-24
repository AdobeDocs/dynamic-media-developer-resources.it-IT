---
description: Questa sezione descrive la sintassi di base del protocollo HTTP Dynamic Media Image Rendering.
solution: Experience Manager
title: Sintassi di base del protocollo HTTP Image Rendering
feature: Dynamic Media Classic, SDK/API
role: Developer,Business Practitioner
exl-id: 8bf5920a-7ada-4db5-9796-05c5a17532c8
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '228'
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
   <td colname="col1"> <p><span class="varname"> server  </span> </p> </td> 
   <td colname="col2"> <p><span class="varname"> server_address</span> [:<span class="varname"> port</span> ] </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> vignetta  </span> </p> </td> 
   <td colname="col2"> <p>Identificatore di vignetta (percorso relativo del file o voce di catalogo di vignetta). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> modificatori  </span> </p> </td> 
   <td colname="col2"> <p><span class="varname"> modificatore</span> *[ e  <span class="varname"> modificatore</span> ] </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> modificatore </span> </p> </td> 
   <td colname="col2"> <p><span class="varname"> comando</span> | { $  <span class="varname"> macro</span> $ } | { .<span class="varname"> commento</span> } </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> command  </span> </p> </td> 
   <td colname="col2"> <p>{ <span class="varname"> cmdName</span> | { $<span class="varname"> var</span> } [ = <span class="varname"> valore</span> ] </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> macro  </span> </p> </td> 
   <td colname="col2"> <p>Nome di una macro di comando. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> commento  </span> </p> </td> 
   <td colname="col2"> <p>Stringa di commento (ignorata dal server). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> cmdName  </span> </p> </td> 
   <td colname="col2"> <p>Nome di un comando o di un attributo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> var  </span> </p> </td> 
   <td colname="col2"> <p>Nome di una variabile personalizzata. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> value  </span> </p> </td> 
   <td colname="col2"> <p>Valore di comando o variabile. </p> </td> 
  </tr> 
 </tbody> 
</table>

*`server`*,  *`cmdName`*,  *`macro`* e  *`var`* sono senza distinzione tra maiuscole e minuscole. Il server conserva il caso di tutti gli altri valori stringa.

**Identificatore server**

Il contesto radice &#39; `/ir/render`&#39; è necessario per tutte le richieste HTTP al Image Rendering.

**Commenti**

I commenti possono essere incorporati nelle stringhe di richiesta in qualsiasi punto e sono identificati da un punto (.) subito dopo il separatore di comando (&amp;). Il commento viene terminato dall&#39;occorrenza successiva di un separatore di comando (non codificato). Questa funzione può essere utilizzata per aggiungere informazioni alla richiesta che non sono per l&#39;uso di Image Server, come timestamp, ID del database, ecc.

**decodifica HTTP**

Image Rendering estrae prima *`object`* e *`modifiers`* dalla richiesta in arrivo. *`object`* viene quindi separato in elementi di percorso che sono singolarmente decodificati tramite HTTP. La stringa *`modifiers`* è separata in coppie *`command`*= *`value`* e *`value`* viene quindi decodificata per HTTP prima dell&#39;elaborazione specifica del comando.
