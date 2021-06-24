---
description: Ritaglia immagine Specifica un'area di ritaglio rettangolare, espressa in pixel o normalizzata rispetto all'immagine sorgente a risoluzione piena o all'immagine maschera.
solution: Experience Manager
title: Ritaglia
feature: Dynamic Media Classic, SDK/API
role: Developer,Business Practitioner
exl-id: d1ea63c1-95f0-4a4e-b65d-eb535eef0205
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '212'
ht-degree: 2%

---

# Ritaglia{#crop}

Ritaglia immagine Specifica un&#39;area di ritaglio rettangolare, espressa in pixel o normalizzata rispetto all&#39;immagine sorgente a risoluzione piena o all&#39;immagine maschera.

`crop= *``*, *`coordsize`*`

`cropN= *``*, *`coordNsizeN`*`

<table id="simpletable_472A9AD67AA64419B0877B0535F8B14A"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> corda</span></span> </p> </td> 
  <td class="stentry"> <p>Offset pixel dall’angolo in alto a sinistra dell’immagine sorgente all’angolo in alto a sinistra del rettangolo di ritaglio (int, int). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> coordN</span></span> </p> </td> 
  <td class="stentry"> <p>Offset normalizzato dall'alto a sinistra dell'immagine sorgente all'alto a sinistra del rettangolo di ritaglio (reale, reale). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> size</span></span> </p></td> 
  <td class="stentry"> <p>Dimensioni del rettangolo di ritaglio in pixel (int, int). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> sizeN</span></span> </p></td> 
  <td class="stentry"> <p>Dimensione normalizzata del rettangolo di ritaglio rispetto alle dimensioni dell'immagine sorgente (reale, reale). </p></td> 
 </tr> 
</table>

Può essere utilizzato anche per estendere l&#39;immagine oltre i suoi limiti specificando valori negativi x, y e/o larghezza, altezza maggiori della larghezza e dell&#39;altezza dell&#39;immagine. In questo caso, l’area estesa è completamente trasparente (a meno che non sia specificato `bgColor=`).

## Proprietà {#section-632e0405bb9940679b5f8b1c10e0902e}

Attributo immagine/maschera di origine. Si applica all&#39;immagine sorgente del livello 0 se `layer=comp`. Ignorato dai livelli che non sono associati a un&#39;immagine sorgente o a una maschera.

## Predefinito {#section-41f62d386c664f77952bc22e7286bb88}

Immagine intera ( `cropN=0,0,1,1`).

## Esempi {#section-2c99b481c0a04321979a3b522aa295d1}

**Ritaglio 10% a sinistra e 10% a destra:**

`…&cropN=0.1,0,0.8,1&…`

**Ritaglia il 20% rispetto al bordo inferiore di un&#39;immagine:**

`…&cropN=0,0,1,0.8&…`

## Consultate anche {#section-d5616c7aa0ce4faa88f51dd5662e5daf}

[](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-croppath.md) [cropPathbgColor=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bgcolor.md#reference-441371ba4ef54fe781887c5ae448f6ab) ,  [anchor=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-anchor.md#reference-6661e548ab284b82828d8d94c8ddeb7c),  [extension=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-extend.md#reference-7e9156beb285459d830e2d56782a74ac)
