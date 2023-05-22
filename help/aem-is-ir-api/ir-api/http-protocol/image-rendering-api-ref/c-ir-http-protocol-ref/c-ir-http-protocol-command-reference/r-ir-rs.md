---
title: rs
description: Impostazioni di rendering avanzate. Specifica le impostazioni di rendering avanzate da applicare durante il rendering della selezione corrente.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 419baeb7-e06e-4753-a487-a1f407845f6d
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '114'
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

Utilizzato per ottimizzare l&#39;aspetto del rendering. Per creare stringhe di impostazioni di rendering, utilizzate la funzione di rendering dello strumento di authoring vignettatura (parte del pacchetto di authoring di immagini Dynamic Media).

## Proprietà {#section-9a2b2228789046658cb80eddf343af75}

Attributo materiale.

## Predefinito {#section-f4751476c3134f16ac6283d6f0c46e47}

`catalog::RenderSettings`.

## Esempio {#section-47e4811882574441a4d517e42a35f352}

Dopo alcune sperimentazioni nell&#39;Image Authoring, si è stabilito che la maschera di contrasto (USM) fornisce la giusta quantità di nitidezza per l&#39;applicazione e il materiale in questione. La stringa delle impostazioni di rendering che configura USM viene copiata nel `rs=` comando da utilizzare con questo materiale:

`…&rs=U2V20W50X2&…`

## Consultate anche {#section-930116e735024a008c994547ba36ee40}

[catalog::RenderSettings](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-rendersettings-dataref.md#reference-9ce753ae4096455eadcc12ac064de711)
