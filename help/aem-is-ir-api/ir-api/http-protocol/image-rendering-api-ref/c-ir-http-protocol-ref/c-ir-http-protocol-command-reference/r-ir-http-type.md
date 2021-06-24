---
description: Tipo di superficie materiale. Specifica il tipo di superficie del materiale.
solution: Experience Manager
title: Testo
feature: Dynamic Media Classic, SDK/API
role: Developer,Business Practitioner
exl-id: 333b8954-e256-4ba1-8055-c4d625470673
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '161'
ht-degree: 22%

---

# Testo{#type}

Tipo di superficie materiale. Specifica il tipo di superficie del materiale.

`type=0...19`

<table id="simpletable_482728CD58144E7BBB2912B2F105FDCA"> 
 <tr class="strow"> 
  <td class="stentry"> <p>0 </p></td> 
  <td class="stentry"> <p>Sconosciuto, il server utilizza l'impostazione predefinita </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>1 </p></td> 
  <td class="stentry"> <p>Altro </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>2 </p></td> 
  <td class="stentry"> <p>Legno naturale </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>3 </p></td> 
  <td class="stentry"> <p>Metallo lucido </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>4 </p></td> 
  <td class="stentry"> <p>Metallo spazzolato </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>5 </p></td> 
  <td class="stentry"> <p>Metallo antiquato </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>6 </p></td> 
  <td class="stentry"> <p>Pittura </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>7 </p></td> 
  <td class="stentry"> <p>Smalto/Lacca </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>8 </p></td> 
  <td class="stentry"> <p>Carta da parati </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>9 </p></td> 
  <td class="stentry"> <p>Plastica </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>10 </p></td> 
  <td class="stentry"> <p>Superficie solida </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>11 </p></td> 
  <td class="stentry"> <p>Laminato </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>12 </p></td> 
  <td class="stentry"> <p>Vinile </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>13 </p></td> 
  <td class="stentry"> <p>Ceramica </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>14 </p></td> 
  <td class="stentry"> <p>Pietra naturale </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>15 </p></td> 
  <td class="stentry"> <p>Vetro </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>16 </p></td> 
  <td class="stentry"> <p>Specchio </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>17 </p></td> 
  <td class="stentry"> <p>Stoffa </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>18 </p></td> 
  <td class="stentry"> <p>Tessuto </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>19 </p></td> 
  <td class="stentry"> <p>Moquette </p></td> 
 </tr> 
</table>

Utilizzato in combinazione con `gloss=` e `rough=` per controllare i comportamenti di riflessione e effetto lucido. Materiali diversi produrranno effetti diversi, anche se `gloss=` e `rough=` sono gli stessi.

## Proprietà {#section-2345b2508273426295ce8ac46182ea64}

Attributo materiale. Ignorato se la vignetta non include dati di riflessione 3D o se gli effetti lucentivi sono disattivati nella vignetta.

## Predefinito {#section-0989055fb74a41a3b2f2a47fe7d90a42}

`catalog::Type` se il materiale è basato su una voce di catalogo. Altrimenti `type=0`. Se non specificato, o se `type=0`, il server selezionerà un valore predefinito adatto a seconda dell&#39;oggetto di destinazione e degli altri attributi del materiale.

## Consultate anche {#section-7cf808b0bb3d4b4fbb7b9a850d5a038b}

[gloss=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-gloss.md#reference-325aef2ee51e4e1584a06047427340ca) ,  [grezzo=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-rough.md#reference-00add846b09f4dc39420bda1ca414180)
