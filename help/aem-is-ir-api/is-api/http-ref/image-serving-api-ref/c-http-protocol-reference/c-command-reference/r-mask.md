---
description: Maschera immagine. Specifica un'immagine maschera separata da usare come maschera non associata.
seo-description: Maschera immagine. Specifica un'immagine maschera separata da usare come maschera non associata.
seo-title: mask
solution: Experience Manager
title: mask
topic: Scene7 Image Serving - Image Rendering API
uuid: 2dc14d20-f02a-4a77-9b73-0c01e10d448d
translation-type: tm+mt
source-git-commit: fe557a2429ceb7b48f22b9cbef5820ad39bad69f

---


# mask{#mask}

Maschera immagine. Specifica un&#39;immagine maschera separata da usare come maschera non associata.

`mask= *``*|{[is|ir]'{' *`objectnidificatedRequest`*'}'}`

<table id="simpletable_F5A8CD8D7E9B48DAB3C8184E8FE60D9B"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> object</span> </p></td> 
  <td class="stentry"> <p>Oggetto immagine da usare come immagine o maschera di livello. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> nidificateRequest</span> </p></td> 
  <td class="stentry"> <p>Image Server nidificato, Image Rendering o richiesta esterna. </p></td> 
 </tr> 
</table>

*`object`* può essere una voce di catalogo o un file immagine/SVG. Può essere specificato per i livelli delle immagini e dei colori in tinta unita.

Se *`object`* viene risolta una voce di catalogo immagini, `catalog::MaskPath` viene utilizzata, o, se non `catalog::MaskPath` è definita, `catalog::Path` viene utilizzata. Se *`object`* non si risolve in una voce di catalogo, questa viene interpretata come un percorso di file.

In tutti i casi, se l&#39;immagine sorgente ha un canale alfa, viene utilizzata. In caso contrario, l’immagine viene convertita in scala di grigio, se necessario, prima di utilizzarla come maschera di livello.

Se una maschera è collegata a un livello in tinta unita, può essere ritagliata e ridimensionata utilizzando le stesse regole utilizzate per le immagini nei livelli delle immagini. `size=`, `scale=`oppure `res=` può essere utilizzato per ridimensionare la maschera.

Le maschere di livello possono essere specificate anche sotto forma di *`nestedRequest`*. Le richieste nidificate o incorporate sono racchiuse tra parentesi graffe. Aggiungete un prefisso a una richiesta Image Server incorporata con `is` e una richiesta di rendering immagine incorporata con `ir`. Se non viene specificato alcun prefisso, si assume una richiesta a un server esterno. Per informazioni dettagliate, consultate [Richiedi nidificazione e incorporamento](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-request-nesting-and-embedding.md#reference-38ec66d4062046589e16c39bf1c6049b) .

## Proprietà {#section-a093043dc249423b8ae322cefb0d545d}

Attributo immagine o livello. Si applica al livello 0 se `layer=comp`. Ignorato dai livelli degli effetti.

*`object`* non deve risolvere un record catalogo che include un `src=` comando o un `mask=` comando in `catalog::Modifier`.

I `is` prefissi e `ir` i prefissi non fanno distinzione tra maiuscole e minuscole.

## Predefinito {#section-10cf793c665f49deb1b248faa3b618a9}

Se `mask=` non viene specificato esplicitamente e se l’immagine del livello è associata a una voce di catalogo, `catalog::MaskPath` viene utilizzata. In caso contrario, viene utilizzato il canale alfa dell’immagine del livello, se presente. Se non è presente un canale alfa, il livello non ha una maschera e il rettangolo del livello viene rappresentato completamente opaco.

## Esempio {#section-1bbe623f7c744bdf97b596458d8e7ea3}

Usate diverse maschere separate per colorare diverse aree di un’immagine. Le aree colorate e mascherate vengono sovrapposte all’immagine originale e non modificata:

`http://server/myRootId/myImageId?wid=500& layer=1&src=myImageId&mask=myMask1&op_colorize=200,0,0& layer=2&src=myImageId&mask=myMask2&op_colorize=0,200,0& layer=3&src=myImageId&mask=myMask3&op_colorize=0,0,200`

## Consultate anche {#section-7ed5201d91594e5f872438a92eaf1c89}

[maskUse=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-maskuse.md#reference-9bb1fb5eee4a4bd38f33dadc1a752464) , [catalog::MaskPath](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-maskpath-cat.md), [oggetto](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-object.md#reference-2591bd24548d462782c68d138ef795a0) , [Request Nesting and Embedding](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-request-nesting-and-embedding.md#reference-38ec66d4062046589e16c39bf1c6049b)
