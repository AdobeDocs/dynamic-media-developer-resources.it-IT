---
description: Rappresenta il numero massimo di fotogrammi da precaricare in ogni direzione quando la Visualizzazione 360 gradi è inattiva.
solution: Experience Manager
title: SpinView.maxloadradius
feature: Dynamic Media Classic,Visualizzatori,SDK/API,Set di file multimediali diversi
role: Developer,Business Practitioner
exl-id: e64fcd95-9660-4c1f-91b2-3ffc5a7493ce
source-git-commit: bfb350e68d9b7e86cec5ee75fe9280b12ce0e54e
workflow-type: tm+mt
source-wordcount: '161'
ht-degree: 2%

---

# SpinView.maxloadradius{#spinview-maxloadradius}

Rappresenta il numero massimo di fotogrammi da precaricare in ogni direzione quando la Visualizzazione 360 gradi è inattiva.

` [SpinView.|<containerId>_spinView.]maxloadradius= *``*[, *`valuehighRes`*]`

<table id="table_06BEA037FA82467CAA88D1CA62AE972E"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> value</span></span> </p> </td> 
   <td colname="col2"> <p> Un valore di <span class="codeph"> -1</span> precarica tutti i fotogrammi del set. I fotogrammi precaricati vengono sempre visualizzati alla risoluzione originale in cui è stato inizialmente caricato SpinView. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> highRes</span></span> </p> </td> 
   <td colname="col2"> <p> Controlla la qualità dei fotogrammi precaricati. </p> <p>Quando è impostato su <span class="codeph"> 1</span> il carico dei fotogrammi è di alta qualità, in corrispondenza delle dimensioni del componente. </p> <p>Se è impostato su <span class="codeph"> 0</span> viene caricato solo il riquadro di anteprima a bassa risoluzione. </p> <p>Il precaricamento in alta risoluzione migliora l'esperienza dell'utente finale, specialmente quando è abilitato il ciclo di rotazione automatica. Allo stesso tempo, si traduce in tempi di avvio più lenti e in un maggiore consumo di rete, quindi dovrebbe essere utilizzato con cura. Quando si utilizza il precaricamento ad alta risoluzione, i fotogrammi precaricati sono sempre nella risoluzione originale in cui il componente è stato inizialmente caricato. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Proprietà {#section-65be9301796240e38f31818229da7acc}

Facoltativo.

## Predefinito {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`6,0`

## Esempio {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`maxloadradius=12,1`
