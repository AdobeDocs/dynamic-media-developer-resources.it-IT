---
title: rotate
description: Angolo di rotazione del materiale. Definisce l'angolo di rotazione dei materiali.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 355d9691-c04b-44a6-9563-5bef185cfa7e
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '123'
ht-degree: 4%

---

# rotate{#rotate}

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

Gli angoli positivi ruotano in senso orario. La texture o la decalcomania viene ruotata attorno al punto di ancoraggio ( `anchor=`); il punto di ancoraggio rimane allineato con l&#39;origine dell&#39;oggetto di destinazione.

## Proprietà {#section-ad4d07897ca24f63af1a4062f8618e36}

Attributo materiale. Ignorato dai materiali di colore solido, carta da parati, armadio e trattamento delle finestre. *`angle`* Deve essere un multiplo di 45 per le texture ripetibili, a meno che non sia applicato agli oggetti di disegno o di linea di flusso.

## Predefinito {#section-14c991e71b74449db8ff18a775949b28}

`rotate=0`, senza rotazione.

## Consultate anche {#section-f73c00e9368b478dac1fd15bb4367a12}

[ancoraggio=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-anchor.md#reference-d53923d785c9442997dc7f2199524c26)
