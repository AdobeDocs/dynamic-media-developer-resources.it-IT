---
title: req
description: Tipo di richiesta. Specifica il tipo di richiesta.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 9242c873-5a85-4ede-82b6-4ef15feecf50
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '245'
ht-degree: 0%

---

# req{#req}

Tipo di richiesta. Specifica il tipo di richiesta.

`req={validate|contents|oversetstatus|exists}`

<table id="table_F39239E5244746DB9F253BB0D5E85D54"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Valore </th> 
   <th colname="col2" class="entry"> Descrizione </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> convalida</span> </p> </td> 
   <td colname="col2"> <p> Restituisce eventuali errori di rendering del file FXG con i modificatori URL forniti. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> contenuto</span> </p> </td> 
   <td colname="col2"> <p> Restituisce un elenco xml di tutti gli elementi con un valore di attributo <span class="codeph"> s7:element</span> e un elenco di tutte le pagine del documento FXG. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> oversetstatus</span> </p> </td> 
   <td colname="col2"> <p>Restituisce un elenco XML di cui <span class="codeph"> &lt;RichText/&gt;</span> elementi sono sovrascritti. </p> <p>Restituisce un elenco XML di <span class="+ topic/ph pr-d/codeph codeph"> &lt;RichText/&gt;</span> elementi non impostati per l'elaborazione sul lato client. Vengono restituiti solo <span class="+ topic/ph pr-d/codeph codeph"> &lt;RichText/&gt;</span> elementi non impostati. <span class="+ topic/ph pr-d/codeph codeph"> s7:elementid</span> è un attributo <span class="+ topic/ph pr-d/codeph codeph"> &lt;RichText/&gt;</span> obbligatorio quando si utilizza <span class="+ topic/ph pr-d/codeph codeph"> req=oversetstatus</span>. Eventuali elementi <span class="+ topic/ph pr-d/codeph codeph"> &lt;RichText/&gt;</span> non inclusi senza un <span class="+ topic/ph pr-d/codeph codeph"> s7:elementid</span> non sono elencati. Ogni elemento <span class="+ topic/ph pr-d/codeph codeph"> &lt;RichText/&gt;</span> dell'elenco include <span class="+ topic/ph pr-d/codeph codeph"> s7:elementid</span>, <span class="+ topic/ph pr-d/codeph codeph"> s7:endCharIndex</span> e il riquadro di delimitazione della cornice di testo non impostata. L'attributo <span class="+ topic/ph pr-d/codeph codeph"> s7:endCharIndex</span> indica l'indice di testo nel brano fino al quale il testo è stato adattato nella cornice. Il valore Req=oversetstatus <span class="+ topic/ph pr-d/codeph codeph"></span> si applica solo a <span class="+ topic/ph pr-d/codeph codeph"> &lt;RichText/&gt;</span> elementi nel file FXG richiesto. Non elenca alcun elemento <span class="+ topic/ph pr-d/codeph codeph"> &lt;RichText/&gt;</span> da alcun FXG incorporato. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> esiste</span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> req=exists[,text|javascript|xml|{json[&amp;id=reqId]}]</span> </p> <p>Identificatore di richiesta univoco reqId </p> <p>Restituisce una singola proprietà denominata catalogRecord.exists. Il valore della proprietà è impostato su "1" se la voce di catalogo specificata esiste nell'immagine o nel catalogo predefinito, altrimenti è impostato su "0". le richieste req=exists nel contesto /is/content indicano la presenza o l'assenza di un record specificato nel catalogo dei contenuti statici. </p> </td> 
  </tr> 
 </tbody> 
</table>
