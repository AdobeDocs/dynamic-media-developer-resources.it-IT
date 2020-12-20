---
description: Posizione del livello.
seo-description: Posizione del livello.
seo-title: pos
solution: Experience Manager
title: pos
topic: Scene7 Image Serving - Image Rendering API
uuid: e9872ce9-5c47-49c5-9c87-4fa8441c4770
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '160'
ht-degree: 3%

---


# pos{#pos}

Posizione del livello.

pos= *`coord`*

posN= *`coordN`*

<table id="simpletable_754F76EE00BF4129B07502647FF172B7"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> accordo</span> </p> </td> 
  <td class="stentry"> <p>L’offset dei pixel dall’origine di questo livello all’origine del livello 0 (int, int). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> coordN</span> </p></td> 
  <td class="stentry"> <p>Offset normalizzato dall’origine di questo livello all’origine del livello 0 (reale, reale). </p></td> 
 </tr> 
</table>

Nel caso di livelli di immagine, testo e tinta unita, `pos=` specifica la posizione di un ancoraggio di livello rispetto all’ancoraggio di livello 0. `posN=` i valori delle coordinate vengono normalizzati rispetto alle dimensioni effettive del livello 0 rect.

In caso di livelli di effetto, `pos=` sposta il livello di effetto rispetto al livello principale.

I valori positivi spostano il livello verso destra/basso, verso sinistra/in alto. `posN=0.5,0.5` sposta il livello di metà del livello 0 di larghezza e altezza verso il basso e verso destra.

## Proprietà {#section-51a60cdc52d040538fef378ace7c2e7d}

Attributo layer. Ignorato se `layer=0` o `layer=comp`.

## Predefinito {#section-70a6bc71ded5494e843194dfb6bf5a6c}

`posN=0,0`. Questo posiziona l’ancoraggio del livello nella stessa posizione dell’ancoraggio del livello 0, se si tratta di un livello di immagine, testo o tinta unita. Posiziona un livello di effetto direttamente sopra o sotto il livello principale.

## Esempio {#section-a89a02c22f6b4260bfcf7c842cd6069d}

Vedere l&#39;esempio A in [Templates](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e).

## Consultate anche {#section-812d95575ba542808e8387d0a8650606}

[origin=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-origin.md#reference-e11c7ac06e2240cc884c3fec98f05138)
