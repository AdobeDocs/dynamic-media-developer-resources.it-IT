---
title: Riflessi
description: Le vignettature possono essere create per includere dati di riflessione quasi 3D.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: f67ede68-03c0-461f-a16d-a308f76fd24c
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '136'
ht-degree: 3%

---

# Riflessi{#reflections}

Le vignettature possono essere create per includere dati di riflessione quasi 3D.

Se create in questo modo, per definire le proprietà della superficie riflettente del materiale vengono utilizzati i seguenti attributi di materiale:

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
   <td> <p>Lucidità della superficie </p> </td> 
   <td> <p>Da vignettatura </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-glossmap.md#reference-99940148ae6a401482b2d03c68530f3a" type="reference" format="dita" scope="local"> <span class="codeph"> glossmap= </span> </a> </p> </td> 
   <td> <p>Variante lucida (immagine in scala di grigio) </p> </td> 
   <td> <p>Nessuno </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-rough.md#reference-00add846b09f4dc39420bda1ca414180" type="reference" format="dita" scope="local"> <span class="codeph"> ruvido= </span> </a> </p> </td> 
   <td> <p>Rugosità della superficie </p> </td> 
   <td> <p>40% </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-type.md#reference-128c7de89e2d46838019b560f3f84a35" type="reference" format="dita" scope="local"> <span class="codeph"> type=</span> </a> </p> </td> 
   <td> <p>Tipo di materiale </p> </td> 
   <td> <p>0 (sconosciuto) </p> </td> 
  </tr> 
 </tbody> 
</table>

Il renderer regola l&#39;intervallo del `gloss=` e `rough=` attributo in base a `type=`. Alcuni tipi di materiale, come il tessuto, sono meno riflettenti rispetto a quelli come la pietra o il metallo. Inoltre, la stessa quantità di brillantezza specificata per una causa spesso un effetto di riflessione diverso rispetto all&#39;altra. Attributo `gloss=` e la rugosità hanno una gamma abbastanza ampia se `type=` non è specificato o è impostato su `0`.

`glossmap=` Utilizzato per controllare la lucidità di un materiale pixel per pixel.
