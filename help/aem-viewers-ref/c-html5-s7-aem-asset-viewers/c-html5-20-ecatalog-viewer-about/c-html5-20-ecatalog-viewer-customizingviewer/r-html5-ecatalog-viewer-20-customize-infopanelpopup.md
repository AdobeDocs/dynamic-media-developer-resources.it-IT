---
description: Quando un utente attiva una mappa immagine con una proprietà rollover_key definita in Dynamic Media Classic e se la funzione del pannello informazioni è configurata correttamente per il visualizzatore, viene visualizzato al centro dell’area del visualizzatore.
solution: Experience Manager
title: Popup pannello informazioni
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '468'
ht-degree: 1%

---


# Popup pannello informazioni{#info-panel-popup}

Quando un utente attiva una mappa immagine con una proprietà rollover_key definita in Dynamic Media Classic e se la funzione del pannello informazioni è configurata correttamente per il visualizzatore, viene visualizzato al centro dell’area del visualizzatore.

Lo sfondo del pannello Info copre l’intera area del visualizzatore ed è controllato con il seguente selettore di classe CSS:

`.s7ecatalogviewer .s7infopanelpopup .s7backoverlay`

<table id="table_94EE3F5BBE4547C0B4943471CEE7EDE4"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> Proprietà CSS </p> </th> 
   <th colname="col2" class="entry"> <p>Descrizione </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> immagine di sfondo  </span> </p> </td> 
   <td colname="col2"> <p>Riempimento di sfondo del pannello informazioni. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> posizione di sfondo  </span> </p> </td> 
   <td colname="col2"> <p> Posizione all’interno dello sprite di un’immagine, se vengono utilizzati gli spriti CSS. </p> <p>Vedi anche <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-customizingviewer/c-html5-20-ecatalog-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> Sprite CSS </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

Esempio: impostare la finestra a comparsa del pannello informazioni per utilizzare uno sfondo nero semitrasparente.

```
.s7ecatalogviewer .s7infopanelpopup .s7backoverlay { 
 background-color : rgba(0,0,0,0.75); 
}
```

La finestra di dialogo del pannello informazioni viene visualizzata per impostazione predefinita al centro dell’area del visualizzatore. Tuttavia è possibile controllarne le dimensioni, l’allineamento, lo sfondo e il bordo con il selettore di classe CSS.

`.s7ecatalogviewer .s7infopanelpopup .s7overlay`

<table id="table_4E666A03A3D44CEEA72225113553AB3F"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> Proprietà CSS </p> </th> 
   <th colname="col2" class="entry"> <p>Descrizione </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> sinistra  </span> </p> </td> 
   <td colname="col2"> <p>Posizione orizzontale della finestra di dialogo del pannello informazioni all’interno del riempimento di sfondo del pannello dell’area del visualizzatore. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> top  </span> </p> </td> 
   <td colname="col2"> <p>Posizione verticale della finestra di dialogo del pannello informazioni all’interno dell’area del visualizzatore. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Larghezza finestra di dialogo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Altezza finestra di dialogo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margine sinistro  </span> </p> </td> 
   <td colname="col2"> <p>Il margine sinistro della finestra di dialogo del pannello informazioni può essere utilizzato a scopo di centratura. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margine superiore  </span> </p> </td> 
   <td colname="col2"> <p>Il margine superiore della finestra di dialogo del pannello informazioni può essere utilizzato a scopo di centratura. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> spaziatura interna  </span> </p> </td> 
   <td colname="col2"> <p>Margine finestra di dialogo interno. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> colore di sfondo  </span> </p> </td> 
   <td colname="col2"> <p>Colore di sfondo della finestra di dialogo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> raggio bordo  </span> </p> </td> 
   <td colname="col2"> <p>Raggio del bordo della finestra di dialogo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ombra  </span> </p> </td> 
   <td colname="col2"> <p>Ombra finestra di dialogo. </p> </td> 
  </tr> 
 </tbody> 
</table>

Esempio: imposta la finestra di dialogo del pannello Info 300 x 200 pixel centrata nell’area del visualizzatore; ha una spaziatura di 40 pixel nella parte superiore e una spaziatura di 10 pixel su tutti gli altri lati, uno sfondo grigio chiaro, un raggio di 10 pixel per il bordo e un’ombra esterna.

```
.s7ecatalogviewer .s7infopanelpopup .s7overlay { 
 left: 50%; 
 top: 50%; 
 margin-left: -150px; 
 margin-top: -100px; 
 width: 300px; 
 height: 200px; 
 padding-top: 40px; 
 padding-right: 10px; 
 padding-bottom: 10px; 
 padding-left: 10px; 
 background-color:rgb(221,221,221); 
 border-radius: 10px 10px 10px 10px; 
box-shadow: 0 0 5px rgba(0,0,0,0.25);  
}
```

Nella finestra di dialogo Info Panel (Pannello Info) è presente un pulsante Chiudi e quando si tocca o fa clic sul pulsante viene chiusa la finestra di dialogo.

L’aspetto di questo pulsante è controllato con il seguente selettore di classe CSS:

`.s7ecatalogviewer .s7infopanelpopup .s7closebutton`

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
   <td colname="col2"> <p>Posizione dal bordo superiore della finestra di dialogo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> right  </span> </p> </td> 
   <td colname="col2"> <p>Posizione dal bordo destro della finestra di dialogo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> sinistra  </span> </p> </td> 
   <td colname="col2"> <p>Posizione dal bordo sinistro della finestra di dialogo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> bottom  </span> </p> </td> 
   <td colname="col2"> <p>Posizione dal bordo inferiore della finestra di dialogo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> larghezza  </span> </p> </td> 
   <td colname="col2"> <p>Larghezza pulsante. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> altezza  </span> </p> </td> 
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
>Questo pulsante supporta il selettore di attributi `state` , che può essere utilizzato per applicare interfacce diverse a diversi stati del pulsante.

La descrizione comando del pulsante può essere localizzata. Per ulteriori informazioni, consulta [Localizzazione degli elementi dell’interfaccia utente](../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) .

Esempio: per impostare un pulsante di chiusura della finestra di dialogo di 28 x 28 pixel, posizionato 5 pixel dal bordo superiore e destro della finestra di dialogo del pannello informazioni, e visualizza un’immagine diversa per ciascuno dei quattro stati del pulsante.

```
.s7ecatalogviewer .s7infopanelpopup .s7closebutton { 
 width: 28px; 
 height: 28px; 
 top: 5px; 
 right: 5px; 
} 
.s7ecatalogviewer .s7infopanelpopup .s7closebutton[state="up"] { 
background-image:url(images/v2/InfoPanelPopup_CloseButton_dark_up.png); 
} 
.s7ecatalogviewer .s7infopanelpopup .s7closebutton[state="over"] { 
background-image:url(images/v2/InfoPanelPopup_CloseButton_dark_over.png); 
} 
.s7ecatalogviewer .s7infopanelpopup .s7closebutton[state="down"] { 
background-image:url(images/v2/InfoPanelPopup_CloseButton_dark_up.png); 
} 
.s7ecatalogviewer .s7infopanelpopup .s7closebutton[state="disabled"] { 
background-image:url(images/v2/InfoPanelPopup_CloseButton_dark_up.png); 
}
```

