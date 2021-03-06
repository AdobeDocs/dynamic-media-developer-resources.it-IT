---
title: ancoraggio
description: Ancoraggio immagine (punto attivo). Specifica il punto di ancoraggio della texture (punto attivo) della texture o del materiale decal ripetibili.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: ea2c5dce-6eb1-4f05-80bd-7336deb08b9e
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '200'
ht-degree: 2%

---

# ancoraggio{#anchor}

Ancoraggio immagine (punto attivo). Specifica il punto di ancoraggio della texture (punto attivo) della texture o del materiale decal ripetibili.

`anchor= *`x`*, *`y`*`

`anchorN= *`xn`*, *`yn`*`

<table id="simpletable_1D8E91D8424A424787C4D20C9B040115"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> x</span>, <span class="varname"> y</span> </p></td> 
  <td class="stentry"> <p>Offset pixel dall'angolo in alto a sinistra dell'immagine sorgente (int, int). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> xn</span>, <span class="varname"> yn</span> </p></td> 
  <td class="stentry"> <p>Offset normalizzato dal centro dell'immagine sorgente (reale, reale). </p></td> 
 </tr> 
</table>

Una texture ripetibile viene applicata a un oggetto vignetta, in modo che il punto di ancoraggio della texture ( `anchor=`) si trova nel punto di origine della texture dell&#39;oggetto.

Un&#39;immagine decal viene applicata a un oggetto vignetta, in modo che il punto di ancoraggio decal si trovi nel punto di origine decal dell&#39;oggetto. La posizione decal può essere ulteriormente regolata utilizzando `pos=` comando.

`anchorN=0,0` Posiziona l’ancoraggio dell’immagine al centro dell’immagine sorgente. `anchorN=-0.5,-0.5` o `anchor=0,0` si trova nell’angolo in alto a sinistra, e `anchorN=0.5,0.5` si trova nell’angolo in basso a destra dell’immagine sorgente.

## Proprietà {#section-91f929d35cd745ab9e1eeecf45fcedae}

**Attributo materiale**. Ignorato se `align=2`o se il materiale non è una texture ripetibile, una carta da parati o un decal.

## Predefinito {#section-b06d728c2f664c29bacf810eefcbde69}

`catalog::Anchor`, se il materiale è basato su una voce di catalogo. In caso contrario, `anchor=0,0` (angolo in alto a sinistra dell&#39;immagine) per texture e sfondi ripetibili, e `anchorN=0,0` (il centro dell&#39;immagine) per decals.

## Consultate anche {#section-b18bf0b035644ca5aedebbc64373718e}

[catalogo::Ancoraggio](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-cat-anchor.md#reference-d9b1d49db1fc440686f64b84453297ab) , [align=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-align.md#reference-4d63baa522ce42f9b15167ba34c5c6a7)
