---
description: L’indicatore della pagina visualizza l’indice della pagina corrente e il conteggio totale delle pagine. Appare nella barra di controllo principale sui sistemi desktop e tablet, sui telefoni cellulari viene aggiunto alla barra di controllo secondaria. L’indicatore di pagina può essere ridimensionato, skin e posizionato tramite CSS.
solution: Experience Manager
title: Indicatore di pagina
feature: Dynamic Media Classic,Visualizzatori,SDK/API,eCatalog
role: Developer,User
exl-id: c63af583-274c-4052-8186-604119a368af
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '261'
ht-degree: 2%

---

# Indicatore di pagina{#page-indicator}

L’indicatore della pagina visualizza l’indice della pagina corrente e il conteggio totale delle pagine. Appare nella barra di controllo principale sui sistemi desktop e tablet, sui telefoni cellulari viene aggiunto alla barra di controllo secondaria. L’indicatore di pagina può essere ridimensionato, skin e posizionato tramite CSS.

L’aspetto dell’indicatore di pagina è controllato dal seguente selettore di classe CSS:

`.s7ecatalogviewer .s7pageindicator`

<table id="table_94EE3F5BBE4547C0B4943471CEE7EDE4"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> Proprietà CSS </p> </th> 
   <th colname="col2" class="entry"> <p>Descrizione </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> top  </span> </p> </td> 
   <td colname="col2"> <p>Posizione dal bordo superiore della barra di controllo principale (su sistemi desktop e tablet) o della barra di controllo secondaria (su telefoni cellulari), compresa la spaziatura. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> right  </span> </p> </td> 
   <td colname="col2"> <p>Posizione dal bordo destro della barra di controllo principale (su sistemi desktop e tablet) o della barra di controllo secondaria (su telefoni cellulari), compresa la spaziatura. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> sinistra  </span> </p> </td> 
   <td colname="col2"> <p>Posizione dal bordo sinistro della barra di controllo principale (su sistemi desktop e tablet) o della barra di controllo secondaria (su telefoni cellulari), compresa la spaziatura. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> bottom  </span> </p> </td> 
   <td colname="col2"> <p>Posizione dal bordo inferiore della barra di controllo principale (su sistemi desktop e tablet) o della barra di controllo secondaria (su telefoni cellulari), compresa la spaziatura. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Larghezza dell’indicatore della pagina. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Altezza dell’indicatore della pagina. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color </span> </p> </td> 
   <td colname="col2"> <p>Colore font. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family  </span> </p> </td> 
   <td colname="col2"> <p>Nome carattere. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size  </span> </p> </td> 
   <td colname="col2"> <p>Dimensione del carattere. </p> </td> 
  </tr> 
 </tbody> 
</table>

Esempio: per impostare un indicatore di pagina di 56 x 28 pixel, centrato in orizzontale e posizionato 4 pixel dal fondo della barra di controllo principale, e utilizzare un carattere Helvetica da 14 pixel.

```
.s7ecatalogviewer  .s7pageindicator { 
 position:absolute; 
 bottom: 4px; 
 margin-left: -28px;  
 left: 50%; 
 width:56px; 
 height:28px; 
 font-family: Helvetica; 
 font-size:14px; 
}
```
