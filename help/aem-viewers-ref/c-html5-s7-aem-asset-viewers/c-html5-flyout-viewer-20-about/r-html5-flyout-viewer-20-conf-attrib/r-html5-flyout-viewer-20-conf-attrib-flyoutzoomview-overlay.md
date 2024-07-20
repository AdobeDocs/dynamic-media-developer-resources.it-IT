---
title: FlyoutZoomView.overlay
description: FlyoutZoomView.overlay
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Flyout
role: Developer,User
exl-id: 7fbf24c6-900f-4e94-b879-3a8f95dc5c08
source-git-commit: 50dddf148345d2ca5243d5d7108fefa56d23dad6
workflow-type: tm+mt
source-wordcount: '103'
ht-degree: 2%

---

# FlyoutZoomView.overlay{#flyoutzoomview-overlay}

`[FlyoutZoomView.|<containerId>_flyout.]overlay=0|1`

<table id="table_D052090D052D4273B37872C0C7E09E4B"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> 0|1</span> </p> </td> 
   <td colname="col2"> <p> Controlla l'aspetto di evidenziazione della vista principale quando il menu a comparsa è attivo. Se è impostato su <span class="codeph"> 0</span>, l'area attualmente visibile nella finestra a comparsa viene evidenziata utilizzando gli stili forniti dai nomi di classe CSS <span class="codeph"> .s7highlight</span> o <span class="codeph"> .s7cursor</span> (a seconda del valore del modificatore <span class="codeph"> highlightmode</span>). Quando è impostato su <span class="codeph">, il componente 1</span> entra in modalità "inversa" in cui l'area visualizzata è completamente trasparente (nel caso in cui <span class="codeph"> highlightmode</span> sia impostato su <span class="codeph"> highlight</span>) o formattato con il nome di classe CSS <span class="codeph"> .s7cursor</span> (nel caso in cui <span class="codeph"> highlightmode</span> sia impostato su <span class="codeph"> cursor</span>), ma l'area circostante viene riempita utilizzando gli stili forniti dal nome di classe CSS <span class="codeph"> .s7overlay</span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Proprietà {#section-5526a5d19e7e4ee2a35b1c4816ed4202}

Facoltativo.

## Predefinito {#section-a08032f0fcf041c09e63c0238a339fc9}

`0`

## Esempio {#section-0338be21edd04ff1a3bed5c8319b61a4}

`overlay=1`
