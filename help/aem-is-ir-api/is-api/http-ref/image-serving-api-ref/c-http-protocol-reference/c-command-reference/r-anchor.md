---
title: ancoraggio
description: Ancoraggio immagine. Definisce il punto di ancoraggio dell'immagine, del colore a tinta unita o del rettangolo del riquadro del testo prima di applicare le trasformazioni (crop=, scale=, rotate=, flip=). Funge anche da centro di rotazione per rotate=.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: f62ae048-0dcc-4e93-a9f1-2e4db6bef51f
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '208'
ht-degree: 1%

---

# ancoraggio{#anchor}

Ancoraggio immagine. Definisce il punto di ancoraggio dell&#39;immagine, del colore a tinta unita o del rettangolo del riquadro del testo prima di applicare le trasformazioni (crop=, scale=, rotate=, flip=). Funge anche da centro di rotazione per rotate=.

`anchor= *`corda`*`

`anchorN= *`coordN`*`

<table id="simpletable_3ED1CD0BF473439FA1132FC84B4452A8"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> corda</span> </span> </p> </td> 
  <td class="stentry"> <p>offset pixel dall'angolo superiore sinistro dell'immagine sorgente (int, int) </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> coordN</span> </span> </p> </td> 
  <td class="stentry"> <p>offset normalizzato dal centro dell'immagine sorgente (reale, reale) </p></td> 
 </tr> 
</table>

Il punto di ancoraggio viene trasformato con l&#39;immagine e diventa il punto di origine del livello (a meno che `origin=` viene specificato anche, nel qual caso `anchor=` viene utilizzato solo come centro di rotazione per `rotate=`).

`anchorN=0,0` posiziona l&#39;ancoraggio dell&#39;immagine al centro dell&#39;immagine sorgente. `anchorN=-0.5,-0.5` o `anchor=0,0` si trova nell’angolo in alto a sinistra, e `anchorN=0.5,0.5` si trova nell’angolo inferiore destro dell’immagine sorgente.

## Proprietà {#section-f08942bc6aae46a8b5d341faaff80640}

Attributo immagine sorgente. Si applica al livello corrente o al livello 0 se `layer=comp`.

## Predefinito {#section-35d369fab1254f1a9b91684a6e169ad1}

Se `anchor=` non è specificato, viene utilizzato catalog::Anchor. Se `catalog::Anchor` non è definito, viene utilizzato il centro del rettangolo dell&#39;immagine (come specificando `anchorN=0,0`).

Livelli di testo con `textPs=` e strati che coinvolgono `clipPath=` possono avere ancoraggi predefiniti diversi.

## Esempio {#section-cc127e6b1ea94524900b5c0dd8b4c7ec}

Vedi &quot;Esempio C&quot; in [Modelli](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e).

## Consultate anche {#section-9877ea3a0743492aaa4fa1dfc9510b07}

[catalogo::ancoraggio](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-anchor-cat.md) , [origin= origine](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-origin.md#reference-e11c7ac06e2240cc884c3fec98f05138), [rotate= ruota](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-rotate.md#reference-12abb086635546ec9ec2e1a793dc1096), [clipPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clippath.md#reference-8139b1b52dc54749b51b109521ddf83d), [Livelli di testo](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-text-formatting/r-text-layers.md#reference-47e78cfb18134db5ab09e17af14a6a8f)
