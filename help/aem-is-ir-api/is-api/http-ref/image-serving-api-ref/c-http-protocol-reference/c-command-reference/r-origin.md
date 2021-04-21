---
description: Origine livello.
solution: Experience Manager
title: origine
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '166'
ht-degree: 3%

---


# origin{#origin}

Origine livello.

`origin= *`corda`*`

`originN= *`coordN`*`

<table id="simpletable_A270FD92B1E841FE81F5AB300351FE01"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> corda</span> </p></td> 
  <td class="stentry"> <p>Offset pixel dall'angolo in alto a sinistra del bordo del livello (int, int). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> coordN</span> </p></td> 
  <td class="stentry"> <p>Offset normalizzato dal centro della direzione dello strato (reale, reale). </p></td> 
 </tr> 
</table>

>[!NOTE]
>
>La correzione del livello include sempre eventuali modifiche di `extend=`.

Definisce il punto di allineamento del rettangolo del livello, utilizzato per posizionare il rettangolo del livello rispetto al livello 0 tramite `pos=`. `originN=0,0` posiziona l’origine del livello al centro del rettangolo del livello. `originN=-0.5,-0.5` ed  `origin=0,0` è l&#39;angolo in alto a sinistra ed  `originN=0.5,0.5` è l&#39;angolo in basso a destra del rettangolo di livello.

## Proprietà {#section-60f639e36ada43d1abc6bfc100afc925}

Attributo livello. Si applica al livello corrente o al livello 0 se `layer=comp`. Non influenzato dalle trasformazioni di livello ( `crop=`, `scale=`, `rotate=`, `flip=`) applicate alla sorgente del livello. Sostituisce `anchor=`. Ignorato dai livelli di effetto.

## Predefinito {#section-b7209e5c2ad6491fb0c2353cc3f1f703}

Se `origin=` non è specificato, l&#39;origine del livello viene determinata applicando le trasformazioni del livello all&#39;ancoraggio dell&#39;immagine. Se l&#39;ancoraggio dell&#39;immagine non è noto, viene utilizzato il centro del rettangolo di livello ( `originN=0,0`).

## Esempio {#section-13e38d6e17be4e6cbc6b27fbde63b291}

Vedi l&#39;esempio A in [Modelli](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e).

## Consultate anche {#section-a9f9c42c86fe45798deb2daaf27ea5b7}

[anchor=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-anchor.md#reference-6661e548ab284b82828d8d94c8ddeb7c) ,  [pos=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-pos.md#reference-65de948f4b404f1182b22119ca332143),  [extension=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-extend.md#reference-7e9156beb285459d830e2d56782a74ac)
