---
title: adatta
description: Modalità Adatta Immagine Risposta. Specifica come viene calcolato il fattore di scala, utilizzato per scalare l'immagine composita all'immagine di risposta quando la dimensione della risposta è specificata con wid= e hei= e scl= non è presente.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: d2939f86-5dab-471d-ba59-70d91ae1e4fd
source-git-commit: 7c4492b583e7bd6fb87229c4566f1d9493c8a650
workflow-type: tm+mt
source-wordcount: '486'
ht-degree: 0%

---

# adatta{#fit}

Modalità Adatta Immagine Risposta. Specifica come viene calcolato il fattore di scala, utilizzato per scalare l&#39;immagine composita all&#39;immagine di risposta quando la dimensione della risposta è specificata con wid= e hei= e scl= non è presente.

` fit= *`modalità`*, *`upscale`*`

<table id="simpletable_50FBDC6B7CB2448891DD0F491DEB5ACF"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> modalità </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> fit|constrain|crop|wrap|stretch|hfit|vfit </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> upscale </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> 0 | 1 </span> </p> </td> 
 </tr> 
</table>

Nella seguente descrizione delle opzioni di modalità, si presume che *`xScale`* è il rapporto tra la larghezza dell&#39;immagine composita e la larghezza dell&#39;immagine di risposta e *`yScale`* è il rapporto tra l’altezza dell’immagine composita e l’altezza dell’immagine di risposta.

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
   <td colname="col2"> <p>Ridimensiona l'immagine composita in modo che rientri nello spazio allocato con <span class="codeph"> wid= </span> e <span class="codeph"> hei= </span>, con spazi vuoti minimi e nessuna ritaglio. L’immagine di risposta avrà le dimensioni esatte specificate con <span class="codeph"> wid= </span> e <span class="codeph"> hei= </span>. Il più piccolo tra <span class="varname"> xScale </span> e <span class="varname"> yScale </span> viene applicata. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> vincolo </span> </p> </td> 
   <td colname="col2"> <p>Ridimensiona l'immagine composita come <span class="codeph"> adatta </span> in modo da adattarsi allo spazio allocato con <span class="codeph"> wid= </span> e <span class="codeph"> hei= </span>, ma l’immagine di risposta effettiva potrebbe essere inferiore a quella specificata con <span class="codeph"> wid= </span> e <span class="codeph"> hei= </span> per evitare spazi vuoti. Il più piccolo tra <span class="varname"> xScale </span> e <span class="varname"> yScale </span> viene applicata. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> ritagliare </span> </p> </td> 
   <td colname="col2"> <p>Ridimensiona l’immagine composita in modo che riempia l’intera immagine di risposta, con ritaglio minimo e senza spazi vuoti. Il più grande di <span class="varname"> xScale </span> e <span class="varname"> yScale </span> viene applicata. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> avvolgere </span> </p> </td> 
   <td colname="col2"> <p>Ridimensiona l'immagine composita come <span class="codeph"> ritagliare </span> in modo che copra l’intera immagine di risposta, ma l’immagine di risposta effettiva potrebbe essere più grande di quanto specificato con <span class="codeph"> wid= </span> e <span class="codeph"> hei= </span> per evitare il ritaglio. Il più grande di <span class="varname"> xScale </span> e <span class="varname"> yScale </span>viene applicata. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> allungare </span> </p> </td> 
   <td colname="col2"> <p>Ridimensiona l’immagine composita in modo indipendente in x e y per riempire l’intera immagine di risposta, senza ritaglio e spazio vuoto. In genere vengono modificate le proporzioni dell'immagine. <span class="varname"> xScale </span> viene utilizzato per il ridimensionamento orizzontale e <span class="varname"> yScale </span> per il ridimensionamento verticale. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> adattare </span> </p> </td> 
   <td colname="col2"> <p>Applicabile <span class="varname"> xScale </span> per adattare strettamente l'immagine in orizzontale, con probabile ritaglio o spazio vuoto nella parte superiore e/o inferiore. Utile per applicazioni speciali. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> vfit </span> </p> </td> 
   <td colname="col2"> <p>Applicabile <span class="varname"> yScale </span> per adattare l'immagine verticalmente, con probabile ritaglio o spazio vuoto a sinistra e/o a destra. Utile per applicazioni speciali. </p> </td> 
  </tr> 
 </tbody> 
</table>

Imposta *`upscale`* a &#39;1&#39; per consentire l&#39;upscaling o a &#39;0&#39; per vincolare *`xScale`*e *`yScale`* limitato a 1:1. Se l&#39;upscaling è disattivato, potrebbero essere presenti spazi vuoti aggiuntivi se l&#39;immagine composita è più piccola dell&#39;immagine di risposta.

Il ritaglio e gli spazi vuoti sono centrati per impostazione predefinita; la loro posizione può essere controllata con `align=`. Il colore e l&#39;opacità del riempimento dello spazio vuoto sono determinati da `bgc=`.

## Proprietà {#section-6d7a5a7e18434bca9bc2fdb236af8909}

Visualizza attributo. Si applica indipendentemente dall&#39;impostazione del livello corrente. Almeno uno di `wid=` o `hei=` deve essere specificato, altrimenti viene restituito un errore; entrambi `wid=` e `hei=` è necessario specificare che le modalità di adattamento si comportino come descritto. Viene restituito un errore quando `req=tmb` viene specificato anche.

## Predefinito {#section-3a553b4b29ef447a8331d6954f3f06da}

`fit=fit,0`

## Consultate anche {#section-788f7e168da64fc5abf29d971a598b01}

[wid=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-wid.md#reference-bfeadcb67bf4485f851eb21345527e47) , [hei=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-hei.md#reference-6d6f556ccc0e4b98a815e8a5c1944a96), [scl=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-scl.md#reference-b2a74e493d0d407e98fe350551ba3fcc), [align=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-align.md#reference-b7d6b87c75124d78884f916dd6544bc7)
