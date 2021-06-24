---
description: Maschera immagine. Specifica un'immagine separata della maschera da utilizzare come maschera non associata.
solution: Experience Manager
title: maschera
feature: Dynamic Media Classic, SDK/API
role: Developer,Business Practitioner
exl-id: 5785844b-945b-4dd0-ac59-efbf1360b7cd
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '346'
ht-degree: 1%

---

# maschera{#mask}

Maschera immagine. Specifica un&#39;immagine separata della maschera da utilizzare come maschera non associata.

`mask= *``*|{[is|ir]'{' *`objectnidificatoRequest`*'}'}`

<table id="simpletable_F5A8CD8D7E9B48DAB3C8184E8FE60D9B"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> oggetto</span> </p></td> 
  <td class="stentry"> <p>Oggetto immagine da utilizzare come immagine o maschera di livello. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> nidificateRequest</span> </p></td> 
  <td class="stentry"> <p>Servizio immagini nidificato, Image Rendering o richiesta esterna. </p></td> 
 </tr> 
</table>

*`object`* può essere una voce di catalogo o un file image/SVG. Può essere specificato per i livelli immagine e i livelli a colori solidi.

Se *`object`* viene risolto in una voce di catalogo immagini, viene utilizzato `catalog::MaskPath` oppure, se `catalog::MaskPath` non è definito, viene utilizzato `catalog::Path`. Se *`object`* non viene risolto in una voce di catalogo, viene interpretato come un percorso di file.

In tutti i casi, se l&#39;immagine sorgente ha un canale alfa, viene utilizzata. In caso contrario, l’immagine viene convertita in scala di grigi, se necessario, prima di utilizzarla come maschera di livello.

Se una maschera è collegata a un livello di colore solido, può essere ritagliata e ridimensionata utilizzando le stesse regole utilizzate per le immagini nei livelli immagine. `size=`,  `scale=` o  `res=` può essere utilizzato per ridimensionare la maschera.

Le maschere di livello possono essere specificate anche sotto forma di *`nestedRequest`*. Le richieste nidificate o incorporate sono racchiuse da parentesi graffe. Aggiungi il prefisso `is` a una richiesta di Image Rendering incorporata e `ir` a una richiesta di Image Rendering incorporata. Se non viene specificato alcun prefisso, si assume una richiesta a un server esterno. Per ulteriori informazioni, consulta [Richiedi nidificazione e incorporamento](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-request-nesting-and-embedding.md#reference-38ec66d4062046589e16c39bf1c6049b) .

## Proprietà {#section-a093043dc249423b8ae322cefb0d545d}

Attributo immagine o livello. Si applica al livello 0 se `layer=comp`. Ignorato dai livelli di effetto.

*`object`* non deve risolvere in un record di catalogo che include un  `src=` comando  `mask=` o in  `catalog::Modifier`.

I prefissi `is` e `ir` non fanno distinzione tra maiuscole e minuscole.

## Predefinito {#section-10cf793c665f49deb1b248faa3b618a9}

Se `mask=` non è specificato esplicitamente e se l&#39;immagine di livello è associata a una voce di catalogo, viene utilizzato `catalog::MaskPath`. In caso contrario, viene utilizzato il canale alfa dell&#39;immagine del livello, se presente. Se non esiste un canale alfa, il livello non ha una maschera e il rettangolo del livello viene reso completamente opaco.

## Esempio {#section-1bbe623f7c744bdf97b596458d8e7ea3}

Utilizza diverse maschere separate per colorare diverse aree di un’immagine. Le aree colorate e mascherate vengono sovrapposte all&#39;immagine originale e non modificata:

`http://server/myRootId/myImageId?wid=500& layer=1&src=myImageId&mask=myMask1&op_colorize=200,0,0& layer=2&src=myImageId&mask=myMask2&op_colorize=0,200,0& layer=3&src=myImageId&mask=myMask3&op_colorize=0,0,200`

## Consultate anche {#section-7ed5201d91594e5f872438a92eaf1c89}

[maskUse=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-maskuse.md#reference-9bb1fb5eee4a4bd38f33dadc1a752464) ,  [catalog::MaskPath](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-maskpath-cat.md),  [oggetto](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-object.md#reference-2591bd24548d462782c68d138ef795a0) ,  [Request Nesting and Embedding](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-request-nesting-and-embedding.md#reference-38ec66d4062046589e16c39bf1c6049b)
