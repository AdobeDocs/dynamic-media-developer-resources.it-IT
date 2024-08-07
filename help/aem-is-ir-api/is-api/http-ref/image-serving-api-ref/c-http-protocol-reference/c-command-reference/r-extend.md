---
title: estendere
description: Estendere il livello. Aggiunge margini a un livello o ritaglia il rettangolo del livello.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 03db6555-6851-49d4-b0de-5570bf56ad76
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '233'
ht-degree: 1%

---

# estendere{#extend}

Estendere il livello. Aggiunge margini a un livello o ritaglia il rettangolo del livello.

`extend= *`left`*, *`top`*, *`right`*, *`bottom`*`

`extendN= *`leftN`*, *`topN`*, *`rightN`*, *`bottomN`*`

<table id="simpletable_1DCCD469712B423C8154630127DC5F54"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> sinistra,alto,basso,destra</span></span> </p></td> 
  <td class="stentry"> <p>Numero di pixel da aggiungere (o rimuovere, se il valore è negativo) al bordo sinistro, superiore, destro e inferiore del rettangolo di livello (int, int, int, int). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> leftN,topN,bottomN,rightN</span></span> </p></td> 
  <td class="stentry"> <p>Quantità di spazio da aggiungere (o rimuovere, se il valore è negativo) al bordo sinistro, superiore, destro e inferiore del rettangolo di livello, espressa come quantità normalizzate relative alle dimensioni del rettangolo di livello originale (reale, reale, reale, reale). </p></td> 
 </tr> 
</table>

`extend=` è applicato al livello *dopo* che l&#39;immagine è ritagliata (`crop=`) e tutte le trasformazioni di livello, incluso `rotate=`, sono state applicate.

L&#39;area estesa è riempita con `bgColor=` oppure, se non specificato, rimane trasparente.

I valori dell&#39;argomento per `extendN=` sono normalizzati in relazione alle dimensioni del rettangolo di livello dopo l&#39;applicazione delle trasformazioni di livello, incluso `rotate=`.

## Proprietà {#section-8fc94de871f841f3bf5e1df135972ca9}

Attributo livello. Si applica al livello 0 se `layer=comp`. Ignorato dai livelli degli effetti.

## Predefinito {#section-de7473649cb9406b8d99028c74c4b8dc}

`extend=0,0,0,0`, per nessuna modifica del rettangolo del livello.

## Esempi {#section-cc6d8e76f3dd4607ac31cb095d86c9fe}

**Ritagliare un&#39;immagine, quindi aggiungere un bordo rosso di 5 pixel:**

`…&cropN=.2,.3,.8,.9&extend=5,5,5,5&bgColor=255,0,0&…`

**Ridimensionare un&#39;immagine a una larghezza di 200 pixel e aggiungere il testo del titolo in un margine di 30 pixel sopra l&#39;immagine.**

L&#39;altezza dell&#39;immagine composita varia a seconda delle proporzioni dell&#39;immagine.

`http://server/myRootId/myImageId?size=200,0&extend=0,30,0,0&origin=0,0 layer=1&text=title-text&origin=0,0`

## Consultate anche {#section-2d9572be32ca4602b60920b3810f3638}

[ritaglio=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-crop.md#reference-6fd0f6399966446ab4425ce050572eab) , [colore=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md), [dimensione=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-size.md#reference-04d383f32c7b4003bed9978cb854747b), [origine=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-origin.md#reference-e11c7ac06e2240cc884c3fec98f05138), [percorsoClip=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clippath.md#reference-8139b1b52dc54749b51b109521ddf83d)
