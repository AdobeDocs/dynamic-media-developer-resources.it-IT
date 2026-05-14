---
title: op_noise
description: Aggiungete rumore. Aggiunge un disturbo casuale ai dati dell'immagine in primo piano o in primo piano di un livello di effetto.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: eeadd3ab-80ff-4f9b-b5b7-4f3da6feebde
TQID: 'https://experienceleague.adobe.com/Awfk7mrYylvJeu8mSTa--aSoVMx8Mk6IqDC6ZtFFu4U'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 92
ht-degree: 1%

---

# op_noise{#op-noise}

Aggiungete rumore. Aggiunge un disturbo casuale ai dati dell&#39;immagine in primo piano o in primo piano di un livello di effetto.

`op_noise= *`val`*[,uniform|gaussian[, *`monocromatico`*]]`

<table id="table_40675464E5824D52BF392ECCE2DDC03C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Valore <span class="codeph"></span> </p> </td> 
   <td colname="col2"> <p>Quantità di rumore in percentuale (0...100 int). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> uniforme</span> </p> </td> 
   <td colname="col2"> <p>Selezionare una distribuzione uniforme del rumore. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> gaussiano</span> </p> </td> 
   <td colname="col2"> <p>Selezionare Distribuzione del rumore gaussiano. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> monocromatico</span> </p> </td> 
   <td colname="col2"> <p>Impostate questo valore su 0 per il disturbo del colore, su 1 per il disturbo del grigio. </p> </td> 
  </tr> 
 </tbody> 
</table>

*`monochrome`* viene ignorato per le immagini in scala di grigio.

## Proprietà {#section-1f1a64c791f545a3bf1abd0b0e575d87}

Comando Livello. Si applica al livello corrente o all&#39;immagine composita se `layer=comp`.

## Predefinito {#section-d548868fa4b64a60bcb481cad1f8113e}

`op_noise=0,uniform,0`, senza alcun rumore.
