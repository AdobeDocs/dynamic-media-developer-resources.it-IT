---
description: Angolo di rotazione del materiale. Definisce l'angolo di rotazione per i materiali.
solution: Experience Manager
title: rotate
feature: Dynamic Media Classic, SDK/API
role: Sviluppatore, Business Practices
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '132'
ht-degree: 6%

---


# rotate{#rotate}

Angolo di rotazione del materiale. Definisce l&#39;angolo di rotazione per i materiali.

` rotate= *`angolo`*`

<table id="simpletable_F1A87ECD86E8429788825374A6882CB9"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> angolo </span> </p> </td> 
  <td class="stentry"> <p>Angolo di rotazione in gradi (reale). </p> </td> 
 </tr> 
</table>

Ruotare materiali di texture ripetibili (esclusi sfondi) di multipli di 45 gradi quando applicati a Oggetti piatti o Oggetti piano.

Ruotare i materiali di texture ripetibili con angoli arbitrari quando applicati a Flowline e Sketch Objects.

Ruotare i materiali di decal per angoli arbitrari.

Gli angoli positivi ruotano in senso orario. La texture o la decal vengono ruotate intorno al punto di ancoraggio ( `anchor=`); il punto di ancoraggio rimane allineato con l’origine dell’oggetto di destinazione.

## Proprietà {#section-ad4d07897ca24f63af1a4062f8618e36}

Attributo materiale. Ignorato da materiali per il trattamento a tinta unita, carta da parati, armadio e finestre. *`angle`* deve essere un multiplo di 45 per texture ripetibili, a meno che non sia applicato a Flowline o Sketch Objects.

## Predefinito {#section-14c991e71b74449db8ff18a775949b28}

`rotate=0`, senza rotazione.

## Consultate anche {#section-f73c00e9368b478dac1fd15bb4367a12}

[anchor=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-anchor.md#reference-d53923d785c9442997dc7f2199524c26)
