---
description: Maschera affilata. Maschera definizione dettagli il livello o l'immagine di visualizzazione finale, dopo tutte le proporzioni, se layer=comp.
solution: Experience Manager
title: op_usmR
feature: Dynamic Media Classic, SDK/API
role: Developer,User
exl-id: 51a779be-568b-40e5-99d9-e875023a2b2c
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '145'
ht-degree: 2%

---

# op_usmR{#op-usmr}

Maschera affilata. Maschera definizione dettagli il livello o l&#39;immagine di visualizzazione finale, dopo tutte le proporzioni, se layer=comp.

I parametri vengono applicati così come sono, indipendentemente dal fatto che si sia verificato il campionamento in basso.

`op_usmR= *``*[, *``*[, *``*[, *`amountRreboldmonochrome`*]]]`

<table id="simpletable_0697E3BCB45F41C494D93A6017ADD2BF"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> importo</span></span> </p></td> 
  <td class="stentry"> <p>Fattore di resistenza del filtro (reale 0...5). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> radiusR</span></span> </p></td> 
  <td class="stentry"> <p>Raggio del kernel del filtro in pixel (reale 0...250). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> soglia</span></span> </p></td> 
  <td class="stentry"> <p>Livello di soglia del filtro (int 0...255). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> monocromatico</span></span> </p></td> 
  <td class="stentry"> <p>Impostare su 0 per applicare separatamente ciascun componente colore o su 1 per applicare solo la luminosità (intensità) dell'immagine. </p> <p><span class="codeph"> <span class="varname"> </span></span> monochromeis ignorato per le immagini in scala di grigi. </p> </td> 
 </tr> 
</table>

Anche la maschera di livello o la maschera composita è affilata.

## Proprietà {#section-fb5311b34d164946b74dadb32359518a}

Attributo di livello o attributo di visualizzazione. Si applica al livello corrente o all&#39;immagine di visualizzazione finale se `layer=comp`. Gli strati degli effetti li ignorano.

## Predefinito {#section-2bedc99866ff473e90e5ea36596d8362}

`op_usmR=0,0,0,0` senza effetti di maschera di contrasto.

## Consultate anche {#section-63f186b8a1b34ec4bb895230838502a4}

[qlt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-qlt.md#reference-f69ed0758c784b0385d979820546d352) ,  [op_sharpen=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-sharpen.md#reference-c32573230c6140f883efdaa201ea8541) ,  [op_usm](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-usm.md#reference-51ac75adadfe4346ab60953192d0a1aa)
