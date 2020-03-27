---
description: 'null'
seo-description: 'null'
seo-title: Visualizzazione 360 gradi.doppio clic
solution: Experience Manager
title: Visualizzazione 360 gradi.doppio clic
topic: Dynamic media
uuid: c1eef3d1-471e-41ef-b899-008d45b616d0
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Visualizzazione 360 gradi.doppio clic{#spinview-doubleclick}

`[SpinView.|<containerId>_spinView.]doubleclick=none|zoom|reset|zoomReset`

<table id="table_E314540D347D47699C04EB80D20C0721"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|zoom|reset|zoomReset </span> </p> </td> 
   <td colname="col2"> <p> Configura la mappatura di azioni con doppio clic o tocco per le azioni di rotazione. Se questa opzione è impostata su <span class="codeph"> none, </span> viene disattivato il doppio clic o il tocco. Se impostato per <span class="codeph"> lo zoom, </span> facendo clic sulle rotazioni dell’immagine in un unico passaggio; CTRL+clic consente di ruotare un passaggio di rotazione. Se si imposta la <span class="codeph"> reimpostazione, </span> l'immagine viene reimpostata con un solo clic per ripristinare il livello iniziale di rotazione. Per <span class="codeph"> il ripristino dello zoom </span>, il ripristino viene applicato se il fattore di rotazione corrente è uguale o superiore al limite specificato. In caso contrario viene applicato il set 360 gradi. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Proprietà {#section-924163cb2f6542499f49894becef7fb5}

Facoltativo.

## Predefinito {#section-7a2128fd488941948aff18421f533ccf}

`reset` su computer desktop; `zoomReset` su dispositivi touch.

## Esempio {#section-622348a84fbe4ff4b5dd7eb53b044d83}

`doubleclick=zoom`
