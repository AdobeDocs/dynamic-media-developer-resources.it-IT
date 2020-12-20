---
description: Abilita l’ottimizzazione di FXG.
seo-description: Abilita l’ottimizzazione di FXG.
seo-title: enableVisibleAttributeOptimization
solution: Experience Manager
title: enableVisibleAttributeOptimization
topic: Scene7 Image Serving - Image Rendering API
uuid: 7f79aa12-6364-4b34-b547-88d4a778c015
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '100'
ht-degree: 3%

---


# enableVisibleAttributeOptimization{#enablevisibleattributeoptimization}

Abilita l’ottimizzazione di FXG.

<table id="simpletable_FDE0D8786BC747AF87A336452500E695"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> &amp;enableVisibleAttributeOptimization</span> </p> </td> 
  <td class="stentry"> <p>0|1 </p></td> 
 </tr> 
</table>

Rimuove gli elementi la cui visibilità è impostata su false in FXG durante il passaggio del file FXG, riducendo il tempo di elaborazione del file FXG. Anche se rimuove solo gli elementi con visibilità come falsi che non avrebbero alcun impatto su altri elementi in FXG. Ad esempio, se il testo è presente su `Path` e la visibilità di `Path` è impostata su false, non viene rimosso dal file FXG anche se questo modificatore è abilitato, perché è necessario disegnare il testo su questo percorso.

Il valore predefinito è 1.
