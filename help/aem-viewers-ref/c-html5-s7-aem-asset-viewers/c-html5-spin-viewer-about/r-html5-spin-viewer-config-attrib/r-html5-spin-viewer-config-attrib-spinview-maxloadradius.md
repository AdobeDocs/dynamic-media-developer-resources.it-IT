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

` [SpinView.|<containerId>_spinView.]maxloadradius= *`valore`*[, *`highRes`*]`

<table id="table_49FFD1BC53B846F09A6D214BC8C5C3FE"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> valore</span></span> </p> </td> 
   <td colname="col2"> <p> Rappresenta il numero massimo di fotogrammi da precaricare in entrambe le direzioni quando la rotazione è inattiva. Un valore di <span class="codeph"> -1</span> precarica tutti i fotogrammi del set. I fotogrammi precaricati vengono sempre visualizzati alla risoluzione originale con cui è stata caricata la visualizzazione 360 gradi. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> highRes</span></span> </p> </td> 
   <td colname="col2"> <p> Controlla la qualità dei fotogrammi precaricati. Se impostato su <span class="codeph"> 1</span> i frame vengono caricati in alta qualità, in base alle dimensioni del componente. Se impostato su <span class="codeph"> 0</span> viene caricata solo la sezione di anteprima a bassa risoluzione. </p> <p>Il precaricamento ad alta risoluzione migliora l'esperienza dell'utente finale, in particolare quando è abilitata la rotazione automatica. Allo stesso tempo, si traduce in un tempo di avvio più lento e in un maggiore consumo di rete, pertanto è consigliabile prestare attenzione. Quando si utilizza un precaricamento ad alta risoluzione, i fotogrammi precaricati sono sempre alla risoluzione originale a cui il componente è stato caricato inizialmente. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Proprietà {#section-924163cb2f6542499f49894becef7fb5}

Facoltativo.

## Predefinito {#section-7a2128fd488941948aff18421f533ccf}

`6,0`

## Esempio {#section-622348a84fbe4ff4b5dd7eb53b044d83}

`maxloadradius=12,1`
