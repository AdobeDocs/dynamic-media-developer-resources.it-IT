---
description: Maschera di contrasto. Maschera di contrasto sul livello o sull’immagine di visualizzazione finale, dopo aver ridimensionato il livello, se layer=comp.
seo-description: Maschera di contrasto. Maschera di contrasto sul livello o sull’immagine di visualizzazione finale, dopo aver ridimensionato il livello, se layer=comp.
seo-title: op_usmR
solution: Experience Manager
title: op_usmR
topic: Scene7 Image Serving - Image Rendering API
uuid: 98afd83c-097e-40b4-b0a6-647f70b95fae
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# op_usmR{#op-usmr}

Maschera di contrasto. Maschera di contrasto sul livello o sull’immagine di visualizzazione finale, dopo aver ridimensionato il livello, se layer=comp.

I parametri vengono applicati così com&#39;è, indipendentemente dal fatto che si sia verificato un downsampling.

`op_usmR= *``*[, *``*[, *``*[, *`amountRreboldmonochrome`*]]]`

<table id="simpletable_0697E3BCB45F41C494D93A6017ADD2BF"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> amount</span></span> </p></td> 
  <td class="stentry"> <p>Fattore di intensità del filtro (0...5 reale). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> radiusR</span></span> </p></td> 
  <td class="stentry"> <p>Filtra raggio kernel in pixel (numero reale 0...250). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> threshold</span></span> </p></td> 
  <td class="stentry"> <p>Livello di soglia del filtro (numero intero: 0...255). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> monocromatico</span></span> </p></td> 
  <td class="stentry"> <p>Impostare su 0 per ciascun componente di colore separatamente o su 1 per applicare solo la luminosità (intensità) dell’immagine. </p> <p><span class="codeph"> Per <span class="varname"> le immagini in scala di grigio viene ignorato il monocromatico</span></span> . </p> </td> 
 </tr> 
</table>

Anche la maschera di livello o la maschera composita vengono rese più nitide.

## Proprietà {#section-fb5311b34d164946b74dadb32359518a}

Attributo livello o attributo vista. Si applica al livello corrente o all’immagine della visualizzazione finale, se `layer=comp`. I livelli degli effetti li ignorano.

## Predefinito {#section-2bedc99866ff473e90e5ea36596d8362}

`op_usmR=0,0,0,0` senza effetti di maschera di contrasto.

## Consultate anche {#section-63f186b8a1b34ec4bb895230838502a4}

[qlt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-qlt.md#reference-f69ed0758c784b0385d979820546d352) , [op_sharpen=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-sharpen.md#reference-c32573230c6140f883efdaa201ea8541) , [op_usm](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-usm.md#reference-51ac75adadfe4346ab60953192d0a1aa)
