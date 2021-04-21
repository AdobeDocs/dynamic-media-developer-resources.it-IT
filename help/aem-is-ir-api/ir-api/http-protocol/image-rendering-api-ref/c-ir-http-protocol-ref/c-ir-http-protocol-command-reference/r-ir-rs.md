---
description: Impostazioni avanzate di rendering. Specifica le impostazioni di rendering avanzate da applicare durante il rendering della selezione corrente.
solution: Experience Manager
title: rs
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '124'
ht-degree: 4%

---


# rs{#rs}

Impostazioni avanzate di rendering. Specifica le impostazioni di rendering avanzate da applicare durante il rendering della selezione corrente.

`rs= *`val`*`

<table id="simpletable_4B028996E5824FC18B9749D1A6A3C2E3"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> val</span> </p> </td> 
  <td class="stentry"> <p>Stringa delle impostazioni di rendering. </p></td> 
 </tr> 
</table>

Utilizzato per ottimizzare l&#39;aspetto del rendering. Utilizza la funzione di rendering dello strumento di authoring delle vignette (parte del pacchetto Dynamic Media Image Authoring) per creare stringhe di impostazioni di rendering.

## Proprietà {#section-9a2b2228789046658cb80eddf343af75}

Attributo materiale.

## Predefinito {#section-f4751476c3134f16ac6283d6f0c46e47}

`catalog::RenderSettings`.

## Esempio {#section-47e4811882574441a4d517e42a35f352}

Dopo una certa sperimentazione nell&#39;authoring delle immagini, viene determinato che l&#39;applicazione di Mascheramento intelligente (USM) fornisce la giusta quantità di nitidezza per l&#39;applicazione e il materiale specificati. La stringa delle impostazioni di rendering che configura USM viene copiata nel comando `rs=` da utilizzare con questo materiale:

`…&rs=U2V20W50X2&…`

## Consultate anche {#section-930116e735024a008c994547ba36ee40}

[catalogo::RenderSettings](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-rendersettings-dataref.md#reference-9ce753ae4096455eadcc12ac064de711)
