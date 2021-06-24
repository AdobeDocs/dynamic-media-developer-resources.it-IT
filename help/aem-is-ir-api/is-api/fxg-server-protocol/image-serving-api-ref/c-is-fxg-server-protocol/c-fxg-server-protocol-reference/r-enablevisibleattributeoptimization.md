---
description: Abilita l'ottimizzazione di FXG.
solution: Experience Manager
title: enableVisibleAttributeOptimization
feature: Dynamic Media Classic, SDK/API
role: Developer,Business Practitioner
exl-id: a643694e-f6a2-424e-8f6e-3dbb4cdc41b3
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '99'
ht-degree: 3%

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
