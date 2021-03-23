---
description: Posizione del livello.
seo-description: Posizione del livello.
seo-title: pos
solution: Experience Manager
title: pos
uuid: e9872ce9-5c47-49c5-9c87-4fa8441c4770
feature: Dynamic Media Classic, SDK/API
role: Sviluppatore, Business Practices
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '168'
ht-degree: 2%

---


# pos{#pos}

Posizione del livello.

pos= *`coord`*

posN= *`coordN`*

<table id="simpletable_754F76EE00BF4129B07502647FF172B7"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> corda</span> </p> </td> 
  <td class="stentry"> <p>Offset pixel dall'origine di questo livello all'origine del livello 0 (int, int). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> coordN</span> </p></td> 
  <td class="stentry"> <p>Offset normalizzato dall'origine di questo livello all'origine del livello 0 (reale, reale). </p></td> 
 </tr> 
</table>

Nel caso di livelli di immagine, testo e colore solido, `pos=` specifica la posizione di un ancoraggio di livello rispetto all’ancoraggio di livello 0. `posN=` i valori delle coordinate vengono normalizzati rispetto alle dimensioni effettive del livello 0.

In caso di livelli di effetto, `pos=` sposta il livello di effetto rispetto al livello padre.

I valori positivi spostano il livello verso destra/basso, negativo verso sinistra/superiore. `posN=0.5,0.5` sposta il livello di metà del livello 0 di larghezza e altezza in basso e a destra.

## Proprietà {#section-51a60cdc52d040538fef378ace7c2e7d}

Attributo livello. Ignorato se `layer=0` o `layer=comp`.

## Predefinito {#section-70a6bc71ded5494e843194dfb6bf5a6c}

`posN=0,0`. Posiziona l’ancoraggio del livello nella stessa posizione dell’ancoraggio del livello 0, se si tratta di un livello di immagine, testo o colore solido. Posiziona un livello di effetto direttamente sopra o sotto il livello padre.

## Esempio {#section-a89a02c22f6b4260bfcf7c842cd6069d}

Vedi l&#39;esempio A in [Modelli](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e).

## Consultate anche {#section-812d95575ba542808e8387d0a8650606}

[origin=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-origin.md#reference-e11c7ac06e2240cc884c3fec98f05138)
