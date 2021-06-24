---
description: Recupera pagina. Recupera una pagina specifica in un FXG multipagina.
solution: Experience Manager
title: pagina
feature: Dynamic Media Classic, SDK/API
role: Developer,Business Practitioner
exl-id: 7c72ceff-30d9-4e0b-8b4f-6cb0039d389e
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '54'
ht-degree: 5%

---

# pagina{#page}

Recupera pagina. Recupera una pagina specifica in un FXG multipagina.

`page= *`val`*`

<table id="simpletable_E92560F812B64A36A3D108CA7DEED5AC"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> val</span></span> </p> </td> 
  <td class="stentry"> <p>Numero di pagina (la prima pagina è 1). </p></td> 
 </tr> 
</table>

## Predefinito {#section-3fd7fcc525b947c7a95457e50414ac9e}

Se `page` non è specificato, viene restituita la prima pagina per l’output raster e tutte le pagine per l’output PDF.
