---
title: pagina
description: Recupera la pagina. Recupera una pagina specifica in un file FXG con più pagine.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 7c72ceff-30d9-4e0b-8b4f-6cb0039d389e
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '49'
ht-degree: 2%

---

# pagina{#page}

Recupera la pagina. Recupera una pagina specifica in un file FXG con più pagine.

`page= *`val`*`

<table id="simpletable_E92560F812B64A36A3D108CA7DEED5AC"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> val</span></span> </p> </td> 
  <td class="stentry"> <p>Numero di pagina (la prima pagina è 1). </p></td> 
 </tr> 
</table>

## Predefinito {#section-3fd7fcc525b947c7a95457e50414ac9e}

Se `page` non è specificato, viene restituita la prima pagina per l’output raster e tutte le pagine per l’output PDF.
