---
description: Abilita l'ottimizzazione di FXG.
seo-description: Abilita l'ottimizzazione di FXG.
seo-title: enableVisibleAttributeOptimization
solution: Experience Manager
title: enableVisibleAttributeOptimization
uuid: 7f79aa12-6364-4b34-b547-88d4a778c015
feature: Dynamic Media Classic, SDK/API
role: Sviluppatore, Business Practices
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '108'
ht-degree: 2%

---


# enableVisibleAttributeOptimization{#enablevisibleattributeoptimization}

Abilita l&#39;ottimizzazione di FXG.

<table id="simpletable_FDE0D8786BC747AF87A336452500E695"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> &amp;enableVisibleAttributeOptimization</span> </p> </td> 
  <td class="stentry"> <p>0|1 </p></td> 
 </tr> 
</table>

Rimuove gli elementi la cui visibilità è impostata su false in FXG mentre trasmetti questo FXG che a sua volta riduce il tempo di elaborazione di FXG. Anche se rimuove come false solo gli elementi con visibilità che non avrebbero alcun impatto su nessun altro elemento in FXG. Ad esempio, se il testo è presente su `Path` e la visibilità di `Path` è impostata su false, non viene rimosso da FXG anche con questo modificatore abilitato, perché il testo deve essere disegnato su questo percorso.

Il valore predefinito è 1.
