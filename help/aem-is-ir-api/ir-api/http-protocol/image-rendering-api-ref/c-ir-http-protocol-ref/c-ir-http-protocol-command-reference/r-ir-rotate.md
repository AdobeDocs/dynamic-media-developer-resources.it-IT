---
description: Angolo di rotazione del materiale. Definisce l'angolo di rotazione per i materiali.
seo-description: Angolo di rotazione del materiale. Definisce l'angolo di rotazione per i materiali.
seo-title: rotate
solution: Experience Manager
title: rotate
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 497cd8ea-c6a4-45d2-b5e0-0898ac00913d
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '134'
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

Ruotare i materiali di texture ripetibili (esclusi i sfondi) di multipli di 45 gradi se applicati a oggetti piatti o a oggetti piano.

Ruotate i materiali di texture ripetibili con angoli arbitrari se applicati agli oggetti Flowline e Sketch.

Ruotare i materiali del decallo per angoli arbitrari.

Gli angoli positivi ruotano in senso orario. La texture o il decallo viene ruotato intorno al punto di ancoraggio ( `anchor=`); il punto di ancoraggio rimane allineato con l&#39;origine dell&#39;oggetto di destinazione.

## Proprietà {#section-ad4d07897ca24f63af1a4062f8618e36}

Attributo materiale. Ignorati da tinta unita, carta da parati, armadio e materiali per il trattamento delle finestre. *`angle`* deve essere un multiplo di 45 per le texture ripetibili, a meno che non venga applicato a Oggetti di flusso o sketch.

## Predefinito {#section-14c991e71b74449db8ff18a775949b28}

`rotate=0`, per nessuna rotazione.

## Consultate anche {#section-f73c00e9368b478dac1fd15bb4367a12}

[anchor=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-anchor.md#reference-d53923d785c9442997dc7f2199524c26)
