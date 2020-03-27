---
description: Allinea immagine con vista. Allinea l’immagine composita (possibilmente dopo il ridimensionamento, se è specificato anche scl=) all’interno del rettangolo di visualizzazione definito da wid= e hei=.
seo-description: Allinea immagine con vista. Allinea l’immagine composita (possibilmente dopo il ridimensionamento, se è specificato anche scl=) all’interno del rettangolo di visualizzazione definito da wid= e hei=.
seo-title: allinea
solution: Experience Manager
title: allinea
topic: Scene7 Image Serving - Image Rendering API
uuid: 91940bd4-8e2b-4949-a76d-31cd238783bc
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# align{#align}

Allinea immagine con vista. Allinea l’immagine composita (possibilmente dopo il ridimensionamento, se è specificato anche scl=) all’interno del rettangolo di visualizzazione definito da wid= e hei=.

` align= *``*, *`orizzonte`*`

<table id="simpletable_4CB26F72A56D4515B767C303F8E8A1CF"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> horiz </span></span> </p> </td> 
  <td class="stentry"> <p>allineamento orizzontale (reale, -1.0...1.0) </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> vert </span></span> </p> </td> 
  <td class="stentry"> <p>allineamento verticale (reale, -1.0...1.0) </p> </td> 
 </tr> 
</table>

Specificate `align=-1,-1` per allineare l’immagine in alto a sinistra con quella in alto a sinistra della vista, specificate `align=1,1` per allineare l’immagine in basso a destra con quella in basso a destra della vista. Per le richieste standard di immagini e miniature, viene riempita qualsiasi area della vista non coperta dai dati compositi delle immagini `bgc=`.

## Proprietà {#section-3fbec8206fc944eda4746d8be84f3b41}

Visualizza attributo. ( `align=` viene anche utilizzato per definire l&#39;allineamento tra un&#39;immagine filigrana e l&#39;immagine composita a cui è applicata la filigrana.) Si applica indipendentemente dall’impostazione del livello corrente. Ignorato se solo uno di `wid=` e `hei=` è specificato e quando `fit=constrain` o `fit=stretch`.

## Predefinito {#section-8a9ceff3dcc844c3af23b1c9066dac79}

`align=0,0`, che centra l’immagine nel rettangolo di visualizzazione.

## Esempio {#section-2c9447aa2e184fb8ab1a4370dc61d554}

La richiesta seguente si inserisce `myImage` in un rettangolo di visualizzazione di 200x200 pixel.

`http://server/myRootId/myImageId?wid=200&hei=200&align=0,-1`

Se `myImage` è esattamente quadrato, riempie l’intero rettangolo di visualizzazione. Se `myImage` ha proporzioni verticali, viene ridimensionato per essere alto 200 pixel e centrato orizzontalmente nella vista. Se `myImage` ha proporzioni orizzontali, viene ridimensionato per essere largo 200 pixel e viene allineato al bordo superiore della visualizzazione. In tutti i casi, l&#39;immagine restituita ha esattamente una dimensione di 200x200 pixel; qualsiasi spazio non coperto dal ridimensionamento `myImage` viene riempito con `attribute::BkgColor` (specificate bgc= per controllare il colore di sfondo in modo dinamico).

## Consultate anche {#section-28b42c6db199456a800c8407faa26a99}

[wid=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-wid.md#reference-bfeadcb67bf4485f851eb21345527e47) , [hei=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-hei.md#reference-6d6f556ccc0e4b98a815e8a5c1944a96), [fit=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-fit.md#reference-f11bff6d93d143d6b135de3a923bc989), [bgc=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bgc.md#reference-53376175f617446fbe5c69120f834b88), [Watermarks](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-watermarks.md#reference-35d2c3a2c98349b792921c6cb8e73832)
