---
description: Origine del livello.
seo-description: Origine del livello.
seo-title: origine
solution: Experience Manager
title: origine
topic: Scene7 Image Serving - Image Rendering API
uuid: a36fc0b6-7744-4c1c-b9f8-4aa31a886bff
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '161'
ht-degree: 3%

---


# origin{#origin}

Origine del livello.

`origin= *`accordo`*`

`originN= *`coordN`*`

<table id="simpletable_A270FD92B1E841FE81F5AB300351FE01"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> accordo</span> </p></td> 
  <td class="stentry"> <p>Offset dei pixel dall’angolo superiore sinistro del rettangolo del livello (int, int). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> coordN</span> </p></td> 
  <td class="stentry"> <p>Offset normalizzato dal centro del rettangolo del livello (reale, reale). </p></td> 
 </tr> 
</table>

>[!NOTE]
>
>La funzione rect del livello include sempre qualsiasi modifica di `extend=`.

Definisce il punto di allineamento del rettangolo del livello, utilizzato per posizionare il rettangolo del livello relativo al livello 0 tramite `pos=`. `originN=0,0` posiziona l’origine del livello al centro del rettangolo del livello. `originN=-0.5,-0.5` ed  `origin=0,0` è l’angolo superiore sinistro ed  `originN=0.5,0.5` è l’angolo inferiore destro del rettangolo del livello.

## Proprietà {#section-60f639e36ada43d1abc6bfc100afc925}

Attributo layer. Si applica al livello corrente o al livello 0 se `layer=comp`. Trasformazioni di livello non interessate da tali trasformazioni ( `crop=`, `scale=`, `rotate=`, `flip=`) applicate alla sorgente del livello. Ignora `anchor=`. Ignorato dai livelli degli effetti.

## Predefinito {#section-b7209e5c2ad6491fb0c2353cc3f1f703}

Se `origin=` non è specificato, l’origine del livello viene determinata applicando le trasformazioni del livello all’ancoraggio dell’immagine. Se l’ancoraggio immagine non è noto, viene utilizzato il centro del rettangolo di livello ( `originN=0,0`).

## Esempio {#section-13e38d6e17be4e6cbc6b27fbde63b291}

Vedere l&#39;esempio A in [Templates](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e).

## Consultate anche {#section-a9f9c42c86fe45798deb2daaf27ea5b7}

[anchor=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-anchor.md#reference-6661e548ab284b82828d8d94c8ddeb7c) ,  [pos=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-pos.md#reference-65de948f4b404f1182b22119ca332143),  [extension=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-extend.md#reference-7e9156beb285459d830e2d56782a74ac)
