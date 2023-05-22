---
title: flag
description: Applicare i flag. Specifica opzioni di rendering aggiuntive.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: d0c3f65e-2dec-4c35-8df4-8d111e81f3f0
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '70'
ht-degree: 1%

---

# flag {#flags}

Applicare i flag. Specifica opzioni di rendering aggiuntive.

`flags= *`val`*`

<table id="simpletable_00B21BD9E47E4D2FB0042CB507431916"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> val</span> </p> </td> 
  <td class="stentry"> <p>Valore del contrassegno. </p></td> 
 </tr> 
</table>

Attualmente utilizzato solo per i materiali del cabinet.

`flags=0` (impostazione predefinita) Esegue il rendering dei cabinet superiori con porte solide.

`flags=1` Esegue il rendering degli armadi superiori con porte in vetro (se la vignettatura è stata creata con porte in vetro).

## Proprietà {#section-a2b00d7bb15e449ea85178acb92d8285}

Attributo materiale. Ignorato se non è un materiale del cabinet o se l&#39;oggetto del cabinet di destinazione non consente porte in vetro.

## Predefinito {#section-4c134b02a1da4ffb9841233f98f6e97c}

`flags=0` Senza porte di vetro.
