---
title: beccaccia
description: Colore e spessore della malta delle sezioni. Simula la malta per piastrelle in ceramica e pietra naturale.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 6647b459-11d2-47e4-9033-3a740f01a623
TQID: 'https://experienceleague.adobe.com/FrYxcizVu3nXej1tt4QpX0AsLEylXTfwYRaSQP43HNI'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 169
ht-degree: 1%

---

# beccaccia {#grout}

Colore e spessore della malta delle sezioni. Simula la malta per piastrelle in ceramica e pietra naturale.

Grout= *`color`*[,*`width`*]

<table id="simpletable_302B78CFC8F14E0F962D1D2064AD1371"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> colore </span> </span> </p> </td>
  <td class="stentry"> <p>Colore di Grout (grigio o RGB). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> larghezza </span> </span> </p> </td>
  <td class="stentry"> <p>Spessore di scanalatura; unità di coordinate della scena (tipicamente pollici) (reale). </p> </td>
 </tr> 
</table>

Per il massimo controllo dell&#39;aspetto della malta, si applicano i seguenti requisiti:

* La tessera deve essere quadrata o rettangolare; attualmente non sono supportate altre forme.
* L’immagine deve contenere solo una sezione singola.
* L&#39;eventuale solidificazione di default nell&#39;immagine deve avere lo stesso spessore su tutti e quattro i bordi.
* È necessario specificare lo spessore della massa predefinita nel catalogo dei materiali ( `catalog::GroutWidth`).

## Proprietà {#section-de78b678245b4ffda48097c345949e77}

Attributo materiale. `*`color`*` deve essere un valore di colore RGB. `*`width`*` deve essere un valore reale pari o superiore a 0.

Ignorato se repeat = 4, 5, 7, 8, 9, 14 o superiore oppure se specificato per materiali diversi dalle texture ripetibili.

## Predefinito {#section-bfab3621f70b4489a21994ab11b20cc6}

Se `grout=` non è specificato, il grout nell&#39;immagine non viene modificato. Se si specifica `grout= *`color`*`, `*`width`*` viene impostato automaticamente su `catalog::GroutWidth`.

## Consultate anche {#section-8d472906a44943f5a8557e98f2fbc71f}

[Valori colore](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/r-ir-color-values.md#reference-657f95c0841742d2a55a48bc938303f6)
