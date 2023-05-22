---
description: Ritaglia immagine. Specifica un'area di ritaglio rettangolare, espressa in pixel o normalizzata rispetto all'immagine sorgente o all'immagine maschera a risoluzione completa.
solution: Experience Manager
title: ritagliare
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: d1ea63c1-95f0-4a4e-b65d-eb535eef0205
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '207'
ht-degree: 1%

---

# ritagliare{#crop}

Ritaglia immagine. Specifica un&#39;area di ritaglio rettangolare, espressa in pixel o normalizzata rispetto all&#39;immagine sorgente o all&#39;immagine maschera a risoluzione completa.

`crop= *`corda`*, *`dimensione`*`

`cropN= *`coordN`*, *`sizeN`*`

<table id="simpletable_472A9AD67AA64419B0877B0535F8B14A"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> corda</span></span> </p> </td> 
  <td class="stentry"> <p>Offset pixel dall'angolo superiore sinistro dell'immagine sorgente all'angolo superiore sinistro del rettangolo di ritaglio (int, int). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> coordN</span></span> </p> </td> 
  <td class="stentry"> <p>Offset normalizzato dall'alto a sinistra dell'immagine sorgente all'alto a sinistra del rettangolo di ritaglio (reale, reale). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> dimensione</span></span> </p></td> 
  <td class="stentry"> <p>Dimensione del ritaglio in pixel (int, int). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> sizeN</span></span> </p></td> 
  <td class="stentry"> <p>Dimensione normalizzata del rettangolo di ritaglio relativa alle dimensioni dell’immagine sorgente (reale, reale). </p></td> 
 </tr> 
</table>

Può essere utilizzato anche per estendere l&#39;immagine oltre i suoi limiti specificando valori negativi di x, y e/o larghezza, valori di altezza maggiori della larghezza e dell&#39;altezza dell&#39;immagine. In questo caso, l&#39;area estesa è completamente trasparente (a meno che `bgColor=` è specificato).

## Proprietà {#section-632e0405bb9940679b5f8b1c10e0902e}

Attributo immagine/maschera di origine. Si applica all&#39;immagine sorgente di livello 0 se `layer=comp`. Ignorato dai livelli non associati a un&#39;immagine o a una maschera di origine.

## Predefinito {#section-41f62d386c664f77952bc22e7286bb88}

Immagine intera ( `cropN=0,0,1,1`).

## Esempi {#section-2c99b481c0a04321979a3b522aa295d1}

**Ritaglia il 10% a sinistra e il 10% a destra:**

`…&cropN=0.1,0,0.8,1&…`

**Ritaglia il 20% dal bordo inferiore di un&#39;immagine:**

`…&cropN=0,0,1,0.8&…`

## Consultate anche {#section-d5616c7aa0ce4faa88f51dd5662e5daf}

[cropPath](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-croppath.md) [bgColor=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bgcolor.md#reference-441371ba4ef54fe781887c5ae448f6ab) , [ancoraggio=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-anchor.md#reference-6661e548ab284b82828d8d94c8ddeb7c), [extend= estensione](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-extend.md#reference-7e9156beb285459d830e2d56782a74ac)
