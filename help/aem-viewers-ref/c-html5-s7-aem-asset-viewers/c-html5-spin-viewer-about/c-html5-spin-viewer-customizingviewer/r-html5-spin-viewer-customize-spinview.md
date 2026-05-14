---
title: Visualizzazione rotazione
description: La vista principale è costituita dall'immagine di rotazione.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Spin Sets
role: Developer,User
exl-id: d3274fe3-1a47-448e-acc6-6df77c6a4211
TQID: 'https://experienceleague.adobe.com/0OPnKfWiXaykg6nJ4cYTDonNYFD-dFvS2pIKRht-ww0'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 60
ht-degree: 1%

---

# Visualizzazione rotazione{#spin-view}

La vista principale è costituita dall&#39;immagine di rotazione.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**Proprietà CSS dell&#39;area visualizzatore principale**

L’aspetto dell’area di visualizzazione è controllato dal seguente selettore di classi CSS:

```
.s7spinviewer .s7spinview
```

<table id="table_94EE3F5BBE4547C0B4943471CEE7EDE4"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> Proprietà CSS </p> </th> 
   <th colname="col2" class="entry"> <p>Descrizione </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> colore di sfondo </span> </p> </td> 
   <td colname="col2"> <p> Colore di sfondo in formato esadecimale della visualizzazione principale. </p> </td> 
  </tr> 
 </tbody> 
</table>

Esempio: per rendere trasparente la visualizzazione principale.

```
.s7spinviewer .s7spinview { 
 background-color: transparent; 
}
```
