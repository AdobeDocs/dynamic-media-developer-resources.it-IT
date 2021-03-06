---
description: Tipo di richiesta. Specifica il tipo di richiesta.
solution: Experience Manager
title: req
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 9242c873-5a85-4ede-82b6-4ef15feecf50
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '240'
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
   <td colname="col2"> <p> Restituisce l’elenco xml di tutti gli elementi con un <span class="codeph"> s7:element</span> valore attributo e un elenco di tutte le pagine del documento fxg. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> oversetstatus</span> </p> </td> 
   <td colname="col2"> <p>Restituisce un elenco XML di cui <span class="codeph"> &lt;richtext /&gt;</span> gli elementi non vengono impostati. </p> <p>Restituisce un elenco xml di <span class="+ topic/ph pr-d/codeph codeph"> &lt;richtext /&gt;</span> elementi non impostati per l’elaborazione sul lato client. Solo <span class="+ topic/ph pr-d/codeph codeph"> &lt;richtext /&gt;</span> vengono restituiti gli elementi che sono sovraimpostati. <span class="+ topic/ph pr-d/codeph codeph"> s7:elementid</span> è obbligatorio <span class="+ topic/ph pr-d/codeph codeph"> &lt;richtext /&gt;</span> attributo quando si utilizza <span class="+ topic/ph pr-d/codeph codeph"> req=oversetstatus</span>. Qualsiasi overset <span class="+ topic/ph pr-d/codeph codeph"> &lt;richtext /&gt;</span> elementi senza <span class="+ topic/ph pr-d/codeph codeph"> s7:elementid</span> non è elencato. Ogni <span class="+ topic/ph pr-d/codeph codeph"> &lt;richtext /&gt;</span> l’elemento dell’elenco ha <span class="+ topic/ph pr-d/codeph codeph"> s7:elementid</span>, <span class="+ topic/ph pr-d/codeph codeph"> s7:endCharIndex</span>e il riquadro di delimitazione della cornice di testo non impostata. La <span class="+ topic/ph pr-d/codeph codeph"> s7:endCharIndex</span> attributo indica l'indice di testo nel brano fino a cui il testo è stato in grado di adattarsi alla cornice. <span class="+ topic/ph pr-d/codeph codeph"> Req=oversetstatus</span> si applica solo a <span class="+ topic/ph pr-d/codeph codeph"> &lt;richtext /&gt;</span> elementi nell'FXG richiesto. Non elencherà alcun <span class="+ topic/ph pr-d/codeph codeph"> &lt;richtext /&gt;</span> elementi da qualsiasi FXG incorporato. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> esiste</span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> req=exists[,text|javascript|xml|{json[&amp;id=reqId]}]</span> </p> <p>identificatore univoco della richiesta reqId </p> <p>Restituisce una singola proprietà denominata catalogRecord.exists. Il valore della proprietà è impostato su "1" se la voce di catalogo specificata esiste nell'immagine o nel catalogo predefinito, altrimenti è impostata su "0". le richieste req=exists rispetto al contesto /is/content indicheranno la presenza o l'assenza di un record specificato nel catalogo dei contenuti statici. </p> </td> 
  </tr> 
 </tbody> 
</table>
