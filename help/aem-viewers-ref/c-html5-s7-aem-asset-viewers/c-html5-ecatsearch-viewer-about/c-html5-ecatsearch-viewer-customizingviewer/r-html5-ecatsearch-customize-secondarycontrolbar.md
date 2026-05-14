---
title: Barra di controllo secondaria
description: La barra di controllo secondaria è l'area rettangolare che contiene i pulsanti Prima e Ultima pagina e un indicatore di pagina quando è disponibile in CSS.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: e5d6abe8-0ae9-4ccd-b311-5895e09310b2
TQID: 'https://experienceleague.adobe.com/NMaW0QPU2A3pUzpvMg3kbW8MmeLbJ1hZlCSGTEcG6Ko'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 171
ht-degree: 0%

---

# Barra di controllo secondaria{#secondary-control-bar}

La barra di controllo secondaria è l&#39;area rettangolare che contiene i pulsanti Prima e Ultima pagina e un indicatore di pagina quando è disponibile in CSS.

Per impostazione predefinita, viene visualizzato solo sui telefoni cellulari, nella parte inferiore del visualizzatore. La larghezza del visualizzatore è sempre l&#39;intera disponibile. È possibile modificarne il colore, l’altezza e la posizione verticale in base agli stili CSS, rispetto al contenitore del visualizzatore.

L’aspetto della barra di controllo secondaria è controllato dal seguente selettore di classe CSS:

`.s7ecatalogsearchviewer .s7secondarycontrols .s7controlbar`

<table id="table_2C8D322F57114A72B43053CB4539C65C"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> Proprietà CSS </p> </th> 
   <th colname="col2" class="entry"> <p>Descrizione </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> primi </span> </p> </td> 
   <td colname="col2"> <p>Posizione dalla parte superiore del visualizzatore. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> in basso </span> </p> </td> 
   <td colname="col2"> <p>Posizione dalla parte inferiore del visualizzatore. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> altezza </span> </p> </td> 
   <td colname="col2"> <p>Altezza della barra di controllo principale. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> colore di sfondo </span> </p> </td> 
   <td colname="col2"> <p>Colore di sfondo della barra di controllo secondaria. </p> </td> 
  </tr> 
 </tbody> 
</table>

Esempio: per impostare una barra di controllo secondaria grigia alta 72 pixel e posizionata nella parte inferiore del contenitore del visualizzatore.

```
.s7ecatalogsearchviewer .s7secondarycontrols .s7controlbar {  
 bottom: 0px; 
 height: 72px; 
}
```
