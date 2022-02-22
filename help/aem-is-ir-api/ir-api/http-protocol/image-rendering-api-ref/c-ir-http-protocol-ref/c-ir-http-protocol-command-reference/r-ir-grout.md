---
title: becco
description: Colore e spessore della scanalatura del riquadro. Simula scanalatura per piastrelle di pietra ceramica e naturale.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 6647b459-11d2-47e4-9033-3a740f01a623
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '162'
ht-degree: 3%

---

# becco {#grout}

Colore e spessore della scanalatura del riquadro. Simula scanalatura per piastrelle di pietra ceramica e naturale.

grout= *`color`*[,*`width`*]

<table id="simpletable_302B78CFC8F14E0F962D1D2064AD1371"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> color </span> </span> </p> </td>
  <td class="stentry"> <p>Colore di scolo (grigio o RGB). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> width </span> </span> </p> </td>
  <td class="stentry"> <p>Spessore della scanalatura; unità di coordinate della scena (tipicamente pollici) (reali). </p> </td>
 </tr> 
</table>

Per il controllo massimo dell&#39;aspetto della grout, si applicano le seguenti prescrizioni:

* La piastrella deve essere quadrata o rettangolare; al momento non sono supportate altre forme.
* L’immagine deve contenere un solo riquadro.
* L&#39;eventuale grout predefinito dell&#39;immagine deve avere lo stesso spessore su tutti e quattro i bordi.
* Lo spessore della grotta predefinita deve essere specificato nel catalogo dei materiali ( `catalog::GroutWidth`).

## Proprietà {#section-de78b678245b4ffda48097c345949e77}

Attributo materiale. `*`color`*` Deve essere un valore di colore RGB. `*`larghezza`*` deve essere un valore reale pari a 0 o superiore.

Ignorato se repeat = 4, 5, 7, 8, 9, 14 o superiore o se specificato per materiali diversi dalle texture ripetibili.

## Predefinito {#section-bfab3621f70b4489a21994ab11b20cc6}

Se `grout=` non viene specificato, la grout nell&#39;immagine non viene modificata. Se `grout= *`color`*` è specificato, `*`larghezza`*` impostazioni predefinite `catalog::GroutWidth`.

## Consultate anche {#section-8d472906a44943f5a8557e98f2fbc71f}

[Valori colore](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/r-ir-color-values.md#reference-657f95c0841742d2a55a48bc938303f6)
