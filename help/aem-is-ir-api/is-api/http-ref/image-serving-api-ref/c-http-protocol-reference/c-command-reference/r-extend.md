---
description: Estende il livello. Aggiunge margini a un livello o ritaglia il rettangolo del livello.
solution: Experience Manager
title: estendere
feature: Dynamic Media Classic, SDK/API
role: Developer,Business Practitioner
exl-id: 03db6555-6851-49d4-b0de-5570bf56ad76
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '240'
ht-degree: 1%

---

# estendere{#extend}

Estende il livello. Aggiunge margini a un livello o ritaglia il rettangolo del livello.

`extend= *``*, *``*, *``*, *`sinistra-destra-basso`*`

`extendN= *``*, *``*, *``*, *`leftNtopNrightNbottomN`*`

<table id="simpletable_1DCCD469712B423C8154630127DC5F54"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> sinistra,superiore,inferiore,destra</span></span> </p></td> 
  <td class="stentry"> <p>Numero di pixel da aggiungere a (o rimuovere da, se il valore è negativo) il bordo sinistro, superiore, destro e inferiore del bordo del livello diretto (int, int, int, int). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> leftN,topN,bottomN,rightN</span></span> </p></td> 
  <td class="stentry"> <p>Quantità di spazio da aggiungere a (o rimuovere da, se il valore è negativo) il bordo sinistro, superiore, destro e inferiore della funzione di correzione del livello, espressa come quantità normalizzate rispetto alle dimensioni della funzione di correzione del livello originale (reale, reale, reale, reale, reale). </p></td> 
 </tr> 
</table>

`extend=` viene applicato al livello  ** dopo il ritaglio dell’immagine (  `crop=`) e tutte le trasformazioni di livello, incluso  `rotate=`, sono state applicate.

L&#39;area estesa viene riempita con `bgColor=` o, se non specificato, rimane trasparente.

I valori dell’argomento per `extendN=` vengono normalizzati rispetto alle dimensioni della correzione del livello dopo l’applicazione delle trasformazioni del livello, incluso `rotate=`.

## Proprietà {#section-8fc94de871f841f3bf5e1df135972ca9}

Attributo livello. Si applica al livello 0 se `layer=comp`. Ignorato dai livelli di effetto.

## Predefinito {#section-de7473649cb9406b8d99028c74c4b8dc}

`extend=0,0,0,0`, senza modificare il rettangolo del livello.

## Esempi {#section-cc6d8e76f3dd4607ac31cb095d86c9fe}

**Ritaglia un’immagine e aggiungi un bordo rosso largo 5 pixel:**

`…&cropN=.2,.3,.8,.9&extend=5,5,5,5&bgColor=255,0,0&…`

**Ridimensiona un’immagine a 200 pixel di larghezza e aggiungi il testo del titolo a un margine di 30 pixel sopra l’immagine.**

L&#39;altezza dell&#39;immagine composita varia a seconda delle proporzioni dell&#39;immagine.

`http://server/myRootId/myImageId?size=200,0&extend=0,30,0,0&origin=0,0 layer=1&text=title-text&origin=0,0`

## Consultate anche {#section-2d9572be32ca4602b60920b3810f3638}

[crop=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-crop.md#reference-6fd0f6399966446ab4425ce050572eab) ,  [color=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md),  [size=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-size.md#reference-04d383f32c7b4003bed9978cb854747b),  [origin=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-origin.md#reference-e11c7ac06e2240cc884c3fec98f05138),  [clipPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clippath.md#reference-8139b1b52dc54749b51b109521ddf83d)
