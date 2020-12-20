---
description: I materiali di decorazione comprendono costrutti di abbigliamento come appliqués, stampe di t-shirt e loghi ricamati o stampati, nonché oggetti piatti non ripetibili, utilizzati in applicazioni interne o esterne, come tappeti di superficie, disegni appesi a muro, cartelli e così via.
seo-description: I materiali di decorazione comprendono costrutti di abbigliamento come appliqués, stampe di t-shirt e loghi ricamati o stampati, nonché oggetti piatti non ripetibili, utilizzati in applicazioni interne o esterne, come tappeti di superficie, disegni appesi a muro, cartelli e così via.
seo-title: Decorazioni
solution: Experience Manager
title: Decorazioni
topic: Scene7 Image Serving - Image Rendering API
uuid: 6e64f382-f15f-4018-b00c-4fd21a4ebc8c
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '264'
ht-degree: 2%

---


# Decorazioni{#decals}

I materiali di decorazione comprendono costrutti di abbigliamento come appliqués, stampe di t-shirt e loghi ricamati o stampati, nonché oggetti piatti non ripetibili, utilizzati in applicazioni interne o esterne, come tappeti di superficie, disegni appesi a muro, cartelli e così via.

Un materiale è considerato un decallo se specificato in un MSS decal. Un decal è in genere un’immagine RGBA, con il canale alfa che definisce la forma del decallo.

È possibile applicare un decallo a ciascun oggetto piano, a linee scorrevoli, a sketch, a piano o a parete (a meno che non sia impostato il flag &#39;Nessuna texture&#39;). Le decimali vengono applicate all&#39;oggetto allineando il decal `anchor=` con il punto di origine decal dell&#39;oggetto vignettatura. La posizione può essere regolata ulteriormente con `pos=`.

Viene eseguito il rendering di un&#39;ombra esterna se il materiale di decallo definisce uno spessore e l&#39;oggetto vignettatura definisce un vettore chiaro.

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
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-src.md#reference-62c98abad22149d68d405ed6aaff8272" type="reference" format="dita" scope="local"> <span class="codeph"> src=  </span> </a> </p> </td> 
   <td colname="col2"> <p>Immagine (in genere con alfa); obbligatorio. </p> </td> 
   <td colname="col3"> <p>Nessuno. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-size.md#reference-1220d6fbcde4479aba91de7adacdc988" type="reference" format="dita" scope="local"> <span class="codeph"> size=  </span> </a> </p> </td> 
   <td colname="col2"> <p>Larghezza, altezza e spessore del carrello (per l’ombra esterna). </p> </td> 
   <td colname="col3"> <p> <span class="varname"> imageWidth  </span> x  <span class="codeph"> res  </span>,  <span class="varname"> imageHeight  </span> x  <span class="codeph"> res, 0  </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-res.md#reference-0ad9de8887144c83a6db97b4994f7c04" type="reference" format="dita" scope="local"> <span class="codeph"> res=  </span> </a> </p> </td> 
   <td colname="col2"> <p>Risoluzione texture (ignorata se è specificata la dimensione=). </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> attribute:Resolution  </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-anchor.md#reference-d53923d785c9442997dc7f2199524c26" type="reference" format="dita" scope="local"> <span class="codeph"> anchor=  </span> </a> </p> </td> 
   <td colname="col2"> <p>Punto di allineamento della scala. </p> </td> 
   <td colname="col3"> <p>Centro immagini. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-pos.md#reference-22c10904a0ce4c8bb41c2c78104221b8" type="reference" format="dita" scope="local"> <span class="codeph"> pos=  </span> </a> </p> </td> 
   <td colname="col2"> <p>Posizione relativa del decallo. </p> </td> 
   <td colname="col3"> <p>0, 0 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-opac.md#reference-136b8563da714313a9e103f4ce179c5b" type="reference" format="dita" scope="local"> <span class="codeph"> opac=  </span> </a> </p> </td> 
   <td colname="col2"> <p>Opacità decale. </p> </td> 
   <td colname="col3"> <p>100% </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-sharp.md#reference-acdd87f6b5de4e3a85e5d3c03022a35a" type="reference" format="dita" scope="local"> <span class="codeph"> sharp=  </span> </a> </td> 
   <td colname="col2"> <p>Opzioni. </p> </td> 
   <td colname="col3"> <p>0 (nessuna nitidezza) </p> </td> 
  </tr> 
 </tbody> 
</table>

