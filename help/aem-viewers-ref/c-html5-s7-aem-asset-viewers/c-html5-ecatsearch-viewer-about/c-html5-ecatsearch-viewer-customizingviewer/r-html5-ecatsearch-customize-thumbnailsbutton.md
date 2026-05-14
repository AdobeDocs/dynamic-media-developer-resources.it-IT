---
title: Pulsante Miniature
description: Se si seleziona questo pulsante, il visualizzatore viene reimpostato alternando la visualizzazione principale alle miniature. Questo pulsante viene visualizzato nella barra di controllo principale. Puoi ridimensionare, applicare lo skin e posizionare questo pulsante utilizzando gli stili CSS.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: 465d4320-14ea-4f07-97c0-41f53034a7df
TQID: 'https://experienceleague.adobe.com/AW3lnolX7gPbB7uDywu6Ne0t0cf1kkr1jynYupUeZPY'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 278
ht-degree: 0%

---

# Pulsante Miniature{#thumbnails-button}

Se si seleziona questo pulsante, il visualizzatore viene reimpostato alternando la visualizzazione principale alle miniature. Questo pulsante viene visualizzato nella barra di controllo principale. Puoi ridimensionare, applicare lo skin e posizionare questo pulsante utilizzando gli stili CSS.

<!--<a id="section_6C008EE11212461FA744F2540D38C295"></a>-->

**Proprietà CSS dell&#39;area visualizzatore principale**

L’aspetto del pulsante è controllato dal seguente selettore di classe CSS:

`.s7ecatalogsearchviewer .s7thumbnailpagebutton`

<table id="table_94EE3F5BBE4547C0B4943471CEE7EDE4"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> Proprietà CSS </p> </th> 
   <th colname="col2" class="entry"> <p>Descrizione </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margine superiore </span> </p> </td> 
   <td colname="col2"> <p> Offset dalla parte superiore della barra di controllo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margine sinistro </span> </p> </td> 
   <td colname="col2"> <p> Distanza dal pulsante successivo a sinistra o dal lato sinistro della barra di controllo se questo pulsante è il primo di una riga. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> larghezza </span> </p> </td> 
   <td colname="col2"> <p>Larghezza del pulsante. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> altezza </span> </p> </td> 
   <td colname="col2"> <p>Altezza del pulsante. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> immagine di sfondo </span> </p> </td> 
   <td colname="col2"> <p>Immagine visualizzata per un determinato stato del pulsante. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> Posizionate all'interno dello sprite del disegno, se vengono utilizzati gli sprite CSS. </p> <p>Vedere anche <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-customizingviewer/c-html5-ecatsearch-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> sprite CSS </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Questo pulsante supporta sia i selettori di attributi `state` che `selected`, che possono essere utilizzati per applicare interfacce diverse a stati di pulsante diversi. In particolare, `selected='true'` corrisponde allo stato del visualizzatore quando la modalità miniatura è attiva e `selected='false'` corrisponde allo stato predefinito con la visualizzazione principale.

La descrizione comando del pulsante può essere localizzata. Per ulteriori informazioni, vedere [Localizzazione degli elementi dell&#39;interfaccia utente](../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74).

Esempio: per impostare un pulsante delle miniature di 28 x 28 pixel posizionato a 4 pixel dal basso e a 5 pixel dal bordo sinistro della barra di controllo principale. Infine, visualizza un&#39;immagine diversa per ciascuno dei quattro diversi stati del pulsante, se selezionato o meno.

```
.s7ecatalogsearchviewer .s7thumbnailpagebutton{ 
margin-top: 4px; 
margin-left: 5px; width:28px; 
 height:28px; 
} 
.s7ecatalogsearchviewer .s7thumbnailpagebutton [selected='false'][state='up'] { 
background-image:url(images/v2/ThumbnailPageButton_dark_up.png); 
} 
.s7ecatalogsearchviewer .s7thumbnailpagebutton [selected='false'][state='over'] { 
background-image:url(images/v2/ThumbnailPageButton_dark_over.png); 
} 
.s7ecatalogsearchviewer .s7thumbnailpagebutton [selected='false'][state='down'] { 
background-image:url(images/v2/ThumbnailPageButton_dark_down.png); 
} 
.s7ecatalogsearchviewer .s7thumbnailpagebutton [selected='false'][state='disabled'] { 
background-image:url(images/v2/ThumbnailPageButton_dark_disabled.png); 
} 
.s7ecatalogsearchviewer .s7thumbnailpagebutton [selected='true'][state='up'] { 
background-image:url(images/v2/ThumbnailPageButton_dark_over.png); 
} 
.s7ecatalogsearchviewer .s7thumbnailpagebutton [selected='true'][state='over'] { 
background-image:url(images/v2/ThumbnailPageButton_dark_over.png); 
} 
.s7ecatalogsearchviewer .s7thumbnailpagebutton [selected='true'][state='down'] { 
background-image:url(images/v2/ThumbnailPageButton_dark_over.png); 
} 
.s7ecatalogsearchviewer .s7thumbnailpagebutton [selected='true'][state='disabled'] { 
background-image:url(images/v2/ThumbnailPageButton_dark_disabled.png); 
}
```
