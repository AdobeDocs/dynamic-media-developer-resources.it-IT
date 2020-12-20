---
description: Immagine risposta predefinita. Specifica l’immagine o la voce di catalogo da utilizzare quando non è possibile trovare un’immagine.
seo-description: Immagine risposta predefinita. Specifica l’immagine o la voce di catalogo da utilizzare quando non è possibile trovare un’immagine.
seo-title: defaultImage
solution: Experience Manager
title: defaultImage
topic: Scene7 Image Serving - Image Rendering API
uuid: 7478325c-9ac5-4b85-a4c5-5c495f924eb5
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '237'
ht-degree: 1%

---


# defaultImage{#defaultimage}

Immagine risposta predefinita. Specifica l’immagine o la voce di catalogo da utilizzare quando non è possibile trovare un’immagine.

` defaultImage= *`object`*`

<table id="simpletable_C1FC14B7D9AE476DB2B10EB402944335"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> object  </span> </span> </p> </td> 
  <td class="stentry"> <p>Oggetto immagine. </p> </td> 
 </tr> 
</table>

*`object`* può essere una voce di catalogo (incluso un modello) o un semplice percorso di file immagine. Utile per sostituire le immagini mancanti con immagini predefinite. Questo valore sostituisce il valore del catalogo corrispondente `attribute::DefaultImage`. Un valore vuoto ( `defaultImage=`) disattiva la gestione predefinita delle immagini.

>[!NOTE]
>
>Il meccanismo predefinito per le immagini non si applica agli oggetti SVG. Se non è possibile trovare l&#39;oggetto SVG specificato nella richiesta, viene restituito un errore.

Se `attribute::DefaultImageMode=0`, *`object`* sostituisce l&#39;intera richiesta originale, anche se manca solo un&#39;immagine in una composizione con più immagini. Gli unici comandi conservati dalla richiesta originale sono: `wid=`, `hei=`, `fmt=`, `qlt=`.

Se `attribute::DefaultImageMode=1`, l&#39;oggetto sostituisce solo l&#39;immagine del livello mancante; gli attributi per il livello mancante vengono applicati e il composito viene elaborato e restituito come al solito.

## Proprietà {#section-d30923d8dc4042eba10989212dd70887}

Attributo di richiesta. Si applica indipendentemente dall’impostazione del livello corrente. Ignorato se `req=` è diverso da `img` o `tmb`.

## Restrizioni {#section-30df31bc8cac41cd917f1e45196779c2}

Le sorgenti di immagine esterne non sono coperte dal meccanismo di immagine predefinito; viene restituito un errore se un&#39;origine immagine esterna non è valida.

Image Serving torna a `DefaultImageMode=0` quando le richieste di rendering delle immagini nidificate o FXG non vanno a buon fine.

## Predefinito {#section-0676c66b233c46a3a3a1517da4ace998}

`attribute::DefaultImage`.

## Consultate anche {#section-745392143c3747a2955e1ae561f58e5f}

[attribute::DefaultImageMode](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultimagemode.md#reference-8a996af162f84e46bbe9e6e0d4e26782) ,  [attribute: DefaultImage](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-is-cat-defaultimage.md#reference-8e9900e129f54ed68462a3c2fc3bc433),  [src=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-src.md#reference-f6506637778c4c69bf106a7924a91ab1),  [ *`object`* ](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-object.md#reference-2591bd24548d462782c68d138ef795a0)
