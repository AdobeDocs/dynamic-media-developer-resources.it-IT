---
description: Ancoraggio immagine (punto di attivazione). Specifica il punto di ancoraggio della texture (punto di attivazione) della texture o del materiale del decallo ripetibile.
seo-description: Ancoraggio immagine (punto di attivazione). Specifica il punto di ancoraggio della texture (punto di attivazione) della texture o del materiale del decallo ripetibile.
seo-title: ancoraggio
solution: Experience Manager
title: ancoraggio
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 1e695882-f97a-4208-b595-2851b91bdbfe
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '219'
ht-degree: 1%

---


# ancoraggio{#anchor}

Ancoraggio immagine (punto di attivazione). Specifica il punto di ancoraggio della texture (punto di attivazione) della texture o del materiale del decallo ripetibile.

`anchor= *``*, *`xy`*`

`anchorN= *``*, *`xnyn`*`

<table id="simpletable_1D8E91D8424A424787C4D20C9B040115"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> x</span>,  <span class="varname"> y</span> </p></td> 
  <td class="stentry"> <p>Offset pixel dall’angolo superiore sinistro dell’immagine sorgente (int, int). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> xn</span>,  <span class="varname"> yn</span> </p></td> 
  <td class="stentry"> <p>Offset normalizzato dal centro dell’immagine sorgente (reale, reale). </p></td> 
 </tr> 
</table>

Una texture ripetibile viene applicata a un oggetto vignettatura, in modo che il punto di ancoraggio della texture ( `anchor=`) si trovi nel punto di origine della texture dell&#39;oggetto.

Un&#39;immagine decal viene applicata a un oggetto vignettatura, in modo che il punto di ancoraggio decal si trovi nel punto di origine decal dell&#39;oggetto. La posizione del decallo può essere regolata ulteriormente utilizzando il comando `pos=`.

`anchorN=0,0` posiziona l’ancoraggio immagine al centro dell’immagine sorgente. `anchorN=-0.5,-0.5` oppure  `anchor=0,0` si trova nell’angolo superiore sinistro e  `anchorN=0.5,0.5` nell’angolo inferiore destro dell’immagine sorgente.

## Proprietà {#section-91f929d35cd745ab9e1eeecf45fcedae}

**Attributo** materiale. Ignorato se `align=2` o se il materiale non è una texture ripetibile, una carta da parati o un decallo.

## Predefinito {#section-b06d728c2f664c29bacf810eefcbde69}

`catalog::Anchor`, se il materiale è basato su una voce di catalogo. In caso contrario, `anchor=0,0` (l&#39;angolo in alto a sinistra dell&#39;immagine) per texture e sfondi ripetibili, e `anchorN=0,0` (il centro dell&#39;immagine) per i decali.

## Consultate anche {#section-b18bf0b035644ca5aedebbc64373718e}

[catalogo::Ancoraggio](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-cat-anchor.md#reference-d9b1d49db1fc440686f64b84453297ab) ,  [align=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-align.md#reference-4d63baa522ce42f9b15167ba34c5c6a7)
