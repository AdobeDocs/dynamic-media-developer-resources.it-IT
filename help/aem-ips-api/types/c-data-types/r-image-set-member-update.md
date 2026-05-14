---
description: In questo tipo, il campo pageReset è significativo per i tipi di risorse immagine RenderSet e Catalog
solution: Experience Manager
title: ImageSetMemberUpdate
feature: Dynamic Media Classic,SDK/API,Image Sets
role: Developer,Admin
exl-id: 4c598afb-a80c-4fac-997f-ef1c7175430c
TQID: 'https://experienceleague.adobe.com/c9-ANQJjBlcpQYnSmrD8nQQ08Vllqt3ZcpW6IBJ9-4I'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 100
ht-degree: 3%

---

# [!DNL ImageSetMemberUpdate]{#imagesetmemberupdate}

All’interno di questo tipo, il campo pageReset è significativo per i tipi di risorse immagine RenderSet e Catalog:

* Per `RenderSet`, `pageReset` indica l&#39;inizio di un nuovo gruppo di campioni/viste di rendering.

* Per il catalogo, `pageReset` indica l&#39;inizio di una nuova visualizzazione di pagina. In genere, sono presenti 2 immagini pagina per visualizzazione pagina, ma è possibile averne un numero maggiore o minore.

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
   <td colname="col3"> Handle risorsa nell’array dei membri del set di immagini. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> pageReset</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:booleano</span> </td> 
   <td colname="col3">Reimposta la pagina. <p>L'impostazione viene ignorata e il valore viene forzato a true per <span class="codeph"> ImageSet</span> e <span class="codeph"> SpinSet</span>. </p></td> 
  </tr> 
 </tbody> 
</table>
