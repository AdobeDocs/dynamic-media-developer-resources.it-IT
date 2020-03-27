---
description: Modalità Adatta immagine risposta Specifica come viene calcolato il fattore di scala, che viene utilizzato per ridimensionare l'immagine composita in base all'immagine di risposta quando la dimensione della risposta è specificata con wid= e hei= e scl= non è presente.
seo-description: Modalità Adatta immagine risposta Specifica come viene calcolato il fattore di scala, che viene utilizzato per ridimensionare l'immagine composita in base all'immagine di risposta quando la dimensione della risposta è specificata con wid= e hei= e scl= non è presente.
seo-title: adatta
solution: Experience Manager
title: adatta
topic: Scene7 Image Serving - Image Rendering API
uuid: 669fe757-f3a1-4cd4-b46c-6fbe5a039ce0
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# adatta{#fit}

Modalità Adatta immagine risposta Specifica come viene calcolato il fattore di scala, che viene utilizzato per ridimensionare l&#39;immagine composita in base all&#39;immagine di risposta quando la dimensione della risposta è specificata con wid= e hei= e scl= non è presente.

` fit= *``*, *`modesta`*`

<table id="simpletable_50FBDC6B7CB2448891DD0F491DEB5ACF"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> modalità </span></span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> fit|vincola|ritaglia|avvolgi|allunga|adatta|vfit </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> upscale </span></span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> 0 | 1 </span> </p> </td> 
 </tr> 
</table>

Nella seguente descrizione delle opzioni di modalità, si presume che *`xScale`* sia il rapporto tra la larghezza dell&#39;immagine composita e la larghezza dell&#39;immagine di risposta e *`yScale`* sia il rapporto tra l&#39;altezza dell&#39;immagine composita e l&#39;altezza dell&#39;immagine di risposta.

<table id="table_33408ECA9D164AFAA249F8589060545E"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Parametro </th> 
   <th colname="col2" class="entry"> Definizione </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> adatta </span> </p> </td> 
   <td colname="col2"> <p>Consente di ridimensionare l'immagine composita in modo che rientri nello spazio allocato con <span class="codeph"> wid= </span> e <span class="codeph"> hei= </span>, con spazi bianchi minimi e nessun ritaglio. L’immagine di risposta avrà le stesse dimensioni specificate con <span class="codeph"> wid= </span> e <span class="codeph"> hei= </span>. Viene applicata la scala <span class="varname"> xScale </span> e la scala <span class="varname"> y minore </span> . </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> vincolare </span> </p> </td> 
   <td colname="col2"> <p>Ridimensiona l’immagine composita come <span class="codeph"> si adatta </span> allo spazio allocato con <span class="codeph"> wid= </span> e <span class="codeph"> hei= </span>, ma l’immagine di risposta effettiva potrebbe essere più piccola di quella specificata con <span class="codeph"> wid= </span> e <span class="codeph"> hei= </span> per evitare spazi bianchi. Viene applicata la scala <span class="varname"> xScale </span> e la scala <span class="varname"> y minore </span> . </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> Ritaglia </span> </p> </td> 
   <td colname="col2"> <p>Consente di ridimensionare l'immagine composita in modo da riempire l'intera immagine di risposta, con un ritaglio minimo e senza spazi bianchi. Viene applicata la dimensione maggiore tra <span class="varname"> Scala </span> x e <span class="varname"> Scala y </span> . </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> involucro </span> </p> </td> 
   <td colname="col2"> <p>Consente di ridimensionare l’immagine composita come <span class="codeph"> ritagliare </span> in modo da coprire l’intera immagine di risposta, ma l’immagine di risposta effettiva potrebbe essere maggiore di quanto specificato con <span class="codeph"> wid= </span> e <span class="codeph"> hei= </span> per evitare il ritaglio. Viene applicata la dimensione maggiore tra <span class="varname"> scala </span> x e <span class="varname"> </span>scala y. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> stretch </span> </p> </td> 
   <td colname="col2"> <p>Consente di ridimensionare l'immagine composita in modo indipendente in x e y per riempire l'intera immagine di risposta, senza ritaglio e senza spazi bianchi. In genere questo modifica le proporzioni dell’immagine. <span class="varname"> xScale </span> viene utilizzato per il ridimensionamento orizzontale e <span class="varname"> yScale </span> per il ridimensionamento verticale. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> hfit </span> </p> </td> 
   <td colname="col2"> <p>Applica <span class="varname"> xScale </span> per adattare l’immagine in orizzontale, con possibilità di ritaglio o di spazi bianchi nella parte superiore e/o inferiore. Utile per applicazioni speciali. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> adatto </span> </p> </td> 
   <td colname="col2"> <p>Applica la <span class="varname"> scala y </span> per adattare l’immagine verticalmente, con possibilità di ritaglio o spazi bianchi a sinistra e/o a destra. Utile per applicazioni speciali. </p> </td> 
  </tr> 
 </tbody> 
</table>

Impostare *`upscale`* &#39;1&#39; per consentire l&#39;ingrandimento o &#39;0&#39; per vincolare *`xScale`*e *`yScale`* essere limitato a 1:1. Se l’opzione di ridimensionamento è disattivata, se l’immagine composita è più piccola dell’immagine di risposta potrebbe essere presente degli spazi bianchi aggiuntivi.

Ritaglia e spazi bianchi sono centrati per impostazione predefinita; la loro posizione può essere controllata con `align=`. Il colore e l’opacità del riempimento degli spazi bianchi sono determinati da `bgc=`.

## Proprietà {#section-6d7a5a7e18434bca9bc2fdb236af8909}

Visualizza attributo. Si applica indipendentemente dall’impostazione del livello corrente. Almeno uno `wid=` o `hei=` deve essere specificato, altrimenti viene restituito un errore; sia `wid=` che `hei=` devono essere specificati affinché le modalità di adattamento funzionino come descritto. Viene restituito un errore anche quando `req=tmb` viene specificato.

## Predefinito {#section-3a553b4b29ef447a8331d6954f3f06da}

`fit=fit,0`

## Consultate anche {#section-788f7e168da64fc5abf29d971a598b01}

[wid=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-wid.md#reference-bfeadcb67bf4485f851eb21345527e47) , [hei=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-hei.md#reference-6d6f556ccc0e4b98a815e8a5c1944a96), [scl=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-scl.md#reference-b2a74e493d0d407e98fe350551ba3fcc), [align=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-align.md#reference-b7d6b87c75124d78884f916dd6544bc7)
