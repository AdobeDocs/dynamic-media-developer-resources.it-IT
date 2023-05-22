---
description: Origine livello.
solution: Experience Manager
title: origine
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 5ea8eb18-d169-4255-b4b1-dda849246485
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '158'
ht-degree: 2%

---

# origine{#origin}

Origine livello.

`origin= *`corda`*`

`originN= *`coordN`*`

<table id="simpletable_A270FD92B1E841FE81F5AB300351FE01"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> corda</span> </p></td> 
  <td class="stentry"> <p>Offset pixel dall'angolo superiore sinistro del rettangolo del livello (int, int). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> coordN</span> </p></td> 
  <td class="stentry"> <p>Scostamento normalizzato dal centro del retto di livello (reale, reale). </p></td> 
 </tr> 
</table>

>[!NOTE]
>
>Il rettangolo di livello include sempre qualsiasi modifica eseguita da `extend=`.

Definisce il punto di allineamento del rettangolo di livello, utilizzato per posizionare il rettangolo di livello rispetto al livello 0 tramite `pos=`. `originN=0,0` posiziona l&#39;origine del livello al centro del rettangolo del livello. `originN=-0.5,-0.5` e `origin=0,0` è l’angolo in alto a sinistra, e `originN=0.5,0.5` è l&#39;angolo inferiore destro del rettangolo del livello.

## Proprietà {#section-60f639e36ada43d1abc6bfc100afc925}

Attributo livello. Si applica al livello corrente o al livello 0 se `layer=comp`. Non influenzato dalle trasformazioni dei livelli ( `crop=`, `scale=`, `rotate=`, `flip=`) applicato alla sorgente del livello. Sostituzioni `anchor=`. Ignorato dai livelli degli effetti.

## Predefinito {#section-b7209e5c2ad6491fb0c2353cc3f1f703}

Se `origin=` non è specificato, l&#39;origine del livello viene determinata applicando le trasformazioni di livello all&#39;ancoraggio immagine. Se l&#39;ancoraggio dell&#39;immagine non è noto, il centro del rettangolo del livello ( `originN=0,0`).

## Esempio {#section-13e38d6e17be4e6cbc6b27fbde63b291}

Vedi l’esempio A in [Modelli](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e).

## Consultate anche {#section-a9f9c42c86fe45798deb2daaf27ea5b7}

[ancoraggio=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-anchor.md#reference-6661e548ab284b82828d8d94c8ddeb7c) , [pos=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-pos.md#reference-65de948f4b404f1182b22119ca332143), [extend= estensione](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-extend.md#reference-7e9156beb285459d830e2d56782a74ac)
