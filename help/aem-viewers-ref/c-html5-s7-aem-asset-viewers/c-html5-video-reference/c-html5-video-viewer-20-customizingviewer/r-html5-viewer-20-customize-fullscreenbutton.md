---
title: pulsante a schermo intero
description: La pulsante a schermo intero fa sì che il lettore video entri o esca dalla modalità a schermo intero quando un utente fa clic su di esso.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Video
role: Developer,User
exl-id: 120f0ee9-e76b-48d5-8ea7-8be5a8f52edc
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '240'
ht-degree: 0%

---

# pulsante a schermo intero{#full-screen-button}

La pulsante a schermo intero fa sì che il lettore video entri o esca dalla modalità a schermo intero quando un utente lo seleziona.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

È possibile ridimensionare, interfacciare e posizionare l&#39;pulsante a schermo intero, rispetto alla barra di controllo che lo contiene, in base ai CSS.

L&#39;aspetto del pulsante a schermo intero è controllato con il selettore della classe CSS:

```
.s7videoviewer .s7fullscreenbutton
```

**Proprietà CSS dell&#39;pulsante a schermo intero**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> In alto </span> </p> </td> 
   <td colname="col2"> <p> Posizione dall'alto bordo, compresa la spaziatura. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> A destra </span> </p> </td> 
   <td colname="col2"> <p> Posizione dal bordo destro, compresa l'imbottitura. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> A sinistra </span> </p> </td> 
   <td colname="col2"> <p> Posizione dal bordo sinistro, compresa l'imbottitura. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Fondoschiena </span> </p> </td> 
   <td colname="col2"> <p>Posizione dal basso bordo, compresa l'imbottitura. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Larghezza </span> </p> </td> 
   <td colname="col2"> <p> Larghezza dello schermo intero pulsante. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> altezza </span> </p> </td> 
   <td colname="col2"> <p>Altezza dello schermo intero pulsante. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> immagine di sfondo </span> </p> </td> 
   <td colname="col2"> <p> Immagine visualizzata per uno stato pulsante specificato. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> posizione sfondo </span> </p> </td> 
   <td colname="col2"> <p> Posizione all'interno dello sprite dell'illustrazione, se vengono utilizzati sprite CSS. </p> <p>Vedere <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-customizingviewer/c-html5-video-viewer-20-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> CSS Sprite </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Questo pulsante supporta sia i selettori di attributi `state` che `selected` quelli che possono essere utilizzati per applicare interfacce diverse a diversi stati di pulsante. In particolare, `selected='true'` corrisponde allo stato &quot;schermo intero&quot; e `selected='false'` corrisponde allo stato &quot;normale&quot;.

Il suggerimento strumento pulsante può essere localizzato. Per ulteriori informazioni, consulta [Localizzazione di utente elementi](../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/r-html5-video-viewer-20-localization.md#concept-1d5ca2d8480f4064a51eddba13940aad) dell&#39;interfaccia.

## Esempio {#section-e8caea0a303c425a8a637c2a47c06355}

Per impostare un pulsante a schermo intero di 32 x 32 pixel e posizionato a 6 pixel dal bordo superiore e destro della barra di controllo. Inoltre, quando è selezionata o non selezionata, viene visualizzata un&#39;immagine diversa per ciascuno dei quattro diversi stati pulsante.

```
.s7videoviewer . s7fullscreenbutton { 
top:6px; 
right:6px; 
width:32px; 
height:32px; 
} 
.s7videoviewer .s7fullscreenbutton [selected='false'][state='up'] { 
background-image:url(images/enterFullBtn_up.png); 
} 
.s7videoviewer .s7fullscreenbutton [selected='false'][state='over'] {  
background-image:url(images/enterFullBtn_over.png); 
} 
.s7videoviewer .s7fullscreenbutton [selected='false'][state='down'] {  
background-image:url(images/enterFullBtn_down.png); 
} 
.s7videoviewer .s7fullscreenbutton [selected='false'][state='disabled'] { 
background-image:url(images/enterFullBtn_disabled.png); 
} 
.s7videoviewer .s7fullscreenbutton [selected='true'][state='up'] {  
background-image:url(images/exitFullBtn_up.png); 
} 
.s7videoviewer .s7fullscreenbutton [selected='true'][state='over'] {  
background-image:url(images/exitFullBtn_over.png); 
} 
.s7videoviewer .s7fullscreenbutton [selected='true'][state='down'] {  
background-image:url(images/exitFullBtn_down.png); 
} 
.s7videoviewer .s7fullscreenbutton [selected='true'][state='disabled'] {  
background-image:url(images/exitFullBtn_disabled.png); } 
}
```
