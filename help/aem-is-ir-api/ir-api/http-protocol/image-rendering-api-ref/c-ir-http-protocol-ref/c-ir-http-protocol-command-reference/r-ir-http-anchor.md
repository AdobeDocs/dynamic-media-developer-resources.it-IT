---
title: ancoraggio
description: Ancoraggio immagine (punto attivo). Specifica il punto di ancoraggio della texture (punto attivo) del materiale di texture o decalcomania ripetibile.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: ea2c5dce-6eb1-4f05-80bd-7336deb08b9e
TQID: 'https://experienceleague.adobe.com/fw1-eDsdT8jsgJfXBzb2bsLlcuTxKdLUmIeD5cFDiFE'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 202
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
