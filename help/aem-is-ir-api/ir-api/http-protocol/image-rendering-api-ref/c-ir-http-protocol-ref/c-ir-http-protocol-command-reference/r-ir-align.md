---
description: Allineamento del rendering della texture. Specifica quale dei punti di origine definiti dall'oggetto vignetta selezionato deve essere utilizzato.
solution: Experience Manager
title: allinea
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 0b76f173-809b-4b41-bf39-6b85f77ab2db
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '178'
ht-degree: 4%

---

# allinea {#align}

Allineamento del rendering della texture. Specifica quale dei punti di origine definiti dall&#39;oggetto vignetta selezionato deve essere utilizzato.

`align=0|1|2|3|4|5|6`

<table id="simpletable_D15233999E35488EB2F933BD72798E2F"> 
 <tr class="strow"> 
  <td class="stentry"> <p>0 </p></td> 
  <td class="stentry"> <p>Origine predefinita (al centro della corrispondenza). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>1 </p></td> 
  <td class="stentry"> <p>Origine di corrispondenza continua. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>2 </p></td> 
  <td class="stentry"> <p>Allineamento casuale. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>3,6 </p></td> 
  <td class="stentry"> <p>Origine definita dall'utente. </p></td> 
 </tr> 
</table>

Il renderer applica la texture all&#39;oggetto in modo che il punto di ancoraggio della texture ( `anchor=`) coincide con il punto di origine specificato.

Ogni oggetto può definire fino a sei punti di origine (0, 1, 3, 4, 5, 6). Se `align` viene specificato ma il punto di origine corrispondente non è definito dall&#39;oggetto vignetta; viene utilizzato il punto di origine predefinito (corrispondenza centrale).

`align=2` Specifica l&#39;allineamento casuale della texture, nel qual caso `anchor=` viene effettivamente ignorato.

Utilizzato principalmente per materiali di imbottitura, possibilmente per tessuti di abbigliamento, per gestire l&#39;allineamento della texture tra oggetti adiacenti.

## Proprietà {#section-350fadc87dcf4812a8a02d1c3d6697a0}

Attributo materiale. Ignorato se è selezionato un oggetto struttura per rivestimenti di pareti, mobili, accessori o finestre o se il materiale non è una texture ripetibile.

## Predefinito {#section-3231c2854bae4477836b626ac208dd34}

`catalog::Alignment`, se il materiale è basato su una voce di catalogo, altrimenti 0 (corrispondente al centro).

## Consultate anche {#section-945d1ce275df487d9d564d4043156c79}

[catalogo::Allineamento](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-alignment.md#reference-e52152e8dc244d0aa13b40c615d0f399) , [anchor=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-anchor.md#reference-d53923d785c9442997dc7f2199524c26)
