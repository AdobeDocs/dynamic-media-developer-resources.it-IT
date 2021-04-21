---
description: FlyoutZoomView.tip
solution: Experience Manager
title: FlyoutZoomView.tip
feature: Dynamic Media Classic,Viewers,SDK/API,Mix Media Sets
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '108'
ht-degree: 4%

---


# FlyoutZoomView.tip{#flyoutzoomview-tip}

` [FlyoutZoomView.|<containerId>_flyout.]tip= *``*[, *``*][, *`durevolationcountfade`*]`

<table id="table_E314540D347D47699C04EB80D20C0721"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> durata</span></span> </p> </td> 
   <td colname="col2"> <p> Specifica il numero di secondi in cui il testo della descrizione viene visualizzato prima che venga nascosto. Se è impostato su <span class="codeph"> -1</span>, il messaggio viene sempre visualizzato, anche se l’utente attiva il riquadro a comparsa. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> count</span></span> </p> </td> 
   <td colname="col2"> <p> Specifica il numero di volte in cui il testo viene visualizzato quando si visualizzano nuove immagini nel set. Il valore <span class="codeph"> -1</span> indica che il testo viene sempre visualizzato quando si visualizza un'immagine nel set. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> dissolvenza</span></span> </p> </td> 
   <td colname="col2"> Specifica la durata di un'animazione di dissolvenza che si verifica quando il testo viene visualizzato o scompare. Un valore di <span class="codeph"> 0</span> non indica alcuna transizione di dissolvenza. </td> 
  </tr> 
 </tbody> 
</table>

## Proprietà {#section-65be9301796240e38f31818229da7acc}

Facoltativo.

## Predefinito {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`3,1,0.3`

## Esempio {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`tip=1,-1,0`
