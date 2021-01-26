---
description: 'All’interno di questo tipo, il campo pageReset è significativo per i tipi di risorse RenderSet e Catalog '
seo-description: 'All’interno di questo tipo, il campo pageReset è significativo per i tipi di risorse RenderSet e Catalog '
seo-title: ImageSetMemberUpdate
solution: Experience Manager
title: ImageSetMemberUpdate
topic: Dynamic Media Image Production System API
uuid: b0226d21-87ba-4e07-9819-79c9df3df13c
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '118'
ht-degree: 3%

---


# ImageSetMemberUpdate{#imagesetmemberupdate}

All’interno di questo tipo, il campo pageReset è significativo per i tipi di risorse di immagine RenderSet e Catalog:

* Per `RenderSet`, `pageReset` indica l&#39;inizio di un nuovo gruppo di viste/campioni di rendering.

* Per Catalogo, `pageReset` indica l&#39;inizio di una nuova visualizzazione di pagina. In genere, ci sono 2 immagini di pagina per visualizzazione pagina, ma è possibile avere più o meno.

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
   <td colname="col3"> Handle risorsa nell’array di membri del set di immagini. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> pageReset</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3">Ripristina la pagina. <p>L'impostazione viene ignorata e il valore viene forzato su true per <span class="codeph"> ImageSet</span> e <span class="codeph"> SpinSet</span>. </p></td> 
  </tr> 
 </tbody> 
</table>

