---
title: SpinView.maxloadradius
description: SpinView.maxloadradius
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Spin Sets
role: Developer,User
exl-id: 4adba865-0b03-469e-a88c-2c3982422a68
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '134'
ht-degree: 2%

---

# SpinView.maxloadradius{#spinview-maxloadradius}

` [SpinView.|<containerId>_spinView.]maxloadradius= *`value`*[, *`highRes`*]`

<table id="table_49FFD1BC53B846F09A6D214BC8C5C3FE"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> value</span></span> </p> </td> 
   <td colname="col2"> <p> Rappresenta il numero massimo di fotogrammi da precaricare in ogni direzione quando la Visualizzazione 360 gradi è inattiva. Un valore di <span class="codeph"> -1</span> precarica tutti i fotogrammi del set. I fotogrammi precaricati vengono sempre visualizzati alla risoluzione originale in cui è stato inizialmente caricato SpinView. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> highRes</span></span> </p> </td> 
   <td colname="col2"> <p> Controlla la qualità dei fotogrammi precaricati. Quando è impostato su <span class="codeph"> 1</span> i fotogrammi vengono caricati in alta qualità, in base alle dimensioni del componente. Quando è impostato su <span class="codeph"> 0</span> viene caricato solo il riquadro di anteprima a bassa risoluzione. </p> <p>Il precaricamento in alta risoluzione migliora l'esperienza dell'utente finale, specialmente quando è abilitato il ciclo di rotazione automatico. Allo stesso tempo, si traduce in un tempo di avvio più lento e in un maggiore consumo di rete, quindi utilizzare con cautela. Quando si utilizza un precaricamento ad alta risoluzione, i fotogrammi precaricati sono sempre alla risoluzione originale in cui il componente è stato inizialmente caricato. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Proprietà {#section-924163cb2f6542499f49894becef7fb5}

Facoltativo.

## Predefinito {#section-7a2128fd488941948aff18421f533ccf}

`6,0`

## Esempio {#section-622348a84fbe4ff4b5dd7eb53b044d83}

`maxloadradius=12,1`
