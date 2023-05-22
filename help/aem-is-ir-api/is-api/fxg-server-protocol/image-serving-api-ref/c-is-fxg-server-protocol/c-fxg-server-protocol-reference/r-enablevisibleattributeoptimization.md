---
description: Consente di ottimizzare FXG.
solution: Experience Manager
title: enableVisibleAttributeOptimization
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: a643694e-f6a2-424e-8f6e-3dbb4cdc41b3
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '94'
ht-degree: 3%

---

# enableVisibleAttributeOptimization{#enablevisibleattributeoptimization}

Consente di ottimizzare FXG.

<table id="simpletable_FDE0D8786BC747AF87A336452500E695"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> &amp;enableVisibleAttributeOptimization</span> </p> </td> 
  <td class="stentry"> <p>0|1 </p></td> 
 </tr> 
</table>

Rimuove gli elementi la cui visibilità è impostata come false in FXG durante il passaggio di questo FXG, il che a sua volta riduce il tempo di elaborazione di FXG. Anche se rimuove solo gli elementi con visibilità false che non influirebbero su nessun altro elemento in FXG. Ad esempio, se è presente del testo `Path` e visibilità di `Path` è impostato come falso, non viene rimosso da FXG nemmeno con questo modificatore abilitato perché è necessario disegnare del testo su questo percorso.

Il valore predefinito è 1.
