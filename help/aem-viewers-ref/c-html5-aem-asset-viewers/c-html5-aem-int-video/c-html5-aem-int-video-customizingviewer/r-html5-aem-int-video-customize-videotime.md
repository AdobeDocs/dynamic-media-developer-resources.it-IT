---
title: Tempo video
description: La durata del video è il display numerico che mostra la durata e l’ora correnti del video attualmente in riproduzione.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: 90ec189e-6de4-44b3-8760-1e8636b919ba
source-git-commit: 6aaf4eccf51a05d200c6cc780e342be646d104d8
workflow-type: tm+mt
source-wordcount: '199'
ht-degree: 0%

---

# Tempo video{#video-time}

La durata del video è il display numerico che mostra la durata e l’ora correnti del video attualmente in riproduzione.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

La famiglia di font ora video, la dimensione e il colore del font sono tra le proprietà che CSS può controllare. Può anche essere posizionato, rispetto alla barra di controllo che lo contiene, da CSS.

L’aspetto del tempo del video è controllato dal seguente selettore di classe CSS:

```
.s7interactivevideoviewer .s7videotime
```

## Proprietà CSS del tempo video {#css-properties-of-video-time}

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> primi </span> </p> </td> 
   <td colname="col2"> <p>Posizione dal bordo superiore, inclusa la spaziatura. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> a destra </span> </p> </td> 
   <td colname="col2"> <p>Posizione dal bordo destro, inclusa la spaziatura. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> larghezza </span> </p> </td> 
   <td colname="col2"> <p> Larghezza del controllo tempo video. Questa proprietà è necessaria per il corretto funzionamento di Internet Explorer 8 o versione successiva. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> famiglia di caratteri </span> </p> </td> 
   <td colname="col2"> <p>Famiglia di font da utilizzare per il testo visualizzato nel tempo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size </span> </p> </td> 
   <td colname="col2"> <p>Dimensione font da utilizzare per il testo visualizzato nel tempo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> colore </span> </p> </td> 
   <td colname="col2"> <p>Colore del carattere da utilizzare per il testo visualizzato nel tempo. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Esempio {#section-e8caea0a303c425a8a637c2a47c06355}

Impostare il tempo video su grigio chiaro (esadecimale `#BBBBBB`), ridimensionato a 12 pixel, posizionato a 15 pixel dalla parte superiore della barra di controllo e a 80 pixel dai bordi superiore e destro della barra di controllo.

```
.s7interactivevideoviewer .s7videotime { 
top:15px; 
right:80px; 
font-size:12px; 
color:#BBBBBB; 
width:60px;  
}
```
