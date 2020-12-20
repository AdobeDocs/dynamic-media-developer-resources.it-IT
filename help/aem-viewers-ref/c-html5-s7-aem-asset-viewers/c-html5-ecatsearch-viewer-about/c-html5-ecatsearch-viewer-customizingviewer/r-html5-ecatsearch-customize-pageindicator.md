---
description: L'indicatore pagina visualizza l'indice della pagina corrente e il conteggio totale delle pagine. Appare nella barra di controllo principale sui sistemi desktop e tablet, sui telefoni cellulari viene aggiunto alla barra di controllo secondaria. L'indicatore della pagina può essere ridimensionato, con l'interfaccia e posizionato tramite CSS.
seo-description: L'indicatore pagina visualizza l'indice della pagina corrente e il conteggio totale delle pagine. Appare nella barra di controllo principale sui sistemi desktop e tablet, sui telefoni cellulari viene aggiunto alla barra di controllo secondaria. L'indicatore della pagina può essere ridimensionato, con l'interfaccia e posizionato tramite CSS.
seo-title: Indicatore pagina
solution: Experience Manager
title: Indicatore pagina
topic: Dynamic media
uuid: 1be6021b-3026-48ef-b121-eeb8270d2bae
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '295'
ht-degree: 2%

---


# Indicatore pagina{#page-indicator}

L&#39;indicatore pagina visualizza l&#39;indice della pagina corrente e il conteggio totale delle pagine. Appare nella barra di controllo principale sui sistemi desktop e tablet, sui telefoni cellulari viene aggiunto alla barra di controllo secondaria. L&#39;indicatore della pagina può essere ridimensionato, con l&#39;interfaccia e posizionato tramite CSS.

L&#39;indicatore della pagina di aspetto è controllato dal seguente selettore di classe CSS:

`.s7ecatalogsearchviewer .s7pageindicator`

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
   <td colname="col2"> <p>Posizione dal bordo superiore della barra di controllo principale (sui sistemi desktop e sui tablet) o dalla barra di controllo secondaria (sui telefoni cellulari), compresa la spaziatura. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> right  </span> </p> </td> 
   <td colname="col2"> <p>Posizione dal bordo destro della barra di controllo principale (sui sistemi desktop e sui tablet) o della barra di controllo secondaria (sui telefoni cellulari), compresa la spaziatura. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> left  </span> </p> </td> 
   <td colname="col2"> <p>Posizione dal bordo sinistro della barra di controllo principale (sui sistemi desktop e sui tablet) o della barra di controllo secondaria (sui telefoni cellulari), compresa la spaziatura. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> bottom  </span> </p> </td> 
   <td colname="col2"> <p>Posizione dal bordo inferiore della barra di controllo principale (sui sistemi desktop e sui tablet) o della barra di controllo secondaria (sui telefoni cellulari), compresa la spaziatura. </p> </td> 
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
   <td colname="col2"> <p>Nome font. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size  </span> </p> </td> 
   <td colname="col2"> <p>Dimensione del font. </p> </td> 
  </tr> 
 </tbody> 
</table>

Esempio: per impostare un indicatore di pagina di 56 x 28 pixel, centrato in orizzontale e posizionato 4 pixel dal fondo della barra di controllo principale, e utilizzare un font Helvetica di 14 pixel.

```
.s7ecatalogsearchviewer  .s7pageindicator { 
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

