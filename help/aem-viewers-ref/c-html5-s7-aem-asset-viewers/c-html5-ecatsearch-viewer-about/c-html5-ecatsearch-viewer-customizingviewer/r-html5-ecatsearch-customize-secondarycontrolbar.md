---
description: La barra di controllo secondaria è l’area rettangolare contenente i pulsanti Prima e Ultima pagina e un indicatore di pagina quando è resa disponibile in CSS.
solution: Experience Manager
title: Barra di controllo secondaria
feature: Dynamic Media Classic,Visualizzatori,SDK/API,Ricerca eCatalog
role: Developer,Business Practitioner
exl-id: e5d6abe8-0ae9-4ccd-b311-5895e09310b2
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '180'
ht-degree: 1%

---

# Barra di controllo secondaria{#secondary-control-bar}

La barra di controllo secondaria è l’area rettangolare contenente i pulsanti Prima e Ultima pagina e un indicatore di pagina quando è resa disponibile in CSS.

Per impostazione predefinita viene visualizzato solo sui telefoni cellulari e si trova nella parte inferiore del visualizzatore. Richiede sempre l’intera larghezza disponibile del visualizzatore. È possibile modificarne il colore, l’altezza e la posizione verticale per CSS, rispetto al contenitore del visualizzatore.

L’aspetto della barra di controllo secondaria è controllato con il seguente selettore di classe CSS:

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
   <td colname="col2"> <p>Posizione dalla parte superiore del visualizzatore. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> bottom  </span> </p> </td> 
   <td colname="col2"> <p>Posizione dal fondo del visualizzatore. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Altezza della barra di controllo principale. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> colore di sfondo  </span> </p> </td> 
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
