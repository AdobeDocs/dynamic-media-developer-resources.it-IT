---
description: Allinea immagine con vista. Allinea l’immagine composita (possibilmente dopo il ridimensionamento, se è specificato anche scl=) all’interno del rettangolo di visualizzazione definito da wid= e hei=.
seo-description: Allinea immagine con vista. Allinea l’immagine composita (possibilmente dopo il ridimensionamento, se è specificato anche scl=) all’interno del rettangolo di visualizzazione definito da wid= e hei=.
seo-title: allinea
solution: Experience Manager
title: allinea
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 91940bd4-8e2b-4949-a76d-31cd238783bc
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '295'
ht-degree: 1%

---


# align{#align}

Allinea immagine con vista. Allinea l’immagine composita (possibilmente dopo il ridimensionamento, se è specificato anche scl=) all’interno del rettangolo di visualizzazione definito da wid= e hei=.

` align= *``*, *`orizzonte`*`

<table id="simpletable_4CB26F72A56D4515B767C303F8E8A1CF"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> horiz  </span> </span> </p> </td> 
  <td class="stentry"> <p>allineamento orizzontale (reale, -1.0...1.0) </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> vert  </span> </span> </p> </td> 
  <td class="stentry"> <p>allineamento verticale (reale, -1.0...1.0) </p> </td> 
 </tr> 
</table>

Specificate `align=-1,-1` per allineare l&#39;angolo superiore sinistro dell&#39;immagine composita con l&#39;angolo superiore sinistro della vista, `align=1,1` per allineare l&#39;angolo inferiore destro dell&#39;immagine con quello inferiore destro della vista. Per le richieste standard di immagini e miniature, qualsiasi area della visualizzazione non coperta da dati di immagini composite viene riempita con `bgc=`.

## Proprietà {#section-3fbec8206fc944eda4746d8be84f3b41}

Visualizza attributo. ( `align=` è anche utilizzato per definire l&#39;allineamento tra un&#39;immagine filigrana e l&#39;immagine composita a cui viene applicata la filigrana.) Si applica indipendentemente dall’impostazione del livello corrente. Ignorato se è specificato solo uno dei `wid=` e `hei=` e quando `fit=constrain` o `fit=stretch`.

## Predefinito {#section-8a9ceff3dcc844c3af23b1c9066dac79}

`align=0,0`, che centra l’immagine nel rettangolo di visualizzazione.

## Esempio {#section-2c9447aa2e184fb8ab1a4370dc61d554}

La richiesta seguente si adatta a `myImage` in un rettangolo di visualizzazione di 200x200 pixel.

`http://server/myRootId/myImageId?wid=200&hei=200&align=0,-1`

Se `myImage` è esattamente quadrato, riempie l&#39;intero rettangolo di visualizzazione. Se `myImage` ha proporzioni verticali, viene ridimensionato per essere alto 200 pixel e viene centrato orizzontalmente nella vista. Se `myImage` ha proporzioni orizzontali, viene ridimensionata per essere larga 200 pixel ed è allineata al bordo superiore della vista. In tutti i casi, l&#39;immagine restituita ha esattamente una dimensione di 200x200 pixel; tutti gli spazi non coperti dalla scala `myImage` vengono riempiti con `attribute::BkgColor` (specificate bgc= per controllare il colore di sfondo in modo dinamico).

## Consultate anche {#section-28b42c6db199456a800c8407faa26a99}

[wid=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-wid.md#reference-bfeadcb67bf4485f851eb21345527e47) ,  [hei=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-hei.md#reference-6d6f556ccc0e4b98a815e8a5c1944a96),  [fit=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-fit.md#reference-f11bff6d93d143d6b135de3a923bc989),  [bgc=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bgc.md#reference-53376175f617446fbe5c69120f834b88),  [Watermarks](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-watermarks.md#reference-35d2c3a2c98349b792921c6cb8e73832)
