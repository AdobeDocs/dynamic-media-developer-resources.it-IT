---
title: Riflessi
description: Le vignettature possono essere create per includere dati di riflessione quasi 3D.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: f67ede68-03c0-461f-a16d-a308f76fd24c
TQID: 'https://experienceleague.adobe.com/IzqnNnq7aFgXgEYQ6MJwxqnajYSJlULdEKxaa0OtGWI'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 140
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
   <td> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-rough.md#reference-00add846b09f4dc39420bda1ca414180" type="reference" format="dita" scope="local"> <span class="codeph"> approssimativo= </span> </a> </p> </td> 
   <td> <p>Rugosità della superficie </p> </td> 
   <td> <p>40% </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-type.md#reference-128c7de89e2d46838019b560f3f84a35" type="reference" format="dita" scope="local"> <span class="codeph"> tipo=</span> </a> </p> </td> 
   <td> <p>Tipo di materiale </p> </td> 
   <td> <p>0 (sconosciuto) </p> </td> 
  </tr> 
 </tbody> 
</table>

Il renderer regola l&#39;intervallo degli attributi `gloss=` e `rough=` in base a `type=`. Alcuni tipi di materiale, come il tessuto, sono meno riflettenti rispetto a quelli come la pietra o il metallo. Inoltre, la stessa quantità di brillantezza specificata per una causa spesso un effetto di riflessione diverso rispetto all&#39;altra. L&#39;attributo `gloss=` e la rugosità hanno una gamma abbastanza ampia se `type=` non è specificato o è impostato su `0`.

`glossmap=` Utilizzato per controllare la lucidità di un materiale pixel per pixel.
