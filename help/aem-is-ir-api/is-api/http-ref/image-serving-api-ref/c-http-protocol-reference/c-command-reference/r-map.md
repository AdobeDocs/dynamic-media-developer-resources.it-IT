---
description: Dati mappa immagine. Fornisce i dati della mappa immagine per questo livello. Ignora tutti i dati della mappa del catalogo per questo livello.
solution: Experience Manager
title: map
feature: Dynamic Media Classic, SDK/API
role: Developer,User
exl-id: 7c1fbb50-98ec-4d9a-b608-93d60d687069
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '228'
ht-degree: 2%

---

# map{#map}

Dati mappa immagine. Fornisce i dati della mappa immagine per questo livello. Ignora tutti i dati dal catalogo::Map per questo livello.

`map=[ *``*]mapA=[ *`stringaA`*]`

<table id="simpletable_2E32B25D5F6246A18A8AF817903877ED"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> string</span></span> </p></td> 
  <td class="stentry"> <p>I dati della mappa immagine per questo livello nelle coordinate del livello. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> stringA</span></span> </p></td> 
  <td class="stentry"> <p>I dati della mappa immagine per questo livello nelle coordinate dell'immagine sorgente. </p></td> 
 </tr> 
</table>

Una stringa vuota indica che questo livello non deve fornire una mappa immagine. Per evitare problemi di analisi, la stringa deve essere codificata correttamente in HTTP.

Tutti i caratteri commerciali (&amp;) presenti in *`string`* devono essere codificati in http.

Mentre `mapA=` e `catalog::Map` specificano i dati della mappa nelle coordinate dell&#39;immagine di origine, `map=` assume le coordinate del livello relative all&#39;angolo superiore sinistro del rettangolo di livello (dopo l&#39;applicazione di `rotate=` e `extend=`).

La mappa immagine di output viene sempre ritagliata al rettangolo del livello. Se l&#39;attributo `shape` viene omesso o impostato su `default`, l&#39;intero rettangolo di livello viene utilizzato come area della mappa immagine.

## Proprietà {#section-a18d9ea95c71414a905a68b8839c0843}

Attributo livello. Se applicati a `layer=comp`, i dati della mappa specificati vengono posizionati dietro tutte le altre mappe immagine. Ignorato a meno che `req=map`. Ignorato dai livelli di effetto. `mapA=` viene ignorato anche se  `map=` è specificato.

## Predefinito {#section-620c19b3f3b84ba49706062de3f12f05}

`catalog::Map` viene utilizzato se non  `map=` è specificato.

## Esempio {#section-cd7691c94f984222845c86dcb0051ce8}

Definire una mappa immagine rettangolare per un livello di testo semplice:

`…&layer=1&text=Scene7&map=<area%20alt=Scene7%20href=www.scene7.com>&…`

Un elemento `AREA` con attributi predefiniti (per lo più) viene utilizzato per inserire l&#39;area della mappa per l&#39;intero rettangolo del livello.

## Consultate anche {#section-bc1d946fdf4b47bf9742a986800aa9b5}

[Mappe immagine](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-image-maps.md#reference-ff7d1bac2a064104b0c508a81316fdab),  [req=map](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76)
