---
title: src
description: Immagine livello.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 88b89e70-59cf-4fb9-bbe7-0ac5eff792f1
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '191'
ht-degree: 2%

---

# src{#src}

Immagine livello.

` src= *`oggetto`*|{[is|ir|fxg]'{' *`nestedRequest`*'}'}`

<table id="simpletable_59104309B8284B21ABCE7DC95BF5A273"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> oggetto </span> </p> </td> 
  <td class="stentry"> <p>Oggetto immagine. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> nestedRequest </span> </p> </td> 
  <td class="stentry"> <p>Server immagini nidificate, Image Rendering o richiesta esterna. </p> </td> 
 </tr> 
</table>

## Descrizione {#section-59ec6dc2afcb43efb34dbb0f7733543f}

Specifica l&#39;immagine di origine per un livello immagine.

*`object`* può essere una voce di catalogo o un file immagine/SVG.

Consulta [oggetto](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-object.md#reference-2591bd24548d462782c68d138ef795a0).

Le richieste nidificate o incorporate sono racchiuse tra parentesi graffe. Aggiungi il prefisso &quot;&quot; a una richiesta Image Server incorporata `is`, una richiesta di Image Rendering incorporata con `ir`, e una richiesta di rendering della grafica FXG con `fxg`. Se non viene specificato alcun prefisso, viene utilizzata una richiesta a un server esterno.

Consulta [Richiedi nidificazione e incorporamento](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-request-nesting-and-embedding.md#reference-38ec66d4062046589e16c39bf1c6049b).

## Proprietà {#section-2c22bb89a35d470f833df8ba898efd93}

Attributo livello. Applicabile a `layer=0` se `layer=comp`. Reciprocamente esclusivo con `text=` e `textPs=` nello stesso livello; l&#39;ultima occorrenza di `text=`, `textPs=`, o `src=` prevale e determina se si tratta di un livello immagine o testo. Ignorato dai livelli degli effetti.

*`object`*potrebbe non risolvere un altro record catalogo che include `src=` o `mask=` comando nel relativo `catalog::Modifier`. Per ottenere un effetto simile, utilizza la nidificazione delle richieste.

Il `is`, `ir`, e `fxg` i prefissi distinguono tra maiuscole e minuscole.

## Predefinito {#section-a92f3882041b4d43ae2caf014647165f}

Per il livello 0 viene utilizzato l&#39;oggetto del componente percorso dell&#39;URL se `src=` non è specificato. Nessun valore predefinito per gli altri livelli.

## Consultate anche {#section-e467e03330564796932ac081f1c9c1d0}

[catalog::Path](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-path-cat.md) , [attribute::RootPath](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md#reference-17d57e5967be403b8408fa7214017494), [text= Testo](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-text.md#reference-84634052e48548539a1ef63cbe41f22f), [textPs=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textps.md#reference-4209a2a6169f44278da2647cfb0cd767), [mask= maschera](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-mask.md#reference-922254e027404fb890b850e2723ee06e), [oggetto](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-object.md#reference-2591bd24548d462782c68d138ef795a0), [Modelli](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e), [Richiedi nidificazione e incorporamento](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-request-nesting-and-embedding.md#reference-38ec66d4062046589e16c39bf1c6049b)
