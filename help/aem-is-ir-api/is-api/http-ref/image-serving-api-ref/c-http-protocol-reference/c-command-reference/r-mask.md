---
title: maschera
description: Maschera immagine. Specifica un'immagine maschera separata da utilizzare come maschera non associata.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 5785844b-945b-4dd0-ac59-efbf1360b7cd
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '342'
ht-degree: 1%

---

# maschera{#mask}

Maschera immagine. Specifica un&#39;immagine maschera separata da utilizzare come maschera non associata.

`mask= *`object`*|{[is|ir]'{' *`nestedRequest`*'}'}`

<table id="simpletable_F5A8CD8D7E9B48DAB3C8184E8FE60D9B"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> oggetto</span> </p></td> 
  <td class="stentry"> <p>Oggetto immagine da utilizzare come immagine o maschera di livello. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> nestedRequest</span> </p></td> 
  <td class="stentry"> <p>Server immagini nidificate, Image Rendering o richiesta esterna. </p></td> 
 </tr> 
</table>

*`object`* può essere una voce di catalogo o un file immagine/SVG. Può essere specificato per i livelli immagine e i livelli colore in tinta unita.

Se *`object`* viene risolto in una voce del catalogo immagini, viene utilizzato `catalog::MaskPath` oppure, se `catalog::MaskPath` non è definito, viene utilizzato `catalog::Path`. Se *`object`* non viene risolto in una voce di catalogo, viene interpretato come un percorso di file.

In tutti i casi, se l&#39;immagine sorgente ha un canale alfa, viene utilizzata. In caso contrario, l&#39;immagine viene convertita in scala di grigio, se necessario, prima di utilizzarla come maschera di livello.

Se una maschera è attaccata a un livello di colore in tinta unita, può essere ritagliata e ridimensionata utilizzando le stesse regole utilizzate per le immagini nei livelli immagine. È possibile usare `size=`, `scale=` o `res=` per ridimensionare la maschera.

È inoltre possibile specificare le maschere di livello sotto forma di *`nestedRequest`*. Le richieste nidificate o incorporate sono racchiuse tra parentesi graffe. Aggiungi il prefisso `is` a una richiesta Image Server incorporata e `ir` a una richiesta Image Rendering incorporata. Se non viene specificato alcun prefisso, viene utilizzata una richiesta a un server esterno. Per ulteriori informazioni, consulta [Annidamento e incorporamento richieste](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-request-nesting-and-embedding.md#reference-38ec66d4062046589e16c39bf1c6049b).

## Proprietà {#section-a093043dc249423b8ae322cefb0d545d}

Attributo immagine o livello. Si applica al livello 0 se `layer=comp`. Ignorato dai livelli degli effetti.

*`object`* non deve essere risolto in un record di catalogo che include un comando `src=` o `mask=` in `catalog::Modifier`.

I prefissi `is` e `ir` non distinguono tra maiuscole e minuscole.

## Predefinito {#section-10cf793c665f49deb1b248faa3b618a9}

Se `mask=` non è specificato in modo esplicito e l&#39;immagine del livello è associata a una voce di catalogo, viene utilizzato `catalog::MaskPath`. In caso contrario, viene utilizzato il canale alfa dell&#39;immagine di livello, se presente. Se non è presente alcun canale alfa, il livello non ha maschera e il rettangolo del livello viene reso completamente opaco.

## Esempio {#section-1bbe623f7c744bdf97b596458d8e7ea3}

Utilizzate diverse maschere separate per colorare diverse aree di un&#39;immagine. Le regioni colorate e mascherate sono sovrapposte all&#39;immagine originale non modificata:

`http://server/myRootId/myImageId?wid=500& layer=1&src=myImageId&mask=myMask1&op_colorize=200,0,0& layer=2&src=myImageId&mask=myMask2&op_colorize=0,200,0& layer=3&src=myImageId&mask=myMask3&op_colorize=0,0,200`

## Consultate anche {#section-7ed5201d91594e5f872438a92eaf1c89}

[maskUse=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-maskuse.md#reference-9bb1fb5eee4a4bd38f33dadc1a752464) , [catalogo::MaskPath](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-maskpath-cat.md), [oggetto](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-object.md#reference-2591bd24548d462782c68d138ef795a0) , [Annidamento e incorporamento richieste](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-request-nesting-and-embedding.md#reference-38ec66d4062046589e16c39bf1c6049b)
