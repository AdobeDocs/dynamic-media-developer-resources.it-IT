---
description: SpinView.maxloadradius
solution: Experience Manager
title: SpinView.maxloadradius
uuid: 8f475fa8-92d1-4663-bc12-1e65b76076ba
feature: Dynamic Media Classic,Visualizzatori,SDK/API,Set 360 gradi
role: Sviluppatore, Business Practices
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '145'
ht-degree: 2%

---


# SpinView.maxloadradius{#spinview-maxloadradius}

` [SpinView.|<containerId>_spinView.]maxloadradius= *``*[, *`valuehighRes`*]`

<table id="table_49FFD1BC53B846F09A6D214BC8C5C3FE"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> value</span></span> </p> </td> 
   <td colname="col2"> <p> Rappresenta il numero massimo di fotogrammi da precaricare in ogni direzione quando la Visualizzazione 360 gradi è inattiva. Un valore di <span class="codeph"> -1</span> precarica tutti i fotogrammi del set. I fotogrammi precaricati vengono sempre visualizzati alla risoluzione originale in cui è stato inizialmente caricato SpinView. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> highRes</span></span> </p> </td> 
   <td colname="col2"> <p> Controlla la qualità dei fotogrammi precaricati. Quando è impostato su <span class="codeph"> 1</span> il carico dei fotogrammi è di alta qualità e corrisponde alle dimensioni del componente. Se è impostato su <span class="codeph"> 0</span> viene caricato solo il riquadro di anteprima a bassa risoluzione. </p> <p>Il precaricamento in alta risoluzione migliora l'esperienza dell'utente finale, specialmente quando è abilitato il ciclo di rotazione automatico. Allo stesso tempo, si traduce in un tempo di avvio più lento e in un maggiore consumo di rete, quindi utilizzare con cautela. Quando si utilizza un precaricamento ad alta risoluzione, i fotogrammi precaricati sono sempre alla risoluzione originale a cui il componente è stato inizialmente caricato. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Proprietà {#section-924163cb2f6542499f49894becef7fb5}

Facoltativo.

## Predefinito {#section-7a2128fd488941948aff18421f533ccf}

`6,0`

## Esempio {#section-622348a84fbe4ff4b5dd7eb53b044d83}

`maxloadradius=12,1`
