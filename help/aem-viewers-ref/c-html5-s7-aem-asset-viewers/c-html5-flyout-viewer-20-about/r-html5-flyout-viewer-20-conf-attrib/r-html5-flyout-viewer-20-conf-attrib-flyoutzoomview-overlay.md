---
description: 'null'
seo-description: 'null'
seo-title: FlyoutZoomView.overlay
solution: Experience Manager
title: FlyoutZoomView.overlay
topic: Dynamic media
uuid: e6e9e97c-5d9b-47ca-bae3-ed3371c5ff9b
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# FlyoutZoomView.overlay{#flyoutzoomview-overlay}

`[FlyoutZoomView.|<containerId>_flyout.]overlay=0|1`

<table id="table_D052090D052D4273B37872C0C7E09E4B"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> 0 | 1</span> </p> </td> 
   <td colname="col2"> <p> Controlla l'aspetto dell'evidenziazione della vista principale quando il menu a comparsa è attivo. Se è impostata su <span class="codeph"> 0</span>, l'area correntemente visibile nella finestra a comparsa viene evidenziata utilizzando gli stili forniti dai nomi delle classi CSS <span class="codeph"> .s7highlight</span> o <span class="codeph"> .s7cursor</span> (a seconda del valore del modificatore <span class="codeph"> highlightmode</span> ). Quando è impostato su <span class="codeph"> 1</span> , il componente entra in modalità "inverse", dove l’area correntemente visualizzata è completamente trasparente (nel caso <span class="codeph"> in cui la modalità</span> evidenziazione sia impostata su <span class="codeph"> evidenziazione</span>) oppure formattata con il nome della classe CSS <span class="codeph"> .s7cursor</span> (nel caso in cui la modalità <span class="codeph"></span> <span class="codeph"></span><span class="codeph"></span> evidenziazione sia impostata su ), ma l’area circostante viene riempita utilizzando gli stili forniti dal nome di classe .s7overlayTracciati. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Proprietà {#section-5526a5d19e7e4ee2a35b1c4816ed4202}

Facoltativo.

## Predefinito {#section-a08032f0fcf041c09e63c0238a339fc9}

`0`

## Esempio {#section-0338be21edd04ff1a3bed5c8319b61a4}

`overlay=1`
