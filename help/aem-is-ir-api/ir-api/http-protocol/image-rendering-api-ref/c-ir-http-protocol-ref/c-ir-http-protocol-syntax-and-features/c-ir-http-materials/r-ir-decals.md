---
title: Decalcomania
description: I materiali delle decalcomanie includono costrutti di abbigliamento come appliqués, stampe di t-shirt e loghi ricamati o stampati. Include anche oggetti piatti non ripetibili utilizzati in applicazioni interne o esterne, come tappeti, appesi alle pareti e segni.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 07190abd-9f6f-46b5-bf77-cd97c48fc9be
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '225'
ht-degree: 1%

---

# Decalcomania{#decals}

I materiali delle decalcomanie includono costrutti di abbigliamento come appliqués, stampe di t-shirt e loghi ricamati o stampati. Include anche oggetti piatti non ripetibili utilizzati in applicazioni interne o esterne, come tappeti, appesi alle pareti e segni.

Un materiale è considerato una decalcomania se è specificato in una decalcomania MSS. Una decalcomania è tipicamente un&#39;immagine RGBA, con il canale alfa che definisce la forma della decalcomania.

È possibile applicare una decalcomania a ogni oggetto piatto, linea di flusso, sketch, piano o parete (a meno che non sia impostato il flag &#39;No Texture&#39;). Le decalcomanie vengono applicate all&#39;oggetto allineando `anchor=` della decalcomania al punto di origine della decalcomania dell&#39;oggetto di vignettatura. La posizione può essere ulteriormente regolata con `pos=`.

Se il materiale della decalcomania definisce uno spessore e l&#39;oggetto di vignettatura definisce un vettore di luce, viene riprodotta un&#39;ombra esterna.

<table id="table_3F119BC9B7654FD092826A34F5827268"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Attributo </p> </th> 
   <th colname="col2" class="entry"> <p>Descrizione </p> </th> 
   <th colname="col3" class="entry"> <p>Predefinito </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-src.md#reference-62c98abad22149d68d405ed6aaff8272" type="reference" format="dita" scope="local"> <span class="codeph"> src= </span> </a> </p> </td> 
   <td colname="col2"> <p>Immagine (in genere con alfa); obbligatoria. </p> </td> 
   <td colname="col3"> <p>Nessuno. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> Dimensione <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-size.md#reference-1220d6fbcde4479aba91de7adacdc988" type="reference" format="dita" scope="local"> <span class="codeph">= </span> </a> </p> </td> 
   <td colname="col2"> <p>Larghezza decalcomania, altezza e spessore (per ombra esterna). </p> </td> 
   <td colname="col3"> <p> <span class="varname"> imageWidth </span> x <span class="codeph"> res </span>, <span class="varname"> imageHeight </span> x <span class="codeph"> res, 0 </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-res.md#reference-0ad9de8887144c83a6db97b4994f7c04" type="reference" format="dita" scope="local"> <span class="codeph"> res= </span> </a> </p> </td> 
   <td colname="col2"> <p>Risoluzione della trama (ignorata se è specificato size=). </p> </td> 
   <td colname="col3"> <p> Attributo <span class="codeph">::Risoluzione </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> Ancoraggio <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-anchor.md#reference-d53923d785c9442997dc7f2199524c26" type="reference" format="dita" scope="local"> <span class="codeph">= </span> </a> </p> </td> 
   <td colname="col2"> <p>Decalca il punto di allineamento. </p> </td> 
   <td colname="col3"> <p>Centro immagini. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-pos.md#reference-22c10904a0ce4c8bb41c2c78104221b8" type="reference" format="dita" scope="local"> <span class="codeph"> pos= </span> </a> </p> </td> 
   <td colname="col2"> <p>Posizione relativa della decalcomania. </p> </td> 
   <td colname="col3"> <p>0, 0 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-opac.md#reference-136b8563da714313a9e103f4ce179c5b" type="reference" format="dita" scope="local"> <span class="codeph"> opac= </span> </a> </p> </td> 
   <td colname="col2"> <p>Opacità decalcomania. </p> </td> 
   <td colname="col3"> <p>100% </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-sharp.md#reference-acdd87f6b5de4e3a85e5d3c03022a35a" type="reference" format="dita" scope="local"> <span class="codeph"> sharp= </span> </a> </td> 
   <td colname="col2"> <p>Nitidezza. </p> </td> 
   <td colname="col3"> <p>0 (nessuna nitidezza) </p> </td> 
  </tr> 
 </tbody> 
</table>
