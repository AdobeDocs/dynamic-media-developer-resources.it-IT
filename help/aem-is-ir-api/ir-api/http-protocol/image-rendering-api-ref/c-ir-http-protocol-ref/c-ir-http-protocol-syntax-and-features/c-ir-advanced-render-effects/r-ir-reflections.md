---
description: Le vignette possono essere create per includere dati di riflessione vicino a 3D.
solution: Experience Manager
title: Riflessioni
feature: Dynamic Media Classic, SDK/API
role: Developer,Business Practitioner
exl-id: f67ede68-03c0-461f-a16d-a308f76fd24c
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '142'
ht-degree: 3%

---

# Riflessioni{#reflections}

Le vignette possono essere create per includere dati di riflessione vicino a 3D.

In tal caso, per definire le proprietà riflettenti della superficie del materiale vengono utilizzati i seguenti attributi di materiale:

<table id="table_8769C726A17E412FB41F7CB87690B1FE"> 
 <thead> 
  <tr> 
   <th class="entry"> <p>Attributo </p> </th> 
   <th class="entry"> <p>Descrizione </p> </th> 
   <th class="entry"> <p>Predefinito </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p><a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-gloss.md#reference-325aef2ee51e4e1584a06047427340ca" type="reference" format="dita" scope="local"> <span class="codeph"> gloss=</span> </a> </p> </td> 
   <td> <p>Lucidità superficiale </p> </td> 
   <td> <p>Da vignetta </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-glossmap.md#reference-99940148ae6a401482b2d03c68530f3a" type="reference" format="dita" scope="local"> <span class="codeph"> glossmap=  </span> </a> </p> </td> 
   <td> <p>Variazione della luminosità (immagine in scala di grigi) </p> </td> 
   <td> <p>Nessuno </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-rough.md#reference-00add846b09f4dc39420bda1ca414180" type="reference" format="dita" scope="local"> <span class="codeph"> grezzo=  </span> </a> </p> </td> 
   <td> <p>rugosità della superficie </p> </td> 
   <td> <p>40% </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-type.md#reference-128c7de89e2d46838019b560f3f84a35" type="reference" format="dita" scope="local"> <span class="codeph"> type=</span> </a> </p> </td> 
   <td> <p>Tipo di materiale </p> </td> 
   <td> <p>0 (sconosciuto) </p> </td> 
  </tr> 
 </tbody> 
</table>

Il renderer regola l’intervallo dell’attributo `gloss=` e `rough=` in base a `type=`. Alcuni tipi di materiale, come il tessuto, sono generalmente meno riflettenti dei tipi di materiale come la pietra o il metallo, e la stessa quantità di lucentezza specificata per uno si tradurrà in un effetto di riflessione diverso rispetto all&#39;altro. `gloss=`e la rugosità hanno una gamma abbastanza ampia se non  `type=` è specificato o è impostato su 0.

`glossmap=` può essere utilizzato per controllare la lucidità di un materiale in base a pixel per pixel.
