---
description: Ritaglia immagine. Specifica un'area di ritaglio rettangolare, espressa in pixel o normalizzata rispetto all'immagine sorgente o all'immagine maschera a risoluzione piena.
seo-description: Ritaglia immagine. Specifica un'area di ritaglio rettangolare, espressa in pixel o normalizzata rispetto all'immagine sorgente o all'immagine maschera a risoluzione piena.
seo-title: Ritaglia
solution: Experience Manager
title: Ritaglia
topic: Scene7 Image Serving - Image Rendering API
uuid: c8eca467-7564-48a6-82d7-17f68a1399e1
translation-type: tm+mt
source-git-commit: fe557a2429ceb7b48f22b9cbef5820ad39bad69f
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---


# Ritaglia{#crop}

Ritaglia immagine. Specifica un&#39;area di ritaglio rettangolare, espressa in pixel o normalizzata rispetto all&#39;immagine sorgente o all&#39;immagine maschera a risoluzione piena.

`crop= *``*, *`coordsize`*`

`cropN= *``*, *`coordNsizeN`*`

<table id="simpletable_472A9AD67AA64419B0877B0535F8B14A"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> accordo</span></span> </p> </td> 
  <td class="stentry"> <p>Offset dei pixel dall’angolo in alto a sinistra dell’immagine sorgente verso l’angolo in alto a sinistra del rettangolo di ritaglio (int, int). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> coordN</span></span> </p> </td> 
  <td class="stentry"> <p>Offset normalizzato dall’angolo superiore sinistro dell’immagine sorgente all’angolo superiore sinistro del rettangolo di ritaglio (reale, reale). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> size</span></span> </p></td> 
  <td class="stentry"> <p>Dimensione del rettangolo di ritaglio in pixel (int, int). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> sizeN</span></span> </p></td> 
  <td class="stentry"> <p>Dimensione normalizzata del rettangolo di ritaglio rispetto alle dimensioni dell’immagine sorgente (reale, reale). </p></td> 
 </tr> 
</table>

Può essere utilizzata anche per estendere l’immagine oltre i suoi bordi specificando valori x, y e/o larghezza, altezza negativi maggiori di larghezza e altezza dell’immagine. In questo caso, l&#39;area estesa è completamente trasparente (a meno che non sia specificato `bgColor=`).

## Proprietà {#section-632e0405bb9940679b5f8b1c10e0902e}

Attributo immagine/maschera di origine. Si applica all&#39;immagine sorgente del livello 0 se `layer=comp`. Ignorato dai livelli che non sono associati a un’immagine o maschera sorgente.

## Predefinito {#section-41f62d386c664f77952bc22e7286bb88}

Immagine intera ( `cropN=0,0,1,1`).

## Esempi {#section-2c99b481c0a04321979a3b522aa295d1}

**Ritagliare il 10% da sinistra e il 10% da destra:**

`…&cropN=0.1,0,0.8,1&…`

**Ritagliare del 20% il bordo inferiore di un’immagine:**

`…&cropN=0,0,1,0.8&…`

## Consultate anche {#section-d5616c7aa0ce4faa88f51dd5662e5daf}

[](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-croppath.md) [CropPathbgColor=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bgcolor.md#reference-441371ba4ef54fe781887c5ae448f6ab) ,  [anchor=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-anchor.md#reference-6661e548ab284b82828d8d94c8ddeb7c),  [extension=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-extend.md#reference-7e9156beb285459d830e2d56782a74ac)
