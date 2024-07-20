---
title: ancoraggio
description: Ancoraggio immagine (punto attivo). Specifica il punto di ancoraggio della texture (punto attivo) del materiale di texture o decalcomania ripetibile.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: ea2c5dce-6eb1-4f05-80bd-7336deb08b9e
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '200'
ht-degree: 1%

---

# ancoraggio{#anchor}

Ancoraggio immagine (punto attivo). Specifica il punto di ancoraggio della texture (punto attivo) del materiale di texture o decalcomania ripetibile.

`anchor= *`x`*, *`y`*`

`anchorN= *`xn`*, *`yn`*`

<table id="simpletable_1D8E91D8424A424787C4D20C9B040115"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> x</span>, <span class="varname"> y</span> </p></td> 
  <td class="stentry"> <p>Offset pixel dall'angolo superiore sinistro dell'immagine sorgente (int, int). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> xn</span>, <span class="varname"> yn</span> </p></td> 
  <td class="stentry"> <p>Offset normalizzato dal centro dell'immagine sorgente (reale, reale). </p></td> 
 </tr> 
</table>

A un oggetto vignettatura viene applicata una texture ripetibile, in modo che il punto di ancoraggio della texture ( `anchor=`) si trovi nel punto di origine della texture dell&#39;oggetto.

Un&#39;immagine di decalcomania viene applicata a un oggetto vignettatura, in modo che il punto di ancoraggio della decalcomania si trovi nel punto di origine della decalcomania dell&#39;oggetto. La posizione della decalcomania può essere ulteriormente regolata utilizzando il comando `pos=`.

`anchorN=0,0` Posiziona l&#39;ancoraggio immagine al centro dell&#39;immagine di origine. `anchorN=-0.5,-0.5` o `anchor=0,0` si trova nell&#39;angolo superiore sinistro e `anchorN=0.5,0.5` nell&#39;angolo inferiore destro dell&#39;immagine di origine.

## Proprietà {#section-91f929d35cd745ab9e1eeecf45fcedae}

**Attributo materiale**. Ignorato se `align=2` o se il materiale non è una texture ripetibile, uno sfondo o una decalcomania.

## Predefinito {#section-b06d728c2f664c29bacf810eefcbde69}

`catalog::Anchor`, se il materiale è basato su una voce di catalogo. In caso contrario, `anchor=0,0` (l&#39;angolo in alto a sinistra dell&#39;immagine) per texture e sfondi ripetibili e `anchorN=0,0` (il centro dell&#39;immagine) per decalcomanie.

## Consultate anche {#section-b18bf0b035644ca5aedebbc64373718e}

[catalogo::ancoraggio](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-cat-anchor.md#reference-d9b1d49db1fc440686f64b84453297ab) , [allineamento=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-align.md#reference-4d63baa522ce42f9b15167ba34c5c6a7)
