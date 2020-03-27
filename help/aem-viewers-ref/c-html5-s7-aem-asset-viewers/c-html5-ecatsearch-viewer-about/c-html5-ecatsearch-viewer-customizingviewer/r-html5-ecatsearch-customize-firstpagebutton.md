---
description: Toccando o facendo clic su questo pulsante l’utente passa alla prima pagina del catalogo. Questo pulsante viene visualizzato nella barra di controllo principale sui sistemi desktop e sui tablet; sui telefoni cellulari viene aggiunto a una barra di controllo secondaria. Questo pulsante può essere ridimensionato, incarnato e posizionato mediante CSS.
seo-description: Toccando o facendo clic su questo pulsante l’utente passa alla prima pagina del catalogo. Questo pulsante viene visualizzato nella barra di controllo principale sui sistemi desktop e sui tablet; sui telefoni cellulari viene aggiunto a una barra di controllo secondaria. Questo pulsante può essere ridimensionato, incarnato e posizionato mediante CSS.
seo-title: Pulsante Prima pagina
solution: Experience Manager
title: Pulsante Prima pagina
topic: Dynamic media
uuid: 10097f10-d53b-409c-baad-d21a04d6b418
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef

---


# Pulsante Prima pagina{#first-page-button}

Toccando o facendo clic su questo pulsante l’utente passa alla prima pagina del catalogo. Questo pulsante viene visualizzato nella barra di controllo principale sui sistemi desktop e sui tablet; sui telefoni cellulari viene aggiunto a una barra di controllo secondaria. Questo pulsante può essere ridimensionato, incarnato e posizionato mediante CSS.

<!--<a id="section_6C008EE11212461FA744F2540D38C295"></a>-->

**Proprietà CSS dell&#39;area visualizzatore principale**

L&#39;aspetto del pulsante è controllato dal seguente selettore di classe CSS:

`.s7ecatalogsearchviewer .s7firstpagebutton .s7panleftbutton`

<table id="table_94EE3F5BBE4547C0B4943471CEE7EDE4"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> Proprietà CSS </p> </th> 
   <th colname="col2" class="entry"> <p>Descrizione </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> top </span> </p> </td> 
   <td colname="col2"> <p>Posizione dal bordo superiore della barra di controllo principale (sui sistemi desktop e sui tablet) o dalla barra di controllo secondaria (sui telefoni cellulari), compresa la spaziatura. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> right </span> </p> </td> 
   <td colname="col2"> <p>Posizione dal bordo destro della barra di controllo principale (sui sistemi desktop e sui tablet) o della barra di controllo secondaria (sui telefoni cellulari), compresa la spaziatura. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> left </span> </p> </td> 
   <td colname="col2"> <p>Posizione dal bordo sinistro della barra di controllo principale (sui sistemi desktop e sui tablet) o della barra di controllo secondaria (sui telefoni cellulari), compresa la spaziatura. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> bottom </span> </p> </td> 
   <td colname="col2"> <p>Posizione dal bordo inferiore della barra di controllo principale (sui sistemi desktop e sui tablet) o della barra di controllo secondaria (sui telefoni cellulari), compresa la spaziatura. </p> </td> 
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
   <td colname="col1"> <p> <span class="codeph"> background-image </span> </p> </td> 
   <td colname="col2"> <p>Immagine visualizzata per un determinato stato del pulsante. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> Posizionare all'interno dello sprite della grafica, se vengono utilizzati gli spriti CSS. </p> <p>Consultate anche <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-customizingviewer/c-html5-ecatsearch-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> CSS Sprite </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Questo pulsante supporta il selettore `state` di attributi, che può essere utilizzato per applicare interfacce diverse a stati di pulsante diversi.

La descrizione del pulsante può essere localizzata. Per ulteriori informazioni, consultate [Localizzazione degli elementi](../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) dell&#39;interfaccia utente.

Esempio: per impostare un pulsante per la prima pagina di 28 x 28 pixel, posizionato 4 pixel dal basso e 220 pixel dal bordo sinistro della barra di controllo principale, e visualizza un’immagine diversa per ciascuno dei quattro stati del pulsante.

```
.s7ecatalogsearchviewer .s7firstpagebutton .s7panleftbutton { 
bottom:4px; 
left:220px; 
width:32px; 
height:32px; 
} 
.s7ecatalogsearchviewer .s7firstpagebutton .s7panleftbutton [state='up'] { 
background-image:url(images/v2/FirstPageButton_dark_up.png); 
} 
.s7ecatalogsearchviewer .s7firstpagebutton .s7panleftbutton [state='over'] {  
background-image:url(images/v2/FirstPageButton_dark_over.png); 
} 
.s7ecatalogsearchviewer .s7firstpagebutton .s7panleftbutton [state='down'] {  
background-image:url(images/v2/FirstPageButton_dark_down.png); 
} 
.s7ecatalogsearchviewer .s7firstpagebutton .s7panleftbutton [state='disabled'] { 
background-image:url(images/v2/FirstPageButton_dark_disabled.png); 
}
```

