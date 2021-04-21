---
description: Ancoraggio immagine (punto attivo). Specifica il punto di ancoraggio della texture (punto attivo) della texture o del materiale decal ripetibili.
solution: Experience Manager
title: ancoraggio
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '210'
ht-degree: 1%

---


# ancoraggio{#anchor}

Ancoraggio immagine (punto attivo). Specifica il punto di ancoraggio della texture (punto attivo) della texture o del materiale decal ripetibili.

`anchor= *``*, *`xy`*`

`anchorN= *``*, *`xnyn`*`

<table id="simpletable_1D8E91D8424A424787C4D20C9B040115"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> x</span>,  <span class="varname"> y</span> </p></td> 
  <td class="stentry"> <p>Offset pixel dall'angolo in alto a sinistra dell'immagine sorgente (int, int). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> xn</span>,  <span class="varname"> yn</span> </p></td> 
  <td class="stentry"> <p>Offset normalizzato dal centro dell'immagine sorgente (reale, reale). </p></td> 
 </tr> 
</table>

Una texture ripetibile viene applicata a un oggetto vignetta, in modo che il punto di ancoraggio della texture ( `anchor=`) sia posizionato nel punto di origine della texture dell&#39;oggetto.

Un&#39;immagine decal viene applicata a un oggetto vignetta, in modo che il punto di ancoraggio decal si trovi nel punto di origine decal dell&#39;oggetto. La posizione decal può essere ulteriormente regolata utilizzando il comando `pos=`.

`anchorN=0,0` posiziona l’ancoraggio immagine al centro dell’immagine sorgente. `anchorN=-0.5,-0.5` o  `anchor=0,0` si trova nell’angolo in alto a sinistra e  `anchorN=0.5,0.5` si trova nell’angolo in basso a destra dell’immagine sorgente.

## Proprietà {#section-91f929d35cd745ab9e1eeecf45fcedae}

**Attributo** materiale Ignorato se `align=2` o se il materiale non è una texture ripetibile, una carta da parati o un decal.

## Predefinito {#section-b06d728c2f664c29bacf810eefcbde69}

`catalog::Anchor`, se il materiale è basato su una voce di catalogo. In caso contrario, `anchor=0,0` (l&#39;angolo in alto a sinistra dell&#39;immagine) per texture e sfondi ripetibili e `anchorN=0,0` (il centro dell&#39;immagine) per decalcomanie.

## Consultate anche {#section-b18bf0b035644ca5aedebbc64373718e}

[catalogo::Ancoraggio](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-cat-anchor.md#reference-d9b1d49db1fc440686f64b84453297ab) ,  [align=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-align.md#reference-4d63baa522ce42f9b15167ba34c5c6a7)
