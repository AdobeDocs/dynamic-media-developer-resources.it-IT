---
description: Trasformazione prospettica. Applicate una trasformazione prospettica all’immagine sorgente del livello per riempire la regione specificata con il quadrilatero. Altre aree dello strato rimangono trasparenti.
seo-description: Trasformazione prospettica. Applicate una trasformazione prospettica all’immagine sorgente del livello per riempire la regione specificata con il quadrilatero. Altre aree dello strato rimangono trasparenti.
seo-title: prospettiva
solution: Experience Manager
title: prospettiva
topic: Scene7 Image Serving - Image Rendering API
uuid: b22d7b49-db08-48df-80bc-5b7237aea475
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# prospettiva{#perspective}

Trasformazione prospettica. Applicate una trasformazione prospettica all’immagine sorgente del livello per riempire la regione specificata con il quadrilatero. Altre aree dello strato rimangono trasparenti.

`perspective= *``*[, *`perspQuadresOptions`*]`

`perspectiveN= *``*[, *`perspQuadNresOptions`*]`

<table id="simpletable_4BD38BBF53964F7D97B9E58914C97B3F"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> perspQuad</span> </p></td> 
  <td class="stentry"> <p>Coordinate pixel quadrilaterali in prospettiva (8 reali, separate da virgole). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> perspQuadN</span> </p></td> 
  <td class="stentry"> <p>Coordinate quadrilaterali normalizzate (8 reali, separate da virgole). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> resOptions</span> </p></td> 
  <td class="stentry"> <p>Opzioni di ricampionamento (vedere di seguito). </p></td> 
 </tr> 
</table>

*`perspQuad`* consiste di quattro valori di coordinate pixel nello spazio di coordinate composito (o livello 0), che ha origine nell’angolo superiore sinistro dell’immagine composita.

`perspQuadN` consiste di quattro valori di coordinate normalizzate, `0.0,0.0` corrispondenti all’angolo superiore sinistro dell’immagine composita/livello 0 e `1.0,1.0` all’angolo inferiore destro.

L&#39;immagine di input viene trasformata in modo che l&#39;angolo superiore sinistro dell&#39;immagine di input venga mappato sul valore della prima coordinata di `perspQuad[N]`, sull&#39;angolo superiore destro sulla seconda coordinata, sull&#39;angolo inferiore destro sulla terza coordinata e sull&#39;angolo inferiore sinistro sulla quarta coordinata.

>[!NOTE]
>
>`pos=` può essere usato per posizionare ulteriormente lo strato trasformato nell’immagine composita.

Le coordinate quadrilaterali prospettiche possono essere collocate all’esterno dell’immagine composita.

Il comportamento non è definito se il quadrilatero non è adatto per una trasformazione prospettica (ad esempio, se due o più vertici coincidono, se tre o tutti i vertici si trovano sulla stessa linea, o se il quadrilatero è autointersecante o concavo).

## Considerazioni sulla qualità {#section-7cc9056afa614300a9b8844d39739fc3}

Mentre l&#39;implementazione predefinita produce un compromesso ragionevole tra qualità e prestazioni, a volte può essere necessario aumentare la risoluzione dell&#39;immagine sorgente per migliorare la nitidezza o ridurla per ridurre gli artefatti di alias.

Se la sorgente è un’immagine, scegliete `scale=` una risoluzione diversa (relativa alla risoluzione completa dell’immagine). Il valore specificato `scale=` viene arrotondato al successivo livello di risoluzione PTIF più alto. Nel caso di un’origine di richiesta nidificata, le dimensioni dell’immagine prodotta dalla richiesta nidificata possono essere regolate in modo da ottenere la nitidezza desiderata. Per i livelli di testo, la risoluzione dell’immagine di input (il testo di cui viene eseguito il rendering) viene regolata selezionando un valore size= più grande insieme all’aumento della risoluzione specificata con `textAttr=`.

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
   <td> <p> Vicina più vicina. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> R2</span> </p> </td> 
   <td> <p> Bilineare. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> R3</span> </p> </td> 
   <td> <p> Super-sampling standard (predefinito). </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph">R3T<span class="varname"> n</span></span> </p> </td> 
   <td> <p> Super-campionamento con jitter regolabile (<span class="varname"> n</span> deve essere un valore intero compreso tra 0 e 200). </p> </td> 
  </tr> 
 </tbody> 
</table>

## Proprietà {#section-818e57df0a1b4449888543bc6af77751}

Livello, comando. Si applica al livello corrente o al livello 0, se `layer=comp`. Ignorato dai livelli degli effetti.

`res=` viene sempre ignorata quando la prospettiva è presente nello stesso livello. `size=` viene ignorato se specificato per i livelli immagine. `size=` e `res=` nei livelli con `perspective=` sono riservati per utilizzi futuri.

## Predefinito {#section-e35683395d514d4eb6b32924e1bf8f2f}

`None`, per nessuna trasformazione prospettica.

## Consultate anche {#section-e5b71ac4a0724df6bf678dd354cfa51a}

[size=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-size.md#reference-04d383f32c7b4003bed9978cb854747b) , [scale=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-scale.md#reference-098c30cea1764f189e6f7c7e400cc065), [pos=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-pos.md#reference-65de948f4b404f1182b22119ca332143), [textAttr=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textattr.md#reference-ff00484fa3244286abeff34911f7ec0d)
