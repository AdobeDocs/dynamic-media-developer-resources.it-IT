---
description: Tipo di richiesta. Specifica il tipo di richiesta.
seo-description: Tipo di richiesta. Specifica il tipo di richiesta.
seo-title: req
solution: Experience Manager
title: req
topic: Scene7 Image Serving - Image Rendering API
uuid: 1c8ff9c3-9f39-46a8-bd38-8e0c5ab0f548
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

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
   <td colname="col2"> <p> Restituisce eventuali errori durante il rendering del file fxg con i modificatori url forniti. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> contents</span> </p> </td> 
   <td colname="col2"> <p> Restituisce un elenco xml di tutti gli elementi con un valore attributo <span class="codeph"> s7:element</span> e un elenco di tutte le pagine del documento fxg. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> overversetstatus</span> </p> </td> 
   <td colname="col2"> <p>Restituisce un elenco XML di cui gli elementi <span class="codeph"> &lt;RichText/&gt;</span> sono impostati come non inseriti. </p> <p>Restituisce un elenco xml di elementi <span class="+ topic/ph pr-d/codeph codeph"> &lt;RichText/&gt;</span> che vengono impostati in modo non corretto per l'elaborazione sul lato client. Verranno restituiti solo gli elementi <span class="+ topic/ph pr-d/codeph codeph"> &lt;RichText/&gt;</span> che sono impostati come non inseriti. <span class="+ topic/ph pr-d/codeph codeph"> s7:elementid</span> è un attributo <span class="+ topic/ph pr-d/codeph codeph"> &lt;RichText/&gt;</span> obbligatorio quando si utilizza <span class="+ topic/ph pr-d/codeph codeph"> req=overetstatus</span>. Eventuali elementi non inseriti <span class="+ topic/ph pr-d/codeph codeph"> &lt;RichText/&gt;</span> senza un elemento <span class="+ topic/ph pr-d/codeph codeph"> s7:elementid</span> non sono elencati. Ogni elemento <span class="+ topic/ph pr-d/codeph codeph"> &lt;RichText/&gt;</span> presente nell'elenco ha <span class="+ topic/ph pr-d/codeph codeph"> s7:elementid</span>, <span class="+ topic/ph pr-d/codeph codeph"> s7:endCharIndex</span>e il rettangolo di selezione della cornice di testo non inserita. L’attributo <span class="+ topic/ph pr-d/codeph codeph"> s7:endCharIndex</span> indica l’indice di testo nel brano fino al quale il testo è stato adattato alla cornice. <span class="+ topic/ph pr-d/codeph codeph"> Req=oversetstatus</span> si applica solo agli elementi <span class="+ topic/ph pr-d/codeph codeph"> &lt;RichText/&gt;</span> nel file FXG richiesto. Non elenca alcun elemento <span class="+ topic/ph pr-d/codeph codeph"> &lt;RichText/&gt;</span> di FXG incorporati. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> exists</span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> req=exists[,testo|javascript|xml|{json[&amp;id=reqId]}]</span> </p> <p>identificatore univoco della richiesta reqId </p> <p>Restituisce una singola proprietà denominata catalogRecord.exists. Il valore della proprietà è impostato su "1" se la voce di catalogo specificata esiste nel catalogo predefinito o dell'immagine, altrimenti è impostata su "0". le richieste req=exists rispetto al contesto /is/content indicheranno la presenza o l'assenza di un record specificato nel catalogo dei contenuti statici. </p> </td> 
  </tr> 
 </tbody> 
</table>

