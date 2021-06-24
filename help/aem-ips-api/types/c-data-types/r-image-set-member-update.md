---
description: 'All’interno di questo tipo, il campo pageReset è significativo per i tipi di risorse immagine RenderSet e Catalog '
solution: Experience Manager
title: ImageSetMemberUpdate
feature: Dynamic Media Classic, SDK/API, Set di immagini
role: Developer,Administrator
exl-id: 4c598afb-a80c-4fac-997f-ef1c7175430c
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '109'
ht-degree: 3%

---

# ImageSetMemberUpdate{#imagesetmemberupdate}

All’interno di questo tipo, il campo pageReset è significativo per i tipi di risorse immagine RenderSet e Catalog:

* Per `RenderSet`, `pageReset` indica l&#39;inizio di un nuovo gruppo di visualizzazione/campioni di rendering.

* Per Catalogo, `pageReset` indica l’inizio di una nuova visualizzazione di pagina. In genere, ci sono 2 immagini di pagina per visualizzazione di pagina, ma è possibile avere più o meno.

## Parametri {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

<table id="table_04100BB8ABD84EF68B0A7CE3AD946414"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Nome </th> 
   <th colname="col2" class="entry"> Tipo </th> 
   <th colname="col3" class="entry"> Descrizione </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> assetHandle</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Handle di risorsa nell’array di membri del set di immagini. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> pageReset</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3">Ripristina la pagina. <p>L'impostazione viene ignorata e il valore viene forzato su true per <span class="codeph"> ImageSet</span> e <span class="codeph"> SpinSet</span>. </p></td> 
  </tr> 
 </tbody> 
</table>
