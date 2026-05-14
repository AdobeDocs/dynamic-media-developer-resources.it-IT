---
title: flag
description: Applicare i flag. Specifica opzioni di rendering aggiuntive.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: d0c3f65e-2dec-4c35-8df4-8d111e81f3f0
TQID: 'https://experienceleague.adobe.com/tdbtQIxutlPSPRm4vGWCQLM8veyivWfabKos9YbvfYg'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 70
ht-degree: 1%

---

# flag {#flags}

Applicare i flag. Specifica opzioni di rendering aggiuntive.

`flags= *`val`*`

<table id="simpletable_00B21BD9E47E4D2FB0042CB507431916"> 
 <tr class="strow"> 
  <td class="stentry"> <p>Valore <span class="varname"></span> </p> </td> 
  <td class="stentry"> <p>Valore del contrassegno. </p></td> 
 </tr> 
</table>

Attualmente utilizzato solo per i materiali del cabinet.

`flags=0` (impostazione predefinita) Esegue il rendering degli archivi superiori con porte piene.

`flags=1` Esegue il rendering dei cabinet superiori con porte di vetro (se la vignettatura è stata creata con porte di vetro).

## Proprietà {#section-a2b00d7bb15e449ea85178acb92d8285}

Attributo materiale. Ignorato se non è un materiale del cabinet o se l&#39;oggetto del cabinet di destinazione non consente porte in vetro.

## Predefinito {#section-4c134b02a1da4ffb9841233f98f6e97c}

`flags=0` Se non si dispone di porte di vetro.
