---
description: SpinView.maxloadradius
solution: Experience Manager
title: SpinView.maxloadradius
topic: Dynamic media
uuid: 8f475fa8-92d1-4663-bc12-1e65b76076ba
translation-type: tm+mt
source-git-commit: 846069e15c622efb1b899956ef84efba9e1a6729
workflow-type: tm+mt
source-wordcount: '134'
ht-degree: 2%

---


# SpinView.maxloadradius{#spinview-maxloadradius}

` [SpinView.|<containerId>_spinView.]maxloadradius= *``*[, *`valuehighRes`*]`

<table id="table_49FFD1BC53B846F09A6D214BC8C5C3FE"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> value</span></span> </p> </td> 
   <td colname="col2"> <p> Rappresenta il numero massimo di fotogrammi da precaricare in ogni direzione quando la Visualizzazione 360 gradi è inattiva. Un valore di <span class="codeph"> -1</span> precarica tutti i fotogrammi del set. I fotogrammi precaricati vengono sempre visualizzati alla risoluzione originale con cui era stata inizialmente caricata la Visualizzazione 360 gradi. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> highRes</span></span> </p> </td> 
   <td colname="col2"> <p> Controlla la qualità dei fotogrammi precaricati. Quando è impostata su <span class="codeph"> 1</span> i fotogrammi vengono caricati in alta qualità, con le stesse dimensioni del componente. Se è impostato su <span class="codeph"> 0</span> viene caricata solo la sezione di anteprima a bassa risoluzione. </p> <p>Il precaricamento ad alta risoluzione migliora l'esperienza dell'utente finale, soprattutto quando è abilitata la rotazione automatica. Allo stesso tempo, si traduce in tempi di avvio più lenti e in un maggiore consumo di rete, pertanto utilizzate con cautela. Quando si utilizza un precaricamento ad alta risoluzione, i fotogrammi precaricati si trovano sempre alla risoluzione originale alla quale il componente è stato inizialmente caricato. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Proprietà {#section-924163cb2f6542499f49894becef7fb5}

Facoltativo.

## Predefinito {#section-7a2128fd488941948aff18421f533ccf}

`6,0`

## Esempio {#section-622348a84fbe4ff4b5dd7eb53b044d83}

`maxloadradius=12,1`
