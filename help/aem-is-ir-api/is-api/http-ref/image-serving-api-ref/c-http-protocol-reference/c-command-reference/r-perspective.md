---
description: Trasformazione della prospettiva. Applicate una trasformazione prospettica all'immagine sorgente del livello per riempire la regione specificata con il quadrilatero. Altre aree dello strato rimangono trasparenti.
solution: Experience Manager
title: prospettiva
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '458'
ht-degree: 2%

---


# prospettiva{#perspective}

Trasformazione della prospettiva. Applicate una trasformazione prospettica all&#39;immagine sorgente del livello per riempire la regione specificata con il quadrilatero. Altre aree dello strato rimangono trasparenti.

`perspective= *``*[, *`perspQuadresOptions`*]`

`perspectiveN= *``*[, *`perspQuadNresOptions`*]`

<table id="simpletable_4BD38BBF53964F7D97B9E58914C97B3F"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> perspQuad</span> </p></td> 
  <td class="stentry"> <p>Coordinate pixel quadrilaterali prospettiche (8 reali, separate da virgole). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> perspQuadN</span> </p></td> 
  <td class="stentry"> <p>Coordinate quadrilaterali normalizzate (8 reali, separate da virgole). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> resOptions</span> </p></td> 
  <td class="stentry"> <p>Opzioni di ricampionamento (vedi di seguito). </p></td> 
 </tr> 
</table>

*`perspQuad`* è costituito da quattro valori di coordinate pixel nello spazio di coordinate composito (o livello 0), che ha origine nell&#39;angolo superiore sinistro dell&#39;immagine composita.

`perspQuadN` è costituito da quattro valori di coordinate normalizzate,  `0.0,0.0` corrispondenti all&#39;angolo superiore sinistro dell&#39;immagine composita/layer 0 e  `1.0,1.0` all&#39;angolo inferiore destro.

L’immagine di input viene trasformata in modo che l’angolo in alto a sinistra dell’immagine di input sia mappato sul primo valore di coordinata `perspQuad[N]`, l’angolo in alto a destra sulla seconda coordinata, l’angolo in basso a destra sulla terza coordinata e l’angolo in basso a sinistra sulla quarta coordinata.

>[!NOTE]
>
>`pos=` può essere utilizzato per posizionare ulteriormente lo strato trasformato nell&#39;immagine composita.

Le coordinate quadrilaterali prospettiche possono essere collocate al di fuori dell&#39;immagine composita.

Il comportamento non è definito se il quadrilatero non è adatto per una trasformazione prospettica (ad esempio, se due o più vertici coincidono, se tre o tutti i vertici si trovano sulla stessa linea, o se il quadrilatero è autointersecante o concava).

## Considerazioni sulla qualità {#section-7cc9056afa614300a9b8844d39739fc3}

Mentre l&#39;implementazione predefinita produce un compromesso ragionevole tra qualità e prestazioni, a volte può essere necessario aumentare la risoluzione dell&#39;immagine sorgente per migliorare la nitidezza o ridurla per ridurre gli artefatti di aliasing.

Se la sorgente è un’immagine, utilizza `scale=` per scegliere una risoluzione diversa (rispetto alla risoluzione completa dell’immagine). Il valore `scale=` specificato viene arrotondato al livello di risoluzione PTIF superiore successivo. Nel caso di una sorgente di richiesta nidificata, le dimensioni dell’immagine prodotta dalla richiesta nidificata possono essere regolate in modo da ottenere la nitidezza desiderata. Per i livelli di testo, la risoluzione dell&#39;immagine di input (il testo di cui è stato eseguito il rendering) viene regolata selezionando un valore di dimensione maggiore= e aumentando la risoluzione specificata con `textAttr=`.

*`resOptions`* consente di selezionare un algoritmo di ricampionamento alternativo. Sono supportati i seguenti valori (con distinzione tra maiuscole e minuscole):

<table id="table_0F20007986324E228096888ED37219C0"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> Valore</b> </th> 
   <th class="entry"> <b> Descrizione</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> R1</span> </p> </td> 
   <td> <p> Vicino più vicino. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> R2</span> </p> </td> 
   <td> <p> Bilineare. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> R3</span> </p> </td> 
   <td> <p> Super-campionamento standard (predefinito). </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph">R3<span class="varname"> Tn</span></span> </p> </td> 
   <td> <p> Il campionamento eccellente con tremolio regolabile (<span class="varname"> n</span> deve essere un valore intero compreso tra 0 e 200). </p> </td> 
  </tr> 
 </tbody> 
</table>

## Proprietà {#section-818e57df0a1b4449888543bc6af77751}

Livello, comando. Si applica al livello corrente o al livello 0 se `layer=comp`. Ignorato dai livelli di effetto.

`res=` viene sempre ignorato quando la prospettiva è presente nello stesso livello. `size=` viene ignorato quando specificato per i livelli immagine. `size=` e  `res=` nei livelli con  `perspective=` sono riservati per utilizzi futuri.

## Predefinito {#section-e35683395d514d4eb6b32924e1bf8f2f}

`None`, senza trasformazione prospettica.

## Consultate anche {#section-e5b71ac4a0724df6bf678dd354cfa51a}

[size=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-size.md#reference-04d383f32c7b4003bed9978cb854747b) ,  [scale=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-scale.md#reference-098c30cea1764f189e6f7c7e400cc065),  [pos=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-pos.md#reference-65de948f4b404f1182b22119ca332143),  [textAttr=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textattr.md#reference-ff00484fa3244286abeff34911f7ec0d)
