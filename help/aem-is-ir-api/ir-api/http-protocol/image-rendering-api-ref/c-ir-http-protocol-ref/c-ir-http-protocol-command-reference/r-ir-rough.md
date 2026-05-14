---
title: ruvido
description: Rugosità superficie materiale. Specifica la rugosità relativa della superficie materiale.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 8903b51c-c7d4-460f-8f28-00053eac9d6e
TQID: 'https://experienceleague.adobe.com/FhLagzJwQodPihSxkEyBl8zSnEU0gDq0zevixYMApUY'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 182
ht-degree: 1%

---

# ruvido{#rough}

Rugosità superficie materiale. Specifica la rugosità relativa della superficie materiale.

` rough= *`val`*`

<table id="simpletable_432E33EC87144AC7A2A8D9406F862708"> 
 <tr class="strow"> 
  <td class="stentry"> <p> Valore <span class="varname"> </span> </p> </td> 
  <td class="stentry"> <p>Rugosità superficie (0...100%) o -1 per selezionare la rugosità di default. </p> </td> 
 </tr> 
</table>

Utilizzato per controllare l&#39;effetto di rendering della riflessione 3D. Valori di rugosità inferiori producono in genere effetti di riflessione più uniformi; valori più elevati causano la randomizzazione e la dispersione dell&#39;immagine riflessa.

Ogni tipo di materiale ( `type=`) definisce un effetto di rendering di riflessione minimo e massimo basato sulla rugosità. Per alcuni tipi di materiale (ad esempio, carta da parati), `rough=` ha un impatto minimo sull&#39;aspetto del riflesso, mentre per altri tipi di materiale (ad esempio, pietra o ceramica), l&#39;effetto è notevolmente più pronunciato.

`rough=-1` Imposta la rugosità su un valore predefinito interno al server (40% per i tipi di materiale tipici).

## Proprietà {#section-515375758b254c80af576271bdb61bb8}

Attributo materiale. Ignorato se la vignettatura non dispone di capacità di riflessione 3D, se all&#39;oggetto di destinazione non è associata alcuna geometria 3D o se l&#39;oggetto di destinazione non riflette altri oggetti della scena.

## Predefinito {#section-11861a5e6e8649ee988267d2707fd7cc}

`catalog::Roughness` Se il materiale è basato su una voce di catalogo, altrimenti circa il 40%.

## Consultate anche {#section-d232fff7237443cc95c4bb50cb3d32bb}

[tipo=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-type.md#reference-128c7de89e2d46838019b560f3f84a35) , [gloss=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-gloss.md#reference-325aef2ee51e4e1584a06047427340ca)
