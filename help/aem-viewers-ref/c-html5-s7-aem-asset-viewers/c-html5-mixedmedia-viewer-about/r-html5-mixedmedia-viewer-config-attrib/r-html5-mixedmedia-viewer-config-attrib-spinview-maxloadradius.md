---
title: SpinView.maxloadradius
description: Rappresenta il numero massimo di fotogrammi da precaricare in entrambe le direzioni quando la rotazione è inattiva.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: e64fcd95-9660-4c1f-91b2-3ffc5a7493ce
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '155'
ht-degree: 1%

---

# SpinView.maxloadradius{#spinview-maxloadradius}

Rappresenta il numero massimo di fotogrammi da precaricare in entrambe le direzioni quando la rotazione è inattiva.

` [SpinView.|<containerId>_spinView.]maxloadradius= *`value`*[, *`highRes`*]`

<table id="table_06BEA037FA82467CAA88D1CA62AE972E"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> Valore <span class="codeph"><span class="varname"></span></span> </p> </td> 
   <td colname="col2"> <p> Un valore di <span class="codeph"> -1</span> precarica tutti i fotogrammi del set. I fotogrammi precaricati vengono sempre visualizzati alla risoluzione originale con cui è stata caricata la visualizzazione 360 gradi. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> highRes</span></span> </p> </td> 
   <td colname="col2"> <p> Controlla la qualità dei fotogrammi precaricati. </p> <p>Se è impostato su <span class="codeph"> 1</span>, i frame vengono caricati di alta qualità, in base alle dimensioni del componente. </p> <p>Se è impostato su <span class="codeph"> 0</span>, viene caricata solo la sezione di anteprima a bassa risoluzione.</p> <p>Il precaricamento ad alta risoluzione migliora l'esperienza dell'utente, in particolare quando è abilitata la rotazione automatica. Allo stesso tempo, si traduce in un tempo di avvio più lento e in un maggiore consumo di rete, pertanto dovrebbe essere utilizzato con cautela. Quando si utilizza il precaricamento ad alta risoluzione, i fotogrammi precaricati sono sempre nella risoluzione originale a cui il componente è stato caricato inizialmente. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Proprietà {#section-65be9301796240e38f31818229da7acc}

Facoltativo.

## Predefinito {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`6,0`

## Esempio {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`maxloadradius=12,1`
