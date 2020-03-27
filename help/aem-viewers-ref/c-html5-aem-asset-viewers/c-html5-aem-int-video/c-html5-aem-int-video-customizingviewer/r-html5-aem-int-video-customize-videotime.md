---
description: L'ora video è la visualizzazione numerica che mostra l'ora e la durata correnti del video attualmente in riproduzione.
seo-description: L'ora video è la visualizzazione numerica che mostra l'ora e la durata correnti del video attualmente in riproduzione.
seo-title: Ora video
solution: Experience Manager
title: Ora video
topic: Dynamic media
uuid: 8cec89b9-b3e8-4c58-90d9-7ab56698e35d
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef

---


# Video time{#video-time}

L&#39;ora video è la visualizzazione numerica che mostra l&#39;ora e la durata correnti del video attualmente in riproduzione.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

La famiglia di font dell&#39;ora video, la dimensione del font e il colore del font sono tra le proprietà che CSS può controllare. Può anche essere posizionato, rispetto alla barra di controllo che lo contiene, tramite CSS.

L&#39;aspetto del tempo video è controllato dal seguente selettore di classe CSS:

```
.s7interactivevideoviewer .s7videotime
```

## Proprietà CSS del tempo video {#css-properties-of-video-time}

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> top </span> </p> </td> 
   <td colname="col2"> <p>Posizione dal bordo superiore, inclusa la spaziatura. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> right </span> </p> </td> 
   <td colname="col2"> <p>Posizione dal bordo destro, inclusa la spaziatura. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p> La larghezza del controllo del tempo video. Questa proprietà è necessaria per il corretto funzionamento di Internet Explorer 8 o versione successiva. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family </span> </p> </td> 
   <td colname="col2"> <p>Famiglia di font da utilizzare per il testo di visualizzazione dell'ora. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size </span> </p> </td> 
   <td colname="col2"> <p>La dimensione del font da utilizzare per il testo di visualizzazione dell'ora. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color </span> </p> </td> 
   <td colname="col2"> <p>Il colore del font da utilizzare per il testo di visualizzazione dell'ora. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Esempio {#section-e8caea0a303c425a8a637c2a47c06355}

Imposta il tempo video su grigio chiaro (esadecimale `#BBBBBB`), con dimensioni pari a 12 pixel, 15 pixel dalla parte superiore della barra di controllo e 80 pixel dai bordi superiore e destro della barra di controllo.

```
.s7interactivevideoviewer .s7videotime { 
top:15px; 
right:80px; 
font-size:12px; 
color:#BBBBBB; 
width:60px;  
}
```

