---
description: Fa sì che il visualizzatore entri o esca dalla modalità a schermo intero quando l’utente fa clic su di esso. Questo pulsante viene visualizzato nella barra di controllo principale. Questo pulsante non viene visualizzato se il visualizzatore funziona in modalità pop-up e il sistema non supporta lo schermo intero nativo. È possibile ridimensionare, applicare uno skin e posizionare il pulsante in modo CSS.
solution: Experience Manager
title: Pulsante Schermo intero
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '330'
ht-degree: 0%

---


# Pulsante a schermo intero{#full-screen-button}

Fa sì che il visualizzatore entri o esca dalla modalità a schermo intero quando l’utente fa clic su di esso. Questo pulsante viene visualizzato nella barra di controllo principale. Questo pulsante non viene visualizzato se il visualizzatore funziona in modalità pop-up e il sistema non supporta lo schermo intero nativo. È possibile ridimensionare, applicare uno skin e posizionare il pulsante in modo CSS.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**Proprietà CSS dell’area visualizzatore principale**

L’aspetto del pulsante è controllato con il seguente selettore di classe CSS:

`.s7ecatalogviewer .s7fullscreenbutton`

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
   <td colname="col2"> <p>Posizione dal bordo superiore della barra di controllo principale, compresa la spaziatura. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> right  </span> </p> </td> 
   <td colname="col2"> <p>Posizione dal bordo destro della barra di controllo principale, compresa la spaziatura. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> sinistra  </span> </p> </td> 
   <td colname="col2"> <p>Posizione dal bordo sinistro della barra di controllo principale, compresa la spaziatura. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> bottom  </span> </p> </td> 
   <td colname="col2"> <p>Posizione dal bordo inferiore della barra di controllo principale, compresa la spaziatura. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Larghezza del pulsante. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Altezza del pulsante. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> immagine di sfondo  </span> </p> </td> 
   <td colname="col2"> <p>Immagine visualizzata per un determinato stato del pulsante. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> posizione di sfondo  </span> </p> </td> 
   <td colname="col2"> <p> Posizione all’interno dello sprite di un’immagine, se vengono utilizzati gli spriti CSS. </p> <p>Vedi anche <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-customizingviewer/c-html5-20-ecatalog-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> Sprite CSS </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Questo pulsante supporta sia i selettori di attributi `state` che `selected` , che possono essere utilizzati per applicare interfacce diverse a diversi stati dei pulsanti. In particolare, `selected='true'` corrisponde allo stato &quot;a schermo intero&quot; e `selected='false'` corrisponde allo stato &quot;normale&quot;.

La descrizione comando del pulsante può essere localizzata. Per ulteriori informazioni, consulta [Localizzazione degli elementi dell’interfaccia utente](../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) .

Esempio: per impostare un pulsante a schermo intero di 28 x 28 pixel, posizionato 4 pixel dal fondo e 5 pixel dal bordo destro della barra di controllo principale, e visualizza un’immagine diversa per ciascuno dei quattro stati del pulsante, se selezionato o meno.

```
.s7ecatalogviewer .s7fullscreenbutton { 
bottom:4px; 
right:5px; 
width:28px; 
height:28px; 
} 
.s7ecatalogviewer .s7fullscreenbutton [selected='false'][state='up'] { 
background-image:url(images/enterFullBtn_up.png); 
} 
.s7ecatalogviewer .s7fullscreenbutton [selected='false'][state='over'] {  
background-image:url(images/enterFullBtn_over.png); 
} 
.s7ecatalogviewer .s7fullscreenbutton [selected='false'][state='down'] {  
background-image:url(images/enterFullBtn_down.png); 
} 
.s7ecatalogviewer .s7fullscreenbutton [selected='false'][state='disabled'] { 
background-image:url(images/enterFullBtn_disabled.png); 
} 
.s7ecatalogviewer .s7fullscreenbutton [selected='true'][state='up'] {  
background-image:url(images/exitFullBtn_up.png); 
} 
.s7ecatalogviewer .s7fullscreenbutton [selected='true'][state='over'] {  
background-image:url(images/exitFullBtn_over.png); 
} 
.s7ecatalogviewer .s7fullscreenbutton [selected='true'][state='down'] {  
background-image:url(images/exitFullBtn_down.png); 
} 
.s7ecatalogviewer .s7fullscreenbutton [selected='true'][state='disabled'] {  
background-image:url(images/exitFullBtn_disabled.png); } 
}
```

