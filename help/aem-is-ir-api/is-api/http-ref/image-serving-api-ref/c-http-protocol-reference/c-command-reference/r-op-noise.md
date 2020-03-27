---
description: Aggiungete rumore. Aggiunge un disturbo casuale ai dati dell’immagine in primo piano o al primo piano di un livello di effetto.
seo-description: Aggiungete rumore. Aggiunge un disturbo casuale ai dati dell’immagine in primo piano o al primo piano di un livello di effetto.
seo-title: op_sound
solution: Experience Manager
title: op_sound
topic: Scene7 Image Serving - Image Rendering API
uuid: 531f7a94-149b-4090-a163-a1895156250b
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# op_sound{#op-noise}

Aggiungete rumore. Aggiunge un disturbo casuale ai dati dell’immagine in primo piano o al primo piano di un livello di effetto.

`op_noise= *``*[,uniform|gaussian[, *`valmonocromatico`*]]`

<table id="table_40675464E5824D52BF392ECCE2DDC03C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> val</span> </p> </td> 
   <td colname="col2"> <p>Quantità di rumore in percentuale (0...100 int). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> uniforme</span> </p> </td> 
   <td colname="col2"> <p>Selezionate una distribuzione uniforme del rumore. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> gossiano</span> </p> </td> 
   <td colname="col2"> <p>Selezionate la distribuzione del rumore gaussiana. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> monocromatico</span> </p> </td> 
   <td colname="col2"> <p>Imposta su 0 per il disturbo del colore, 1 per il disturbo del grigio. </p> </td> 
  </tr> 
 </tbody> 
</table>

*`monochrome`* viene ignorato per le immagini in scala di grigio.

## Proprietà {#section-1f1a64c791f545a3bf1abd0b0e575d87}

Livello, comando. Si applica al livello corrente o all’immagine composita, se `layer=comp`.

## Predefinito {#section-d548868fa4b64a60bcb481cad1f8113e}

`op_noise=0,uniform,0`, senza rumore.
