---
title: mappa
description: Dati mappa immagine. Fornisce i dati mappa immagine per questo livello. Sostituisce tutti i dati dalla mappa del catalogo per questo livello.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 7c1fbb50-98ec-4d9a-b608-93d60d687069
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '223'
ht-degree: 1%

---

# mappa{#map}

Dati mappa immagine. Fornisce i dati mappa immagine per questo livello. Esegue l&#39;override dei dati di catalog::Map per questo livello.

`map=[ *`stringa`*]mapA=[ *`stringA`*]`

<table id="simpletable_2E32B25D5F6246A18A8AF817903877ED"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> stringa</span></span> </p></td> 
  <td class="stentry"> <p>Dati mappa immagine per questo livello in coordinate livello. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> stringA</span></span> </p></td> 
  <td class="stentry"> <p>Dati mappa immagine per questo livello nelle coordinate dell'immagine sorgente. </p></td> 
 </tr> 
</table>

Una stringa vuota indica che questo livello non deve fornire una mappa immagine. Per evitare problemi di analisi, la stringa deve essere correttamente codificata per HTTP.

Tutti i caratteri e commerciale (&amp;) presenti in *`string`* deve avere la codifica http.

Mentre `mapA=` e `catalog::Map` specificare i dati della mappa nelle coordinate dell&#39;immagine di origine; `map=` assume le coordinate di livello relative all&#39;angolo superiore sinistro del rettangolo di livello (dopo `rotate=` e `extend=` sono state applicate).

La mappa immagine di output viene sempre ritagliata nel rettangolo del livello. Se il `shape` attributo omesso o impostato su `default`, l&#39;intero rettangolo di livello viene utilizzato come area della mappa immagine.

## Proprietà {#section-a18d9ea95c71414a905a68b8839c0843}

Attributo livello. Quando viene applicato a `layer=comp`, i dati di mappa specificati sono sovrapposti a tutte le altre mappe immagine. Ignorato a meno che `req=map`. Ignorato dai livelli degli effetti. `mapA=` viene ignorato se `map=` viene specificato anche.

## Predefinito {#section-620c19b3f3b84ba49706062de3f12f05}

`catalog::Map` viene utilizzato se `map=` non è specificato.

## Esempio {#section-cd7691c94f984222845c86dcb0051ce8}

Definite una mappa immagine rettangolare per un livello di testo semplice:

`…&layer=1&text=Scene7&map=<area%20alt=Scene7%20href=www.scene7.com>&…`

Un `AREA` per inserire l&#39;area della mappa per l&#39;intero rettangolo del livello viene utilizzato l&#39;elemento con (principalmente) attributi predefiniti.

## Consultate anche {#section-bc1d946fdf4b47bf9742a986800aa9b5}

[Mappe immagine](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-image-maps.md#reference-ff7d1bac2a064104b0c508a81316fdab), [req=map](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76)
