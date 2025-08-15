---
title: adatto
description: La risposta Immagine modalità di adattamento. Specifica come viene calcolato il fattore di scala, che viene utilizzato per ridimensionare l'immagine composita all'immagine di risposta quando la dimensione di risposta è specificata con wid= e hei= e scl= non è presente.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: d2939f86-5dab-471d-ba59-70d91ae1e4fd
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '489'
ht-degree: 0%

---

# adatto{#fit}

La risposta Immagine modalità di adattamento. Specifica come viene calcolato il fattore di scala, che viene utilizzato per ridimensionare l&#39;immagine composita all&#39;immagine di risposta quando la dimensione di risposta è specificata con wid= e hei= e scl= non è presente.

` fit= *`Upscale della modalità`*, *``*`

<table id="simpletable_50FBDC6B7CB2448891DD0F491DEB5ACF"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"><span class="varname"> modo </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> fit|vincolo|crop|wrap|stretch|hfit|vfit </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"><span class="varname"> Lusso </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> 0|1 </span> </p> </td> 
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
   <td colname="col1"> <p> <span class="codeph"> adatto </span> </p> </td> 
   <td colname="col2"> <p>Ridimensiona l'immagine composita in modo che rientri nello spazio allocato con <span class="codeph"> wid= </span> e <span class="codeph"> hei= </span>, con spazi bianchi minimi e senza ritaglio. L'immagine di risposta ha le dimensioni esatte specificate con <span class="codeph"> wid= </span> e <span class="codeph"> hei= </span>. Viene applicato il più piccolo tra <span class="varname"> xScale </span> e <span class="varname"> yScale </span> . </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> costringere </span> </p> </td> 
   <td colname="col2"> <p>Ridimensiona l'immagine composita like <span class="codeph"> adatta </span> in modo che rientri nello spazio allocato con <span class="codeph"> wid= </span> e <span class="codeph"> hei= </span>, ma l'immagine di risposta effettiva potrebbe essere più piccola di quella specificata con <span class="codeph"> wid= </span> e <span class="codeph"> hei= </span> per evitare spazi vuoti. Viene applicato il più piccolo tra <span class="varname"> xScale </span> e <span class="varname"> yScale </span> . </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> raccolto </span> </p> </td> 
   <td colname="col2"> <p>Ridimensiona l'immagine composita in modo che riempia l'intera immagine di risposta, con un ritaglio minimo e senza spazi vuoti. Viene applicato il più grande tra <span class="varname"> xScale </span> e <span class="varname"> yScale </span> . </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> avvolgere </span> </p> </td> 
   <td colname="col2"> <p>Ridimensiona l'immagine composita like <span class="codeph"> ritaglia </span> in modo che copra l'intera immagine di risposta, ma l'immagine di risposta effettiva potrebbe essere più grande di quanto specificato con <span class="codeph"> wid= </span> e <span class="codeph"> hei= </span> per evitare il ritaglio. Viene applicato il più grande tra <span class="varname"> xScale </span> e <span class="varname"> yScale </span>. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> stendere </span> </p> </td> 
   <td colname="col2"> <p>Ridimensiona l'immagine composita in modo indipendente in x e y per riempire l'intera immagine di risposta, senza ritaglio e senza spazi vuoti. Questo in genere modifica le proporzioni dell'immagine. <span class="varname"> xScale </span> viene utilizzato per il ridimensionamento orizzontale e <span class="varname"> yScale </span> per il ridimensionamento verticale. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> hfit </span> </p> </td> 
   <td colname="col2"> <p>Applica <span class="varname"> xScale </span> per adattare perfettamente l'immagine orizzontalmente, con probabile ritaglio o spazio bianco nella parte superiore e/o inferiore. Utile per applicazioni speciali. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> vfit </span> </p> </td> 
   <td colname="col2"> <p>Applica <span class="varname"> yScale </span> per adattare perfettamente l'immagine in verticale, con probabile ritaglio o spazio bianco a sinistra e/o a destra. Utile per applicazioni speciali. </p> </td> 
  </tr> 
 </tbody> 
</table>

Imposta *`upscale`* su &#39;1&#39; per consentire l&#39;upscaling o su &#39;0&#39; su vincolo *`xScale`* e *`yScale`* su un limite a 1:1. Se l&#39;upscaling è disabilitato, potrebbe essere presente uno spazio bianco aggiuntivo se l&#39;immagine composita è più piccola dell&#39;immagine di risposta.

Ritaglio e gli spazi vuoti sono centrati per impostazione predefinita; La loro posizione può essere controllata con `align=`. Il colore e l&#39;opacità del riempimento degli spazi bianchi sono determinati da `bgc=`.

## Proprietà {#section-6d7a5a7e18434bca9bc2fdb236af8909}

Visualizza attributo. Si applica indipendentemente dall&#39;impostazione corrente del livello. Almeno uno di o `wid=` deve anche essere specificato, altrimenti viene restituito un errore; entrambi `hei=` e `wid=` devono essere specificati affinché le modalità di `hei=` adattamento si comportino come descritto. Quando viene specificato, viene restituito `req=tmb` anche un errore.

## Predefinito {#section-3a553b4b29ef447a8331d6954f3f06da}

`fit=fit,0`

## Consultate anche {#section-788f7e168da64fc5abf29d971a598b01}

[wid=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-wid.md#reference-bfeadcb67bf4485f851eb21345527e47) , [hei=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-hei.md#reference-6d6f556ccc0e4b98a815e8a5c1944a96), [scl=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-scl.md#reference-b2a74e493d0d407e98fe350551ba3fcc), [align=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-align.md#reference-b7d6b87c75124d78884f916dd6544bc7)
