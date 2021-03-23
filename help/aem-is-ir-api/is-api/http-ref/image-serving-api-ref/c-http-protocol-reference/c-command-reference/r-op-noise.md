---
description: Aggiungi del rumore. Aggiunge un rumore casuale ai dati dell’immagine in primo piano o in primo piano di un livello di effetto.
seo-description: Aggiungi del rumore. Aggiunge un rumore casuale ai dati dell’immagine in primo piano o in primo piano di un livello di effetto.
seo-title: op_rumore
solution: Experience Manager
title: op_rumore
uuid: 531f7a94-149b-4090-a163-a1895156250b
feature: Dynamic Media Classic, SDK/API
role: Sviluppatore, Business Practices
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '119'
ht-degree: 1%

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
