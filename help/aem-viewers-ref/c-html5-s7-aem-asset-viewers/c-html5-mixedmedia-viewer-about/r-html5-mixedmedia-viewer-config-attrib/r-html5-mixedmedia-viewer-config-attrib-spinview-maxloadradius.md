---
description: Rappresenta il numero massimo di fotogrammi da precaricare in ogni direzione quando la Visualizzazione 360 gradi è inattiva.
seo-description: Rappresenta il numero massimo di fotogrammi da precaricare in ogni direzione quando la Visualizzazione 360 gradi è inattiva.
seo-title: SpinView.maxloadradius
solution: Experience Manager
title: SpinView.maxloadradius
topic: Dynamic media
uuid: e1b9fa84-837c-465e-8d37-0b6867404cae
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '169'
ht-degree: 2%

---


# SpinView.maxloadradius{#spinview-maxloadradius}

Rappresenta il numero massimo di fotogrammi da precaricare in ogni direzione quando la Visualizzazione 360 gradi è inattiva.

` [SpinView.|<containerId>_spinView.]maxloadradius= *``*[, *`valuehighRes`*]`

<table id="table_06BEA037FA82467CAA88D1CA62AE972E"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> value</span></span> </p> </td> 
   <td colname="col2"> <p> Un valore di <span class="codeph"> -1</span> precarica tutti i fotogrammi del set. I fotogrammi precaricati vengono sempre visualizzati alla risoluzione originale con cui era stata inizialmente caricata la Visualizzazione 360 gradi. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> highRes</span></span> </p> </td> 
   <td colname="col2"> <p> Controlla la qualità dei fotogrammi precaricati. </p> <p>Se impostato su <span class="codeph"> 1</span>, il carico dei fotogrammi è di alta qualità, in base alle dimensioni del componente. </p> <p>Se è impostato su <span class="codeph"> 0</span> viene caricata solo la sezione di anteprima a bassa risoluzione. </p> <p>Il precaricamento ad alta risoluzione migliora l'esperienza dell'utente finale, soprattutto quando è abilitata la rotazione automatica. Allo stesso tempo, si traduce in tempi di avvio più lenti e in un maggiore consumo di rete, per cui dovrebbe essere utilizzato con cura. Quando si utilizza il precaricamento ad alta risoluzione, i fotogrammi precaricati sono sempre nella risoluzione originale alla quale il componente è stato inizialmente caricato. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Proprietà {#section-65be9301796240e38f31818229da7acc}

Facoltativo.

## Predefinito {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`6,0`

## Esempio {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`maxloadradius=12,1`
