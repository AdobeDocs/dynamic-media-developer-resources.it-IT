---
description: Aggiungi del rumore. Aggiunge un rumore casuale ai dati dell’immagine in primo piano o in primo piano di un livello di effetto.
solution: Experience Manager
title: op_rumore
feature: Dynamic Media Classic, SDK/API
role: Sviluppatore, Business Practices
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '99'
ht-degree: 2%

---


# op_rumore{#op-noise}

Aggiungi del rumore. Aggiunge un rumore casuale ai dati dell’immagine in primo piano o in primo piano di un livello di effetto.

`op_noise= *``*[,uniform|gaussian[, *`valmonocromatico`*]]`

<table id="table_40675464E5824D52BF392ECCE2DDC03C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> val</span> </p> </td> 
   <td colname="col2"> <p>Quantità di rumore in percentuale (0...100 int). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> uniforme</span> </p> </td> 
   <td colname="col2"> <p>Selezionare la distribuzione uniforme del rumore. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> gossiano</span> </p> </td> 
   <td colname="col2"> <p>Selezionare la distribuzione del rumore gaussiana. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> monocromatico</span> </p> </td> 
   <td colname="col2"> <p>Imposta su 0 per il rumore del colore, 1 per il rumore del grigio. </p> </td> 
  </tr> 
 </tbody> 
</table>

*`monochrome`* viene ignorato per le immagini in scala di grigi.

## Proprietà {#section-1f1a64c791f545a3bf1abd0b0e575d87}

Livello, comando. Si applica al livello corrente o all&#39;immagine composita se `layer=comp`.

## Predefinito {#section-d548868fa4b64a60bcb481cad1f8113e}

`op_noise=0,uniform,0`senza rumore.
