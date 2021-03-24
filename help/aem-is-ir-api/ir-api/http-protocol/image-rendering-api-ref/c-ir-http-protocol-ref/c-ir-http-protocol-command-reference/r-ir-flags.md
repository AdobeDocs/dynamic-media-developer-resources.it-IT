---
description: Applica dei flag. Specifica opzioni di rendering aggiuntive.
solution: Experience Manager
title: flag
feature: Dynamic Media Classic, SDK/API
role: Sviluppatore, Business Practices
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '78'
ht-degree: 2%

---


# flag{#flags}

Applica dei flag. Specifica opzioni di rendering aggiuntive.

`flags= *`val`*`

<table id="simpletable_00B21BD9E47E4D2FB0042CB507431916"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> val</span> </p> </td> 
  <td class="stentry"> <p>Valore contrassegno. </p></td> 
 </tr> 
</table>

Attualmente utilizzato solo per i materiali dei cabinet.

`flags=0` (impostazione predefinita) esegue il rendering degli armadi superiori con porte solide.

`flags=1` rende gli armadi superiori con porte in vetro (se la vignetta è stata creata con porte in vetro).

## Proprietà {#section-a2b00d7bb15e449ea85178acb92d8285}

Attributo materiale. Ignorato se non è un materiale mobile o se l&#39;oggetto mobile di destinazione non consente porte in vetro.

## Predefinito {#section-4c134b02a1da4ffb9841233f98f6e97c}

`flags=0` senza porte in vetro.
