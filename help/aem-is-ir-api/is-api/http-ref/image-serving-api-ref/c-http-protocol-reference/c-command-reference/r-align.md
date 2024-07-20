---
title: allinea
description: Allinea immagine con vista. Allinea l'immagine composita (possibilmente dopo il ridimensionamento, se è specificato anche scl=) all'interno del rettangolo di visualizzazione definito da wid= e hei=.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 01001cc6-1a60-4d6b-a27f-ea5822be6d11
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '274'
ht-degree: 1%

---

# allinea{#align}

Allinea immagine con vista. Allinea l&#39;immagine composita (possibilmente dopo il ridimensionamento, se è specificato anche scl=) all&#39;interno del rettangolo di visualizzazione definito da wid= e hei=.

` align= *`horiz`*, *`vert`*`

<table id="simpletable_4CB26F72A56D4515B767C303F8E8A1CF"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> oriz </span> </span> </p> </td> 
  <td class="stentry"> <p>allineamento orizzontale (reale, -1,0, 1,0) </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> vert </span> </span> </p> </td> 
  <td class="stentry"> <p>allineamento verticale (reale, -1,0...1,0) </p> </td> 
 </tr> 
</table>

Specificare `align=-1,-1` per allineare la parte superiore sinistra dell&#39;immagine composita alla parte superiore sinistra della visualizzazione. Specificare `align=1,1` per allineare la parte inferiore destra dell&#39;immagine alla parte inferiore destra della visualizzazione. Per le richieste di immagini e miniature standard, qualsiasi area della visualizzazione non coperta da dati immagine compositi viene riempita con `bgc=`.

## Proprietà {#section-3fbec8206fc944eda4746d8be84f3b41}

Visualizza attributo. ( `align=` viene utilizzato anche per definire l&#39;allineamento tra un&#39;immagine della filigrana e l&#39;immagine composita a cui viene applicata la filigrana.) Si applica indipendentemente dall&#39;impostazione del livello corrente. Ignorato se viene specificato solo uno di `wid=` e `hei=` e quando `fit=constrain` o `fit=stretch`.

## Predefinito {#section-8a9ceff3dcc844c3af23b1c9066dac79}

`align=0,0`, che centra l&#39;immagine nel rettangolo di visualizzazione.

## Esempio {#section-2c9447aa2e184fb8ab1a4370dc61d554}

La richiesta seguente inserisce `myImage` in un rettangolo di visualizzazione di 200x200 pixel.

`http://server/myRootId/myImageId?wid=200&hei=200&align=0,-1`

Se `myImage` è esattamente quadrato, riempie l&#39;intero rettangolo di visualizzazione. Se `myImage` ha proporzioni verticali, viene ridimensionato in modo da raggiungere un&#39;altezza di 200 pixel e centrato orizzontalmente nella visualizzazione. Se `myImage` ha proporzioni orizzontali, viene ridimensionato per essere largo 200 pixel e allineato al bordo superiore della visualizzazione. In tutti i casi, l&#39;immagine restituita è esattamente di 200x200 pixel; qualsiasi spazio non coperto dal ridimensionamento `myImage` viene riempito con `attribute::BkgColor` (specificare bgc= per controllare dinamicamente il colore di sfondo).

## Consultate anche {#section-28b42c6db199456a800c8407faa26a99}

[wid=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-wid.md#reference-bfeadcb67bf4485f851eb21345527e47) , [hei=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-hei.md#reference-6d6f556ccc0e4b98a815e8a5c1944a96), [fit=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-fit.md#reference-f11bff6d93d143d6b135de3a923bc989), [bgc=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bgc.md#reference-53376175f617446fbe5c69120f834b88), [filigrane](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-watermarks.md#reference-35d2c3a2c98349b792921c6cb8e73832)
