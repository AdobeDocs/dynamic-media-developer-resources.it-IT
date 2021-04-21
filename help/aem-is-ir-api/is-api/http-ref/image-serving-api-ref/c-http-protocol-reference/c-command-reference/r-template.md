---
description: Modello di composizione. Consente di specificare un modello di composizione posizionato in un catalogo diverso dal catalogo principale.
solution: Experience Manager
title: template
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: ddfccb4ca157764e39fc719d96b63e6ee95304bf
workflow-type: tm+mt
source-wordcount: '172'
ht-degree: 4%

---


# template{#template}

Modello di composizione. Consente di specificare un modello di composizione in un catalogo diverso dal catalogo principale.

`template= *`template`*`

<table id="simpletable_DEC6F4EB460D453B8F272C98C9C8B7E5"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> oggetto</span> </p> </td> 
  <td class="stentry"> <p>Modello. </p></td> 
 </tr> 
</table>

*`template`* deve essere una voce di catalogo immagini con il corpo del modello contenuto in  `catalog::Modifier`.

Quando `template=` è presente, l&#39;oggetto specificato nel percorso della richiesta non viene applicato come origine per il livello 0. Tuttavia, è possibile farvi riferimento come `src=` o `mask=` in qualsiasi punto del modello utilizzando la variabile di percorso predefinita `$object$` come valore `src=`. `catalog::Modifier` dell’oggetto specificato nel percorso della richiesta viene applicato solo con la sostituzione di all’ `$object$` interno del modello, mentre  `catalog::PostModifier` viene sempre applicato.

Il livello 0 è definito nel corpo del modello e può essere un livello di richiesta di immagine, colore solido, testo o nidificato o incorporato.

`catalog:PostModifier` di  *`object`* viene ignorato quando  *`object`* viene utilizzato con  `template=`.

## Predefinito {#section-9de53ea27c4b4fd4811e40e345d8ba05}

Nessuno.

## Proprietà {#section-daf3afb1d09c45a6a394468d0874c439}

Attributo di richiesta. Si applica indipendentemente dall&#39;impostazione del livello corrente.

## Esempio {#section-9a4f260ed43342b186b0fe855f34bca6}

Vedi gli esempi in [Modelli](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e).

## Consultate anche {#section-067587444f774469931ecafd5a39834c}

[oggetto](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-object.md#reference-2591bd24548d462782c68d138ef795a0),  [modelli](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e), variabile di percorso  [predefinita](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-is-http-substitution-variables.md#reference-90dc01aba44940e4acdd0c6476e7aa5a)
