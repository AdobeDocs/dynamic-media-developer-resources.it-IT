---
title: adatta
description: Modalità di adattamento dell'immagine di risposta. Specifica come viene calcolato il fattore di scala, utilizzato per scalare l'immagine composita sull'immagine di risposta quando la dimensione di risposta è specificata con wid= e hei= e scl= non è presente.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: d2939f86-5dab-471d-ba59-70d91ae1e4fd
source-git-commit: 7c4492b583e7bd6fb87229c4566f1d9493c8a650
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# adatta{#fit}

Modalità di adattamento dell&#39;immagine di risposta. Specifica come viene calcolato il fattore di scala, utilizzato per scalare l&#39;immagine composita sull&#39;immagine di risposta quando la dimensione di risposta è specificata con wid= e hei= e scl= non è presente.

` fit= *`modalità`*, *`aumento`*`

<table id="simpletable_50FBDC6B7CB2448891DD0F491DEB5ACF"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> modalità </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> adattamento|vincolo|ritaglio|avvolgimento|allungamento|adattamento|adattamento </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> aumento </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> 0 | 1 </span> </p> </td> 
 </tr> 
</table>

Nella seguente descrizione delle opzioni della modalità, si presume che *`xScale`* è il rapporto tra la larghezza dell&#39;immagine composita e la larghezza dell&#39;immagine di risposta e *`yScale`* è il rapporto tra l&#39;altezza dell&#39;immagine composita e l&#39;altezza dell&#39;immagine di risposta.

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
   <td colname="col2"> <p>Ridimensiona l'immagine composita in modo che si adatti allo spazio allocato con <span class="codeph"> wid= </span> e <span class="codeph"> hei= </span>con spazio bianco minimo e nessuna ritaglio. L'immagine di risposta avrà la dimensione esatta specificata con <span class="codeph"> wid= </span> e <span class="codeph"> hei= </span>. Più piccolo di <span class="varname"> xScale </span> e <span class="varname"> Scala y </span> viene applicata. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> vincolo </span> </p> </td> 
   <td colname="col2"> <p>Ridimensiona l'immagine composita come <span class="codeph"> adatto </span> in modo che si adatti allo spazio assegnato con <span class="codeph"> wid= </span> e <span class="codeph"> hei= </span>, ma l'immagine di risposta effettiva può essere inferiore a quanto specificato con <span class="codeph"> wid= </span> e <span class="codeph"> hei= </span> per evitare spazi bianchi. Più piccolo di <span class="varname"> xScale </span> e <span class="varname"> Scala y </span> viene applicata. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> Ritaglia </span> </p> </td> 
   <td colname="col2"> <p>Ridimensiona l'immagine composita in modo da riempire l'intera immagine di risposta, con un ritaglio minimo e senza spazi bianchi. Più grande di <span class="varname"> xScale </span> e <span class="varname"> Scala y </span> viene applicata. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> avvolgere </span> </p> </td> 
   <td colname="col2"> <p>Ridimensiona l'immagine composita come <span class="codeph"> coltura </span> in modo che copra l'intera immagine di risposta, ma l'immagine di risposta effettiva può essere più grande di quanto specificato con <span class="codeph"> wid= </span> e <span class="codeph"> hei= </span> per evitare il ritaglio. Più grande di <span class="varname"> xScale </span> e <span class="varname"> Scala y </span>viene applicata. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> distendere </span> </p> </td> 
   <td colname="col2"> <p>Ridimensiona l'immagine composita in modo indipendente in x e y per riempire l'intera immagine di risposta, senza ritaglio e senza spazi bianchi. In genere questo cambia le proporzioni dell'immagine. <span class="varname"> xScale </span> viene utilizzato per la scala orizzontale e <span class="varname"> Scala y </span> per il ridimensionamento verticale. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> vestibilità </span> </p> </td> 
   <td colname="col2"> <p>Si applica <span class="varname"> xScale </span> per adattare rigorosamente l'immagine orizzontalmente, con probabile ritaglio o spazio bianco nella parte superiore e/o inferiore. Utile per applicazioni speciali. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> viziare </span> </p> </td> 
   <td colname="col2"> <p>Si applica <span class="varname"> Scala y </span> per adattare verticalmente l'immagine, con probabile ritaglio o spazio vuoto a sinistra e/o a destra. Utile per applicazioni speciali. </p> </td> 
  </tr> 
 </tbody> 
</table>

Imposta *`upscale`* a &#39;1&#39; per consentire l&#39;upscaling o a &#39;0&#39; per vincolare *`xScale`*e *`yScale`* da limitare a 1:1. Se l’opzione di ridimensionamento è disabilitata, potrebbe essere presente ulteriore spazio vuoto se l’immagine composita è più piccola dell’immagine di risposta.

Ritaglio e spazi bianchi sono centrati per impostazione predefinita; la loro posizione può essere controllata con `align=`. Il colore e l&#39;opacità del riempimento dello spazio vuoto sono determinati da `bgc=`.

## Proprietà {#section-6d7a5a7e18434bca9bc2fdb236af8909}

Visualizza attributo. Si applica indipendentemente dall&#39;impostazione del livello corrente. Almeno uno di `wid=` o `hei=` deve essere inoltre specificato, altrimenti viene restituito un errore; entrambi `wid=` e `hei=` devono essere specificati affinché le modalità di adattamento si comportino come descritto. Viene restituito un errore quando `req=tmb` è specificato anche.

## Predefinito {#section-3a553b4b29ef447a8331d6954f3f06da}

`fit=fit,0`

## Consultate anche {#section-788f7e168da64fc5abf29d971a598b01}

[wid=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-wid.md#reference-bfeadcb67bf4485f851eb21345527e47) , [hei=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-hei.md#reference-6d6f556ccc0e4b98a815e8a5c1944a96), [scl=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-scl.md#reference-b2a74e493d0d407e98fe350551ba3fcc), [align=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-align.md#reference-b7d6b87c75124d78884f916dd6544bc7)
