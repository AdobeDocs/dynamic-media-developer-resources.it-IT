---
title: rotazione
description: Angolo di rotazione del materiale. Definisce l'angolo di rotazione dei materiali.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 355d9691-c04b-44a6-9563-5bef185cfa7e
TQID: 'https://experienceleague.adobe.com/prSGGMuV4SpFfhd8uCVzMRGpr-VBpowxE-UagKtpnqI'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 125
ht-degree: 2%

---

# rotazione{#rotate}

Angolo di rotazione del materiale. Definisce l&#39;angolo di rotazione dei materiali.

` rotate= *`angolo`*`

<table id="simpletable_F1A87ECD86E8429788825374A6882CB9"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> angolo </span> </p> </td> 
  <td class="stentry"> <p>Angolo di rotazione in gradi (reale). </p> </td> 
 </tr> 
</table>

Ruotare i materiali di texture ripetibili (esclusi gli sfondi) di multipli di 45° quando applicati a oggetti piatti o a oggetti piani.

Ruotate i materiali di texture ripetibili mediante angoli arbitrari quando applicate agli oggetti di sketch e di flusso.

Ruotare i materiali delle decalcomanie per angoli arbitrari.

Gli angoli positivi ruotano in senso orario. La trama o la decalcomania viene ruotata attorno al punto di ancoraggio ( `anchor=`); il punto di ancoraggio rimane allineato con l&#39;origine dell&#39;oggetto di destinazione.

## Proprietà {#section-ad4d07897ca24f63af1a4062f8618e36}

Attributo materiale. Ignorato dai materiali di colore solido, carta da parati, armadio e trattamento delle finestre. *`angle`* Deve essere un multiplo di 45 per le texture ripetibili, a meno che non sia applicato agli oggetti di disegno o di linea di flusso.

## Predefinito {#section-14c991e71b74449db8ff18a775949b28}

`rotate=0`, senza rotazione.

## Consultate anche {#section-f73c00e9368b478dac1fd15bb4367a12}

[ancoraggio=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-anchor.md#reference-d53923d785c9442997dc7f2199524c26)
