---
title: FlyoutZoomView.overlay
description: FlyoutZoomView.overlay
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Flyout
role: Developer,User
exl-id: 7fbf24c6-900f-4e94-b879-3a8f95dc5c08
source-git-commit: 50dddf148345d2ca5243d5d7108fefa56d23dad6
workflow-type: tm+mt
source-wordcount: '104'
ht-degree: 3%

---

# FlyoutZoomView.overlay{#flyoutzoomview-overlay}

`[FlyoutZoomView.|<containerId>_flyout.]overlay=0|1`

<table id="table_D052090D052D4273B37872C0C7E09E4B"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> 0 | 1</span> </p> </td> 
   <td colname="col2"> <p> Controlla l'aspetto di evidenziazione della vista principale quando il menu a comparsa è attivo. Se impostato su <span class="codeph"> 0</span>, l’area attualmente visibile nella finestra a comparsa viene evidenziata utilizzando gli stili forniti da <span class="codeph"> .s7highlight</span> o da <span class="codeph"> .s7cursor</span> Nomi di classi CSS (a seconda del valore di <span class="codeph"> highlightmode</span> modificatore). Se impostato su <span class="codeph"> 1</span> il componente entra in modalità "inversa" dove l’area attualmente visualizzata è completamente trasparente (nel caso in cui <span class="codeph"> highlightmode</span> è impostato su <span class="codeph"> evidenziare</span>) o formattato con <span class="codeph"> .s7cursor</span> Nome classe CSS (nel caso <span class="codeph"> highlightmode</span> è impostato su <span class="codeph"> cursore</span>), ma l'area circostante viene riempita utilizzando gli stili forniti da <span class="codeph"> .s7overlay</span> Nome classe CSS. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Proprietà {#section-5526a5d19e7e4ee2a35b1c4816ed4202}

Facoltativo.

## Predefinito {#section-a08032f0fcf041c09e63c0238a339fc9}

`0`

## Esempio {#section-0338be21edd04ff1a3bed5c8319b61a4}

`overlay=1`
