---
description: Consente di regolare l’opacità dell’immagine. Consente di ridurre l’opacità in primo piano di un’immagine, di un testo, di un colore in tinta unita o di un livello di effetto.
seo-description: Consente di regolare l’opacità dell’immagine. Consente di ridurre l’opacità in primo piano di un’immagine, di un testo, di un colore in tinta unita o di un livello di effetto.
seo-title: opac
solution: Experience Manager
title: opac
topic: Scene7 Image Serving - Image Rendering API
uuid: 268279bd-d777-4afe-b175-841af7e55406
translation-type: tm+mt
source-git-commit: 94a26628ec619076f0942e9278165cc591f1c150

---


# opac{#opac}

Consente di regolare l’opacità dell’immagine. Consente di ridurre l’opacità in primo piano di un’immagine, di un testo, di un colore in tinta unita o di un livello di effetto.

`opac= *``*[, *`opacityfillOpacity`*]`

<table id="simpletable_DA4B5D86C496480886FADB284AD6047F"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> opacità</span> </p> </td> 
  <td class="stentry"> <p>Opacità primaria (0...100 int). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> fillOpacity</span> </p></td> 
  <td class="stentry"> <p>Opacità riempimento (0...100 int). </p></td> 
 </tr> 
</table>

L’opacità in primo piano di un livello immagine è determinata dalla maschera di livello o dal canale alfa dell’immagine oppure, se non sono presenti, è del 100%. L’opacità in primo piano di un livello di testo è del 100% e quella di un livello di colore in tinta unita è impostata da `color=`.

`opac=` non modifica mai l’opacità delle aree riempite con `color=` o `bgColor=`, ad eccezione delle aree in primo piano dei livelli di colore tinta unita e degli effetti (impostati con `color=`).

Se specificato in un livello di immagine, testo o colore in tinta unita, *`opacity`* applica l’intero livello, inclusi tutti i livelli di effetto associati, mentre *`fillOpacity`* si applica solo al contenuto del livello principale. Se specificato in un livello di effetto, *`opacity`* viene applicato al livello di effetto, mentre *`fillOpacity`* viene ignorato.

L&#39;opacità effettiva per il contenuto dello strato principale è ( *`opacity`* * *`fillOpacity`* / 100). L&#39;opacità effettiva per i livelli degli effetti è (effetto principale *`opacity`* * *`opacity`* / 100).

## Proprietà {#section-ac3f136ff1584a2eab87500b7164f7fa}

Attributo layer. Si applica al livello corrente o all’immagine composita, se `layer=comp`.

## Predefinito {#section-abba67ed028049048ae43405ea69b164}

`opac=100,100`, per non modificare l’opacità del livello.

## Esempio {#section-9710810e96af40538652e8ae4aadd3be}

… `&layer=1&text=variable%20opacity&opac=90,70&effect=-1&opac=50&`…

L’opacità del testo in questo esempio è 90*70/100=63% e l’opacità del livello dell’effetto è 90*50/100=45%.

## Consultate anche {#section-dbdad35ccd544590b4b11d31a9ab062e}

[color=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md) , [bgColor=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bgcolor.md#reference-441371ba4ef54fe781887c5ae448f6ab)
