---
description: Colore e spessore della tegola. Simula l'arachide per piastrelle di pietra in ceramica e naturale.
seo-description: Colore e spessore della tegola. Simula l'arachide per piastrelle di pietra in ceramica e naturale.
seo-title: malva
solution: Experience Manager
title: malva
topic: Scene7 Image Serving - Image Rendering API
uuid: 00069004-40f2-4ab6-85d8-ca197b7bef69
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# malva{#grout}

Colore e spessore della tegola. Simula l&#39;arachide per piastrelle di pietra in ceramica e naturale.

grout= *`color`*[,*`width`*]

<table id="simpletable_302B78CFC8F14E0F962D1D2064AD1371"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> colore </span></span> </p> </td> 
  <td class="stentry"> <p>Colore di scanalatura (grigio o RGB). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> width </span> </span> </p> </td> 
  <td class="stentry"> <p>Spessore della Grotta; unità di coordinate della scena (in genere pollici) (reali). </p> </td> 
 </tr> 
</table>

Per il controllo massimo dell&#39;aspetto dell&#39;arachide si applicano i seguenti requisiti:

* La piastrella deve essere quadrata o rettangolare; al momento non sono supportate altre forme.
* L’immagine deve contenere un solo riquadro.
* L’eventuale grout predefinito nell’immagine deve avere esattamente lo stesso spessore su tutti e quattro i bordi.
* Lo spessore dell&#39;insieme predefinito deve essere specificato nel catalogo dei materiali ( `catalog::GroutWidth`).

## Proprietà {#section-de78b678245b4ffda48097c345949e77}

Attributo materiale. ` *`il colore`*` deve essere un valore di colore RGB. ` *`width`*` deve essere un valore reale pari a 0 o superiore.

Ignorato se ripeti = 4, 5, 7, 8, 9, 14 o superiore o se specificato per materiali diversi da texture ripetibili.

## Predefinito {#section-bfab3621f70b4489a21994ab11b20cc6}

Se non `grout=` viene specificato, l’intervallo nell’immagine non viene modificato. Se ` grout= *`viene specificato il colore`*` , per impostazione predefinita la ` *`larghezza`*` è `catalog::GroutWidth`.

## Consultate anche {#section-8d472906a44943f5a8557e98f2fbc71f}

[Valori colore](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/r-ir-color-values.md#reference-657f95c0841742d2a55a48bc938303f6)
