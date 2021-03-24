---
description: Tipo di richiesta. Specifica il tipo di richiesta.
solution: Experience Manager
title: req
feature: Dynamic Media Classic, SDK/API
role: Sviluppatore, Business Practices
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '249'
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
   <td colname="col1"> <p> <span class="codeph"> validate</span> </p> </td> 
   <td colname="col2"> <p> Restituisce eventuali errori durante il rendering della fxg con i modificatori url forniti. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> sommario</span> </p> </td> 
   <td colname="col2"> <p> Restituisce l'elenco xml di tutti gli elementi con un valore di attributo <span class="codeph"> s7:element</span> e un elenco di tutte le pagine del documento fxg. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> oversetstatus</span> </p> </td> 
   <td colname="col2"> <p>Restituisce un elenco XML di cui gli elementi <span class="codeph"> &lt;RichText/&gt;</span> sono sovraimpostati. </p> <p>Restituisce un elenco xml di elementi <span class="+ topic/ph pr-d/codeph codeph"> &lt;RichText/&gt;</span> che vengono impostati per l'elaborazione sul lato client. Verranno restituiti solo gli elementi <span class="+ topic/ph pr-d/codeph codeph"> &lt;RichText/&gt;</span> che sono stati superati. <span class="+ topic/ph pr-d/codeph codeph"> s7:</span> elementidis un  <span class="+ topic/ph pr-d/codeph codeph"> &lt;richtext /&gt;</span> attributo obbligatorio quando si utilizza  <span class="+ topic/ph pr-d/codeph codeph"> req=oversetstatus</span>. Non sono elencati gli elementi sovraimpostati <span class="+ topic/ph pr-d/codeph codeph"> &lt;RichText/&gt;</span> senza <span class="+ topic/ph pr-d/codeph codeph"> s7:elementid</span>. Ogni elemento <span class="+ topic/ph pr-d/codeph codeph"> &lt;RichText/&gt;</span> dell’elenco ha il <span class="+ topic/ph pr-d/codeph codeph"> s7:elementid</span>, <span class="+ topic/ph pr-d/codeph codeph"> s7:endCharIndex</span> e il riquadro di delimitazione della cornice di testo non impostata. L'attributo <span class="+ topic/ph pr-d/codeph codeph"> s7:endCharIndex</span> indica l'indice di testo nel brano fino al quale il testo è stato in grado di adattarsi alla cornice. <span class="+ topic/ph pr-d/codeph codeph"> Req=</span> oversetstatusonly si applica agli  <span class="+ topic/ph pr-d/codeph codeph"> &lt;richtext /&gt;</span> elementi nell'FXG richiesto. Non elencherà alcun elemento <span class="+ topic/ph pr-d/codeph codeph"> &lt;RichText/&gt;</span> da alcun FXG incorporato. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> esiste</span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> req=exists[,text|javascript|xml|{json[&amp;id=reqId]}]</span> </p> <p>identificatore univoco della richiesta reqId </p> <p>Restituisce una singola proprietà denominata catalogRecord.exists. Il valore della proprietà è impostato su "1" se la voce di catalogo specificata esiste nell'immagine o nel catalogo predefinito, altrimenti è impostata su "0". le richieste req=exists rispetto al contesto /is/content indicheranno la presenza o l'assenza di un record specificato nel catalogo dei contenuti statici. </p> </td> 
  </tr> 
 </tbody> 
</table>

