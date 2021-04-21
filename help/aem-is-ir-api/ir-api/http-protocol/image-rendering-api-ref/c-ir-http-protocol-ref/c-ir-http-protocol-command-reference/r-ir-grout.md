---
description: Colore e spessore della scanalatura del riquadro. Simula scanalatura per piastrelle di pietra ceramica e naturale.
solution: Experience Manager
title: becco
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '173'
ht-degree: 2%

---


# grotta{#grout}

Colore e spessore della scanalatura del riquadro. Simula scanalatura per piastrelle di pietra ceramica e naturale.

grout= *`color`*[,*`width`*]

<table id="simpletable_302B78CFC8F14E0F962D1D2064AD1371"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> color  </span> </span> </p> </td> 
  <td class="stentry"> <p>Colore di Grout (grigio o RGB). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> width </span> </span> </p> </td> 
  <td class="stentry"> <p>Spessore della scanalatura; unità di coordinate della scena (tipicamente pollici) (reali). </p> </td> 
 </tr> 
</table>

Per il controllo massimo dell&#39;aspetto della grout si applicano i seguenti requisiti:

* La piastrella deve essere quadrata o rettangolare; al momento non sono supportate altre forme.
* L’immagine deve contenere un solo riquadro.
* L&#39;eventuale grout predefinito dell&#39;immagine deve avere esattamente lo stesso spessore su tutti e quattro i bordi.
* Lo spessore della grotta predefinita deve essere specificato nel catalogo dei materiali ( `catalog::GroutWidth`).

## Proprietà {#section-de78b678245b4ffda48097c345949e77}

Attributo materiale. `*``*` il colore deve essere un valore di colore RGB. `*`La larghezza di `*`  deve essere un valore reale pari a 0 o superiore.

Ignorato se repeat = 4, 5, 7, 8, 9, 14 o superiore o se specificato per materiali diversi dalle texture ripetibili.

## Predefinito {#section-bfab3621f70b4489a21994ab11b20cc6}

Se `grout=` non è specificato, la grout nell&#39;immagine non viene modificata. Se è specificato ` grout= *`color`*`, `*`width`*` viene impostato automaticamente su `catalog::GroutWidth`.

## Consultate anche {#section-8d472906a44943f5a8557e98f2fbc71f}

[Valori colore](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/r-ir-color-values.md#reference-657f95c0841742d2a55a48bc938303f6)
