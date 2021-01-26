---
description: Immagine del livello.
seo-description: Immagine del livello.
seo-title: src
solution: Experience Manager
title: src
topic: Dynamic Media Image Serving - Image Rendering API
uuid: b4396848-b992-4371-a8ae-4ff1781ae1be
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '194'
ht-degree: 2%

---


# src{#src}

Immagine del livello.

` src= *``*|{[is|ir|fxg]'{' *`objectnidificatedRequest`*'}'}`

<table id="simpletable_59104309B8284B21ABCE7DC95BF5A273"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> object  </span> </p> </td> 
  <td class="stentry"> <p>Oggetto immagine. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> nidificateRequest  </span> </p> </td> 
  <td class="stentry"> <p>Image Server nidificato, Image Rendering o richiesta esterna. </p> </td> 
 </tr> 
</table>

## Descrizione {#section-59ec6dc2afcb43efb34dbb0f7733543f}

Specifica l’immagine sorgente per un livello immagine.

*`object`* può essere una voce di catalogo o un file immagine/SVG.

Vedere [oggetto](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-object.md#reference-2591bd24548d462782c68d138ef795a0).

Le richieste nidificate o incorporate sono racchiuse tra parentesi graffe. Prefissate una richiesta di Image Server incorporata con `is`, una richiesta di rendering immagine incorporata con `ir` e una richiesta di rendering di immagini FXG con `fxg`. Se non viene specificato alcun prefisso, si assume una richiesta a un server esterno.

Vedere [Richiedi nidificazione e incorporazione](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-request-nesting-and-embedding.md#reference-38ec66d4062046589e16c39bf1c6049b).

## Proprietà {#section-2c22bb89a35d470f833df8ba898efd93}

Attributo layer. Si applica a `layer=0` se `layer=comp`. Esclusivo reciproco con `text=` e `textPs=` nello stesso livello; l&#39;ultima occorrenza di `text=`, `textPs=` o `src=` prevale e determina se si tratta di un&#39;immagine o di un livello di testo. Ignorato dai livelli degli effetti.

*`object`*potrebbe non essere risolto in un altro record di catalogo che include un comando `src=` o `mask=` nel relativo `catalog::Modifier`. Utilizzate la nidificazione delle richieste per ottenere un effetto simile.

I prefissi `is`, `ir` e `fxg` fanno distinzione tra maiuscole e minuscole.

## Predefinito {#section-a92f3882041b4d43ae2caf014647165f}

Per il livello 0, l&#39;oggetto del componente percorso dell&#39;URL viene utilizzato se `src=` non è specificato. Nessun valore predefinito per altri livelli.

## Consultate anche {#section-e467e03330564796932ac081f1c9c1d0}

[catalogo::](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-path-cat.md) ,  [attributo::RootPath](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md#reference-17d57e5967be403b8408fa7214017494),  [text=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-text.md#reference-84634052e48548539a1ef63cbe41f22f),  [textPs=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textps.md#reference-4209a2a6169f44278da2647cfb0cd767),  [mask=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-mask.md#reference-922254e027404fb890b850e2723ee06e),  [ ](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-object.md#reference-2591bd24548d462782c68d138ef795a0)  [ ](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e)  [object, TemplatePath, Nesting e Incorporazione delle richieste](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-request-nesting-and-embedding.md#reference-38ec66d4062046589e16c39bf1c6049b)
