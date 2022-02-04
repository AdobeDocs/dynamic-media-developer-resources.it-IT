---
title: SpinView.maxloadradius
description: Rappresenta il numero massimo di fotogrammi da precaricare in ogni direzione quando la Visualizzazione 360 gradi è inattiva.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: e64fcd95-9660-4c1f-91b2-3ffc5a7493ce
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '152'
ht-degree: 2%

---

# SpinView.maxloadradius{#spinview-maxloadradius}

Rappresenta il numero massimo di fotogrammi da precaricare in ogni direzione quando la Visualizzazione 360 gradi è inattiva.

` [SpinView.|<containerId>_spinView.]maxloadradius= *`value`*[, *`highRes`*]`

<table id="table_06BEA037FA82467CAA88D1CA62AE972E"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> value</span></span> </p> </td> 
   <td colname="col2"> <p> Un valore di <span class="codeph"> -1</span> precarica tutti i fotogrammi del set. I fotogrammi precaricati vengono sempre visualizzati alla risoluzione originale in cui è stato inizialmente caricato SpinView. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> highRes</span></span> </p> </td> 
   <td colname="col2"> <p> Controlla la qualità dei fotogrammi precaricati. </p> <p>Quando è impostato su <span class="codeph"> 1</span> i fotogrammi vengono caricati in alta qualità, in base alle dimensioni del componente. </p> <p>Quando è impostato su <span class="codeph"> 0</span> viene caricato solo il riquadro di anteprima a bassa risoluzione.</p> <p>Il precaricamento in alta risoluzione migliora l'esperienza dell'utente, specialmente quando è abilitato l'spin automatico. Allo stesso tempo, si traduce in tempi di avvio più lenti e in un maggiore consumo di rete, quindi dovrebbe essere utilizzato con cura. Quando si utilizza il precaricamento ad alta risoluzione, i fotogrammi precaricati sono sempre nella risoluzione originale in cui il componente è stato inizialmente caricato. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Proprietà {#section-65be9301796240e38f31818229da7acc}

Facoltativo.

## Predefinito {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`6,0`

## Esempio {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`maxloadradius=12,1`
