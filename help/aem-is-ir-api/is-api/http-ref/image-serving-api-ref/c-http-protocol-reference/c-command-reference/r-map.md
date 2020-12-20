---
description: Dati mappa immagine. Fornisce i dati delle mappe immagine per questo livello. Ignora tutti i dati dalla mappa catalogo per questo livello.
seo-description: Dati mappa immagine. Fornisce i dati delle mappe immagine per questo livello. Ignora tutti i dati dalla mappa catalogo per questo livello.
seo-title: map
solution: Experience Manager
title: map
topic: Scene7 Image Serving - Image Rendering API
uuid: 9c1c3323-21ab-4820-bf4e-761b82ada1ab
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '243'
ht-degree: 2%

---


# map{#map}

Dati mappa immagine. Fornisce i dati delle mappe immagine per questo livello. Ignora tutti i dati dal catalogo::Map per questo livello.

`map=[ *``*]mapA=[ *`stringstringA`*]`

<table id="simpletable_2E32B25D5F6246A18A8AF817903877ED"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> string</span></span> </p></td> 
  <td class="stentry"> <p>I dati della mappa immagine per questo livello nelle coordinate del livello. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> stringA</span></span> </p></td> 
  <td class="stentry"> <p>I dati della mappa immagine per questo livello nelle coordinate dell’immagine sorgente. </p></td> 
 </tr> 
</table>

Una stringa vuota indica che questo livello non deve fornire una mappa immagine. Per evitare problemi di analisi, la stringa deve essere codificata correttamente tramite HTTP.

Tutti i caratteri e commerciale (&amp;) presenti in *`string`* devono essere codificati http-encoded.

Mentre `mapA=` e `catalog::Map` specificano i dati della mappa nelle coordinate dell&#39;immagine sorgente, `map=` presuppone che le coordinate del livello siano relative all&#39;angolo superiore sinistro del rettangolo del livello (dopo l&#39;applicazione di `rotate=` e `extend=`).

La mappa immagine di output viene sempre ritagliata al rettangolo del livello. Se l&#39;attributo `shape` viene omesso o impostato su `default`, l&#39;intero rettangolo del livello viene utilizzato come area della mappa immagine.

## Proprietà {#section-a18d9ea95c71414a905a68b8839c0843}

Attributo layer. Se applicati a `layer=comp`, i dati della mappa specificati sono posizionati dietro tutte le altre mappe immagine. Ignorato a meno che `req=map`. Ignorato dai livelli degli effetti. `mapA=` viene ignorato se  `map=` è specificato anche.

## Predefinito {#section-620c19b3f3b84ba49706062de3f12f05}

`catalog::Map` viene utilizzato se non  `map=` è specificato.

## Esempio {#section-cd7691c94f984222845c86dcb0051ce8}

Definite una mappa immagine rettangolare per un semplice livello di testo:

`…&layer=1&text=Scene7&map=<area%20alt=Scene7%20href=www.scene7.com>&…`

Per inserire l’area della mappa per l’intero rettangolo del livello, viene utilizzato un elemento `AREA` con (principalmente) attributi predefiniti.

## Consultate anche {#section-bc1d946fdf4b47bf9742a986800aa9b5}

[Mappe](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-image-maps.md#reference-ff7d1bac2a064104b0c508a81316fdab) immagine,  [req=map](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76)
