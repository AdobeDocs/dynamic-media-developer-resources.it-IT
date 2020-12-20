---
description: Impostazioni di rendering avanzate. Specifica le impostazioni di rendering avanzate da applicare durante il rendering della selezione corrente.
seo-description: Impostazioni di rendering avanzate. Specifica le impostazioni di rendering avanzate da applicare durante il rendering della selezione corrente.
seo-title: rs
solution: Experience Manager
title: rs
topic: Scene7 Image Serving - Image Rendering API
uuid: 4ff7fcb4-a10a-4e82-80a1-edf79ae1f717
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '132'
ht-degree: 3%

---


# rs{#rs}

Impostazioni di rendering avanzate. Specifica le impostazioni di rendering avanzate da applicare durante il rendering della selezione corrente.

`rs= *`val`*`

<table id="simpletable_4B028996E5824FC18B9749D1A6A3C2E3"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> val</span> </p> </td> 
  <td class="stentry"> <p>Stringa delle impostazioni di rendering. </p></td> 
 </tr> 
</table>

Utilizzato per ottimizzare l’aspetto del rendering. Usate la funzione di rendering dello strumento di authoring delle vignettature (parte del pacchetto Scene7 Image Authoring) per creare le stringhe delle impostazioni di rendering.

## Proprietà {#section-9a2b2228789046658cb80eddf343af75}

Attributo materiale.

## Predefinito {#section-f4751476c3134f16ac6283d6f0c46e47}

`catalog::RenderSettings`.

## Esempio {#section-47e4811882574441a4d517e42a35f352}

Dopo alcuni esperimenti con l’authoring delle immagini, viene determinato che Maschera di contrasto (USM) fornisce la giusta quantità di nitidezza per l’applicazione e il materiale in questione. La stringa delle impostazioni di rendering che configura USM viene copiata nel comando `rs=` da usare con questo materiale:

`…&rs=U2V20W50X2&…`

## Consultate anche {#section-930116e735024a008c994547ba36ee40}

[catalogo::RenderSettings](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-rendersettings-dataref.md#reference-9ce753ae4096455eadcc12ac064de711)
