---
title: op_usm
description: Maschera di contrasto. Maschere di contrasto del livello o dell'immagine di visualizzazione finale, dopo tutte le operazioni di ridimensionamento, se layer=comp.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: a83d6326-9029-4c5c-a069-92bc81120866
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '151'
ht-degree: 1%

---

# op_usm{#op-usm}

Maschera di contrasto. Maschere di contrasto del livello o dell&#39;immagine di visualizzazione finale, dopo tutte le operazioni di ridimensionamento, se layer=comp.

Si presume che i parametri vengano applicati all&#39;immagine a risoluzione completa e che vengano ridimensionati durante l&#39;elaborazione di un&#39;immagine ricampionata verso il basso.

`op_usm= *`importo`*[, *`raggio`*[, *`soglia`*[, *`monocromatico`*]]]`

<table id="simpletable_0697E3BCB45F41C494D93A6017ADD2BF"> 
 <tr class="strow"> 
  <td class="stentry"> <p>Importo <span class="codeph"><span class="varname"></span></span> </p></td> 
  <td class="stentry"> <p>Fattore di intensità del filtro (reale 0...5). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>Raggio <span class="codeph"><span class="varname"></span></span> </p></td> 
  <td class="stentry"> <p>Raggio kernel del filtro in pixel (reale 0...250). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> soglia</span></span> </p></td> 
  <td class="stentry"> <p>Livello soglia filtro (int 0...255). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> monocromatico</span></span> </p></td> 
  <td class="stentry"> <p>Impostate questo valore su 0 per applicarlo separatamente a ogni componente di colore, oppure su 1 per applicarlo solo alla luminosità (intensità) dell'immagine. </p> <p> <span class="codeph"><span class="varname"> monocromatico</span></span> ignorato per le immagini in scala di grigio. </p></td> 
 </tr> 
</table>

Anche la maschera di livello o la maschera composita viene resa più nitida.

## Proprietà {#section-fb5311b34d164946b74dadb32359518a}

Attributo di livello o attributo di visualizzazione. Si applica al livello corrente o all&#39;immagine di visualizzazione finale se `layer=comp`. Ignorato dai livelli degli effetti.

## Predefinito {#section-2bedc99866ff473e90e5ea36596d8362}

`op_usm=0,0,0,0` per nessun effetto di maschera di contrasto.

## Consultate anche {#section-63f186b8a1b34ec4bb895230838502a4}

[qlt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-qlt.md#reference-f69ed0758c784b0385d979820546d352) , [op_sharpen=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-sharpen.md#reference-c32573230c6140f883efdaa201ea8541) , [op_usmR](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-usmr.md#reference-c0168bc1e3a24370883670c09bcb0fef)
