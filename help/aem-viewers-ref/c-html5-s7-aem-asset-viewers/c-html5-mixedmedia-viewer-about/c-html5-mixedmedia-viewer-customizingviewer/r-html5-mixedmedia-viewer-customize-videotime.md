---
description: L’ora del video è la visualizzazione numerica che mostra l’ora e la durata correnti del video in riproduzione.
solution: Experience Manager
title: Ora video
feature: Dynamic Media Classic,Visualizzatori,SDK/API,Set di file multimediali diversi
role: Developer,Business Practitioner
exl-id: 5efae314-5f37-4afc-9b9e-3108a8529e50
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '202'
ht-degree: 1%

---

# Ora video{#video-time}

L’ora del video è la visualizzazione numerica che mostra l’ora e la durata correnti del video in riproduzione.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

La famiglia di font, la dimensione del font e il colore del font dell’ora video sono tra le proprietà che CSS può controllare. Può anche essere posizionato tramite CSS rispetto alla barra di controllo che lo contiene.

L’aspetto dell’ora del video è controllato con il seguente selettore di classe CSS:

```
.s7mixedmediaviewer .s7videotime
```

## Proprietà CSS del tempo video {#css-properties-of-video-time}

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> top  </span> </p> </td> 
   <td colname="col2"> <p>Posizione dal bordo superiore, inclusa la spaziatura. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> right  </span> </p> </td> 
   <td colname="col2"> <p>Posizione dal bordo destro, compresa la spaziatura. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p> La larghezza del controllo del tempo video. Questa proprietà è necessaria per il corretto funzionamento di Internet Explorer 8 o versioni successive. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family  </span> </p> </td> 
   <td colname="col2"> <p>Famiglia di font da utilizzare per il testo di visualizzazione dell'ora. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size  </span> </p> </td> 
   <td colname="col2"> <p>Dimensione del font da utilizzare per il testo visualizzato in base all'ora. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color </span> </p> </td> 
   <td colname="col2"> <p>Il colore del font da utilizzare per il testo visualizzato in base all'ora. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Esempio {#section-e8caea0a303c425a8a637c2a47c06355}

Impostare il tempo video su grigio chiaro (esadecimale `#BBBBBB`), dimensionato a 12 pixel, posizionato 15 pixel dalla parte superiore della barra di controllo e 80 pixel dai bordi destri della barra di controllo.

```
.s7mixedmediaviewer .s7videotime { 
top:15px; 
right:80px; 
font-size:12px; 
color:#BBBBBB; 
width:60px;  
}
```
