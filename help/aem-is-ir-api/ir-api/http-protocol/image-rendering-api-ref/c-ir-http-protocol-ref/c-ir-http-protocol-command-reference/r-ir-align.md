---
title: allinea
description: Allineamento rendering texture. Specifica quale dei punti di origine definiti dall'oggetto vignettatura selezionato deve essere utilizzato.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 0b76f173-809b-4b41-bf39-6b85f77ab2db
TQID: 'https://experienceleague.adobe.com/U6V-e23e9ILdnQfTpJzGPzbCTZEICccSpcMebA-NRjA'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 190
ht-degree: 4%

---

# allinea {#align}

Allineamento rendering texture. Specifica quale dei punti di origine definiti dall&#39;oggetto vignettatura selezionato deve essere utilizzato.

`align=0|1|2|3|4|5|6`

<table id="simpletable_D15233999E35488EB2F933BD72798E2F"> 
 <tr class="strow"> 
  <td class="stentry"> <p>0 </p></td> 
  <td class="stentry"> <p>Origine predefinita (corrispondenza centrale). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>1 </p></td> 
  <td class="stentry"> <p>Origine di corrispondenza continua. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>2 </p></td> 
  <td class="stentry"> <p>Allineamento casuale </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>3..6 </p></td> 
  <td class="stentry"> <p>Origine definita dall'utente. </p></td> 
 </tr> 
</table>

Il renderer applica la texture all&#39;oggetto in modo che il punto di ancoraggio della texture ( `anchor=`) coincida con il punto di origine specificato.

Ogni oggetto può definire fino a sei punti di origine (0, 1, 3, 4, 5, 6). Se si specifica un valore `align` ma il punto di origine corrispondente non è definito dall&#39;oggetto vignettatura, viene utilizzato il punto di origine predefinito (corrispondenza centrale).

`align=2` Specifica l&#39;allineamento casuale della trama, nel qual caso `anchor=` viene effettivamente ignorato.

Utilizzato principalmente per materiali da tappezzeria, possibilmente per tessuti di abbigliamento, per gestire l&#39;allineamento della texture tra oggetti adiacenti.

## Proprietà {#section-350fadc87dcf4812a8a02d1c3d6697a0}

Attributo materiale. Ignorato se è selezionato un oggetto cornice per rivestimenti per pareti, armadi, accessori o finestre o se il materiale non è una texture ripetibile.

## Predefinito {#section-3231c2854bae4477836b626ac208dd34}

`catalog::Alignment`, se il materiale è basato su una voce di catalogo, altrimenti 0 (corrisponde al centro).

## Consultate anche {#section-945d1ce275df487d9d564d4043156c79}

[catalogo::Alignment](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-alignment.md#reference-e52152e8dc244d0aa13b40c615d0f399) , [ancoraggio=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-anchor.md#reference-d53923d785c9442997dc7f2199524c26)
