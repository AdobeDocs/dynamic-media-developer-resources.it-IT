---
description: La barra di controllo secondaria è l’area rettangolare che contiene i pulsanti Prima e Ultima pagina e un indicatore di pagina se disponibile in CSS.
seo-description: La barra di controllo secondaria è l’area rettangolare che contiene i pulsanti Prima e Ultima pagina e un indicatore di pagina se disponibile in CSS.
seo-title: Barra di controllo secondaria
solution: Experience Manager
title: Barra di controllo secondaria
topic: Dynamic media
uuid: 38217d2a-8668-46e1-9df1-f29c1c7e0798
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---


# Barra di controllo secondaria{#secondary-control-bar}

La barra di controllo secondaria è l’area rettangolare che contiene i pulsanti Prima e Ultima pagina e un indicatore di pagina se disponibile in CSS.

Per impostazione predefinita, viene visualizzata solo sui telefoni cellulari e nella parte inferiore del visualizzatore. L’intera larghezza del visualizzatore disponibile è sempre sufficiente. È possibile modificarne il colore, l&#39;altezza e la posizione verticale mediante CSS, rispetto al contenitore del visualizzatore.

L&#39;aspetto della barra di controllo secondaria è controllato dal seguente selettore di classe CSS:

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
   <td colname="col1"> <p> <span class="codeph"> top  </span> </p> </td> 
   <td colname="col2"> <p>Posizione nella parte superiore del visualizzatore. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> bottom  </span> </p> </td> 
   <td colname="col2"> <p>Posizione nella parte inferiore del visualizzatore. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Altezza della barra di controllo principale. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color  </span> </p> </td> 
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

