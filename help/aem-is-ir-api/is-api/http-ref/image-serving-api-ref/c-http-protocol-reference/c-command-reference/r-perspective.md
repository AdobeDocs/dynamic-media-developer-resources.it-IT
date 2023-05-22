---
description: Trasformazione prospettica. Applicate una trasformazione prospettica all'immagine sorgente del livello per riempire la regione specificata con il quadrilatero. Altre aree del livello rimangono trasparenti.
solution: Experience Manager
title: prospettiva
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 2e0297b0-c9a4-4bbd-9f06-368f722288d4
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '450'
ht-degree: 1%

---

# prospettiva{#perspective}

Trasformazione prospettica. Applicate una trasformazione prospettica all&#39;immagine sorgente del livello per riempire la regione specificata con il quadrilatero. Altre aree del livello rimangono trasparenti.

`perspective= *`perspQuad`*[, *`resOptions`*]`

`perspectiveN= *`perspQuadN`*[, *`resOptions`*]`

<table id="simpletable_4BD38BBF53964F7D97B9E58914C97B3F"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> perspQuad</span> </p></td> 
  <td class="stentry"> <p>Coordinate prospettiche in pixel quadrilaterali (8 reali, separate da virgole). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> perspQuadN</span> </p></td> 
  <td class="stentry"> <p>Coordinate prospettiche normalizzate quadrilaterali (8 reali, separate da virgole). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> resOptions</span> </p></td> 
  <td class="stentry"> <p>Opzioni di ricampionamento (vedere di seguito). </p></td> 
 </tr> 
</table>

*`perspQuad`* è costituito da quattro valori di coordinate in pixel nello spazio di coordinate composito (o livello 0), che ha origine nell&#39;angolo superiore sinistro dell&#39;immagine composita.

`perspQuadN` è costituito da quattro valori di coordinate normalizzati, in cui `0.0,0.0` corrisponde all&#39;angolo superiore sinistro dell&#39;immagine composita/livello 0 e `1.0,1.0` nell’angolo in basso a destra.

L&#39;immagine di input viene trasformata in modo che l&#39;angolo superiore sinistro dell&#39;immagine di input venga mappato al primo valore di coordinata di `perspQuad[N]`, l&#39;angolo superiore destro alla seconda coordinata, l&#39;angolo inferiore destro alla terza coordinata e l&#39;angolo inferiore sinistro alla quarta coordinata.

>[!NOTE]
>
>`pos=` può essere utilizzato per posizionare ulteriormente il livello trasformato nell&#39;immagine composita.

Le coordinate quadrilaterali prospettiche possono essere posizionate all&#39;esterno dell&#39;immagine composita.

Il comportamento è indefinito se il quadrilatero non è adatto a una trasformazione prospettica (ad esempio, se due o più vertici coincidono, se tre o tutti i vertici si trovano sulla stessa linea o se il quadrilatero è auto-intersecante o concavo).

## Considerazioni sulla qualità {#section-7cc9056afa614300a9b8844d39739fc3}

Anche se l&#39;implementazione predefinita produce un compromesso ragionevole tra qualità e prestazioni, a volte può essere necessario aumentare la risoluzione dell&#39;immagine sorgente per migliorare la nitidezza o ridurla per ridurre gli artefatti di aliasing.

Se l’origine è un’immagine, utilizza `scale=` per scegliere una risoluzione diversa (relativa alla risoluzione massima dell&#39;immagine). Il valore specificato `scale=` viene arrotondato al successivo livello di risoluzione PTIF superiore. In caso di origine di richiesta nidificata, è possibile regolare le dimensioni dell’immagine prodotta dalla richiesta nidificata per ottenere la nitidezza desiderata. Per i livelli di testo, la risoluzione dell&#39;immagine di input (il testo di cui è stato eseguito il rendering) viene regolata selezionando un valore size= più grande insieme all&#39;aumento della risoluzione specificato con `textAttr=`.

*`resOptions`* consente di selezionare un algoritmo di ricampionamento alternativo. Sono supportati i seguenti valori (distinzione maiuscole/minuscole):

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
   <td> <p> Il vicino più vicino. </p> </td> 
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
   <td> <p> <span class="codeph">R3T<span class="varname"> n</span></span> </p> </td> 
   <td> <p> Super-campionamento con jitter regolabile (<span class="varname"> n</span> deve essere un numero intero compreso tra 0 e 200). </p> </td> 
  </tr> 
 </tbody> 
</table>

## Proprietà {#section-818e57df0a1b4449888543bc6af77751}

Comando Livello. Si applica al livello corrente o al livello 0 se `layer=comp`. Ignorato dai livelli degli effetti.

`res=` viene sempre ignorato quando la prospettiva è presente nello stesso livello. `size=` viene ignorato se specificato per i livelli immagine. `size=` e `res=` nei livelli con `perspective=` sono riservati per un utilizzo futuro.

## Predefinito {#section-e35683395d514d4eb6b32924e1bf8f2f}

`None`, senza alcuna trasformazione prospettica.

## Consultate anche {#section-e5b71ac4a0724df6bf678dd354cfa51a}

[size= dimensione](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-size.md#reference-04d383f32c7b4003bed9978cb854747b) , [scale=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-scale.md#reference-098c30cea1764f189e6f7c7e400cc065), [pos=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-pos.md#reference-65de948f4b404f1182b22119ca332143), [textAttr=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textattr.md#reference-ff00484fa3244286abeff34911f7ec0d)
