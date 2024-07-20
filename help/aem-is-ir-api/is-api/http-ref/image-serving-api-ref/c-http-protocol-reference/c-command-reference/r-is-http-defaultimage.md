---
title: defaultImage
description: Immagine di risposta predefinita. Specifica l'immagine o la voce di catalogo da utilizzare quando non è possibile trovare un'immagine.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 741833b5-e858-4aa5-96c1-bb06539deef3
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '218'
ht-degree: 1%

---

# defaultImage{#defaultimage}

Immagine di risposta predefinita. Specifica l&#39;immagine o la voce di catalogo da utilizzare quando non è possibile trovare un&#39;immagine.

` defaultImage= *`oggetto`*`

<table id="simpletable_C1FC14B7D9AE476DB2B10EB402944335"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> oggetto </span> </span> </p> </td> 
  <td class="stentry"> <p>Oggetto immagine. </p> </td> 
 </tr> 
</table>

*`object`* può essere una voce di catalogo (incluso un modello) o un semplice percorso di file di immagine. Utile per sostituire le immagini mancanti con quelle predefinite. Questo valore sostituisce il valore del catalogo corrispondente `attribute::DefaultImage`. Un valore vuoto ( `defaultImage=`) disabilita la gestione dell&#39;immagine predefinita.

>[!NOTE]
>
>Il meccanismo di immagine predefinito non si applica agli oggetti SVG. Se non è possibile trovare l’oggetto SVG specificato nella richiesta, viene restituito un errore.

Se `attribute::DefaultImageMode=0`, *`object`* sostituisce l&#39;intera richiesta originale, anche se manca una sola immagine in una composizione con più immagini. Gli unici comandi mantenuti dalla richiesta originale sono: `wid=`, `hei=`, `fmt=`, `qlt=`.

Se `attribute::DefaultImageMode=1`, l&#39;oggetto sostituisce solo l&#39;immagine di livello mancante; gli attributi per il livello mancante vengono applicati e il composito viene elaborato e restituito come di consueto.

## Proprietà {#section-d30923d8dc4042eba10989212dd70887}

Attributo della richiesta. Si applica indipendentemente dall&#39;impostazione del livello corrente. Ignorato se `req=` è diverso da `img` o `tmb`.

## Restrizioni {#section-30df31bc8cac41cd917f1e45196779c2}

Le sorgenti di immagine esterne non sono coperte dal meccanismo di immagine predefinito; se una sorgente di immagine esterna non è valida, viene restituito un errore.

Image Server torna a `DefaultImageMode=0` se le richieste di rendering immagini o FXG nidificate non riescono.

## Predefinito {#section-0676c66b233c46a3a3a1517da4ace998}

`attribute::DefaultImage`.

## Consultate anche {#section-745392143c3747a2955e1ae561f58e5f}

[attributo::DefaultImageMode](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultimagemode.md#reference-8a996af162f84e46bbe9e6e0d4e26782) , [attributo: DefaultImage](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-is-cat-defaultimage.md#reference-8e9900e129f54ed68462a3c2fc3bc433), [src=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-src.md#reference-f6506637778c4c69bf106a7924a91ab1), [*`object`*](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-object.md#reference-2591bd24548d462782c68d138ef795a0)
