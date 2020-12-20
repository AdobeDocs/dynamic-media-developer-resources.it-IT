---
description: Ancoraggio immagine. Definisce il punto di ancoraggio del rettangolo dell’immagine, del colore in tinta unita o del rettangolo del rettangolo del rettangolo di selezione del testo, prima di applicare le trasformazioni (ritaglio=, scala=, rotate=, flip=). Funge anche da centro di rotazione per rotate=.
seo-description: Ancoraggio immagine. Definisce il punto di ancoraggio del rettangolo dell’immagine, del colore in tinta unita o del rettangolo del rettangolo del rettangolo di selezione del testo, prima di applicare le trasformazioni (ritaglio=, scala=, rotate=, flip=). Funge anche da centro di rotazione per rotate=.
seo-title: ancoraggio
solution: Experience Manager
title: ancoraggio
topic: Scene7 Image Serving - Image Rendering API
uuid: 3b174360-9bb7-4dc8-83be-6b8c4ea88cd4
translation-type: tm+mt
source-git-commit: fe557a2429ceb7b48f22b9cbef5820ad39bad69f
workflow-type: tm+mt
source-wordcount: '239'
ht-degree: 2%

---


# ancoraggio{#anchor}

Ancoraggio immagine. Definisce il punto di ancoraggio del rettangolo dell’immagine, del colore in tinta unita o del rettangolo del rettangolo del rettangolo di selezione del testo, prima di applicare le trasformazioni (ritaglio=, scala=, rotate=, flip=). Funge anche da centro di rotazione per rotate=.

`anchor= *`accordo`*`

`anchorN= *`coordN`*`

<table id="simpletable_3ED1CD0BF473439FA1132FC84B4452A8"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> accordo</span> </span> </p> </td> 
  <td class="stentry"> <p>scostamento pixel dall’angolo superiore sinistro dell’immagine sorgente (int, int) </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> coordN</span> </span> </p> </td> 
  <td class="stentry"> <p>offset normalizzato dal centro dell’immagine sorgente (reale, reale) </p></td> 
 </tr> 
</table>

Il punto di ancoraggio viene trasformato con l&#39;immagine e diventa il punto di origine del livello (a meno che non venga specificato anche `origin=`, nel qual caso `anchor=` viene utilizzato solo come centro di rotazione per `rotate=`).

`anchorN=0,0` posiziona l’ancoraggio immagine al centro dell’immagine sorgente. `anchorN=-0.5,-0.5` oppure  `anchor=0,0` si trova nell’angolo superiore sinistro e  `anchorN=0.5,0.5` nell’angolo inferiore destro dell’immagine sorgente.

## Proprietà {#section-f08942bc6aae46a8b5d341faaff80640}

Attributo immagine di origine. Si applica al livello corrente o al livello 0 se `layer=comp`.

## Predefinito {#section-35d369fab1254f1a9b91684a6e169ad1}

Se `anchor=` non è specificato, viene utilizzato catalog::Anchor. Se `catalog::Anchor` non è definito, viene utilizzato il centro del rettangolo immagine (come se fosse stato specificato `anchorN=0,0`).

I livelli di testo che coinvolgono `textPs=` e che coinvolgono `clipPath=` possono avere ancoraggi predefiniti diversi.

## Esempio {#section-cc127e6b1ea94524900b5c0dd8b4c7ec}

Vedere &quot;Esempio C&quot; in [Templates](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e).

## Consultate anche {#section-9877ea3a0743492aaa4fa1dfc9510b07}

[catalogo::Ancoraggio](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-anchor-cat.md) ,  [origine=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-origin.md#reference-e11c7ac06e2240cc884c3fec98f05138),  [rotate=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-rotate.md#reference-12abb086635546ec9ec2e1a793dc1096),  [clipPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clippath.md#reference-8139b1b52dc54749b51b109521ddf83d), livelli di  [testo](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-text-formatting/r-text-layers.md#reference-47e78cfb18134db5ab09e17af14a6a8f)
