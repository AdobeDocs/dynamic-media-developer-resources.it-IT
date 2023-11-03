---
title: Condivisione e-mail
description: Lo strumento Condivisione e-mail è costituito da un pulsante aggiunto al pannello Condivisione e dalla finestra di dialogo modale che viene visualizzata quando lo strumento viene attivato. La posizione del pulsante è completamente gestita dallo strumento Condivisione social.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: 4c72500b-9750-4fae-9447-96cf600b31c7
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '3045'
ht-degree: 1%

---

# Condivisione e-mail{#email-share}

Lo strumento Condivisione e-mail è costituito da un pulsante aggiunto al pannello Condivisione e dalla finestra di dialogo modale che viene visualizzata quando lo strumento viene attivato. La posizione del pulsante è completamente gestita dallo strumento Condivisione social.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

L’aspetto del pulsante di condivisione e-mail è controllato dal seguente selettore di classe CSS:

```
.s7ecatalogviewer .s7emailshare
```

**Proprietà CSS dello strumento condivisione e-mail**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
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
   <td colname="col2"> <p> Immagine visualizzata per un determinato stato del pulsante. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> Posizionate all'interno dello sprite del disegno, se vengono utilizzati gli sprite CSS. </p> <p>Vedi anche <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-customizingviewer/c-html5-20-ecatalog-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> Spunti CSS </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Questo pulsante supporta `state` selettore di attributi, che può essere utilizzato per applicare interfacce diverse a stati di pulsante diversi.

È possibile rimuovere il pulsante dal pannello Condivisione social impostando `display:none` proprietà CSS nella relativa classe CSS.

La descrizione comando del pulsante può essere localizzata. Consulta [Localizzazione degli elementi dell’interfaccia utente](../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) per ulteriori informazioni.

Esempio: per impostare un pulsante di condivisione e-mail di 28 x 28 pixel e visualizzare un’immagine diversa per ciascuno dei quattro diversi stati del pulsante.

```
.s7ecatalogviewer .s7emailshare { 
 width:28px; 
 height:28px; 
} 
.s7ecatalogviewer .s7emailshare[state='up'] { 
background-image:url(images/v2/EmailShare_dark_up.png); 
} 
.s7ecatalogviewer .s7emailshare[state='over'] { 
background-image:url(images/v2/EmailShare_dark_over.png); 
} 
.s7ecatalogviewer .s7emailshare[state='down'] { 
background-image:url(images/v2/EmailShare_dark_down.png); 
} 
.s7ecatalogviewer .s7emailshare[state='disabled'] { 
background-image:url(images/v2/EmailShare_dark_disabled.png); 
}
```

La sovrapposizione di sfondo che copre la pagina web quando la finestra di dialogo è attiva è controllata dal seguente selettore di classe CSS:

```
.s7ecatalogviewer .s7emaildialog .s7backoverlay
```

**Proprietà CSS della sovrapposizione posteriore**

<table id="table_1A0C28D8C81D413C83D73DEAC53057C5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> opacità </span> </p> </td> 
   <td colname="col2"> <p> Opacità sovrapposizione sfondo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p>Colore di sovrapposizione sfondo. </p> </td> 
  </tr> 
 </tbody> 
</table>

Esempio: per impostare la sovrapposizione di sfondo su grigio con opacità 70%:

```
.s7ecatalogviewer .s7emaildialog .s7backoverlay { 
 opacity:0.7; 
 background-color:#222222; 
}
```

Per impostazione predefinita, la finestra di dialogo modale viene visualizzata centrata sullo schermo dei sistemi desktop e occupa l’intera area della pagina web sui dispositivi touch. In tutti i casi, il posizionamento e il ridimensionamento della finestra di dialogo vengono gestiti dal componente. La finestra di dialogo è controllata con il seguente selettore di classe CSS:

```
.s7ecatalogviewer .s7emaildialog .s7dialog
```

**Proprietà CSS della finestra di dialogo**

<table id="table_5272BC8EF9124018B4290356B95B5559"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> border-radius </span> </p> </td> 
   <td colname="col2"> <p> Raggio del bordo della finestra di dialogo (se la finestra di dialogo non occupa l'intera finestra del browser); </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p> Colore di sfondo della finestra di dialogo; </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p> Deve essere disattivato o impostato su 100%, nel qual caso la finestra di dialogo occupa l’intera finestra del browser (questa modalità è preferita sui dispositivi touch); </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p> Deve essere disattivato o impostato su 100%, nel qual caso la finestra di dialogo occupa l’intera finestra del browser (questa modalità è preferita sui dispositivi touch). </p> </td> 
  </tr> 
 </tbody> 
</table>

Esempio: per impostare la finestra di dialogo in modo da utilizzare l’intera finestra del browser e avere uno sfondo bianco sui dispositivi touch:

```
.s7ecatalogviewer .s7touchinput .s7emaildialog .s7dialog { 
 width:100%; 
 height:100%; 
background-color: #ffffff; 
}
```

L&#39;intestazione della finestra di dialogo è costituita da un&#39;icona, un testo del titolo e un pulsante Chiudi. Il contenitore di intestazione è controllato con il seguente selettore di classe CSS

```
.s7ecatalogviewer .s7emaildialog .s7dialogheader
```

**Proprietà CSS dell’intestazione della finestra di dialogo**

<table id="table_E407E844C9BD4B5DA8B5BBDE0554F9CA"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> riempimento </span> </p> </td> 
   <td colname="col2"> <p> Spaziatura interna per contenuto intestazione. </p> </td> 
  </tr> 
 </tbody> 
</table>

L’icona e il testo del titolo vengono racchiusi in un contenitore aggiuntivo controllato da

```
.s7ecatalogviewer .s7emaildialog .s7dialogheader .s7dialogline
```

**Proprietà CSS della riga di dialogo**

<table id="table_5B03CF843F0D4B1295A3FC1EB50C56F1"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> riempimento </span> </p> </td> 
   <td colname="col2"> <p> Spaziatura interna per l’icona e il titolo dell’intestazione. </p> </td> 
  </tr> 
 </tbody> 
</table>

L’icona dell’intestazione è controllata dal seguente selettore di classe CSS:

```
.s7ecatalogviewer .s7emaildialog .s7dialogheadericon
```

**Proprietà CSS dell&#39;icona dell&#39;intestazione della finestra di dialogo**

<table id="table_DD4B0413721B49CE8E21B4A55BDE8F7D"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Larghezza icona. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Altezza icona. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image </span> </p> </td> 
   <td colname="col2"> <p>Immagine icona. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> Posizionate all'interno dello sprite del disegno, se vengono utilizzati gli sprite CSS. </p> <p>Vedi anche <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-customizingviewer/c-html5-20-ecatalog-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> Spunti CSS </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

Il titolo dell’intestazione è controllato dal seguente selettore di classe CSS:

```
.s7ecatalogviewer .s7emaildialog .s7dialogheadertext
```

**Proprietà CSS del testo dell’intestazione della finestra di dialogo**

<table id="table_207B4B13153E425EAB38FC61F382A05F"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-weight </span> </p> </td> 
   <td colname="col2"> <p>Spessore font. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size </span> </p> </td> 
   <td colname="col2"> <p>Altezza carattere. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family </span> </p> </td> 
   <td colname="col2"> <p>Famiglia di caratteri. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> riempimento </span> </p> </td> 
   <td colname="col2"> <p>Spaziatura interna testo. </p> </td> 
  </tr> 
 </tbody> 
</table>

Il pulsante Chiudi è controllato dal seguente selettore di classe CSS:

```
.s7ecatalogviewer .s7emaildialog .s7closebutton
```

**Proprietà CSS del ** del pulsante Chiudi

<table id="table_FAECBC489FC442588E50E3DA0AC16DD7"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> top </span> </p> </td> 
   <td colname="col2"> <p> Posizione verticale del pulsante rispetto al contenitore di intestazione. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> destra </span> </p> </td> 
   <td colname="col2"> <p> Posizione del pulsante orizzontale relativa al contenitore di intestazione. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Larghezza pulsante. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Altezza pulsante. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> riempimento </span> </p> </td> 
   <td colname="col2"> <p>Spaziatura interna del pulsante. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image </span> </p> </td> 
   <td colname="col2"> <p>Immagine pulsante per ogni stato. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> Posizionate all'interno dello sprite del disegno, se vengono utilizzati gli sprite CSS. </p> <p>Vedi anche <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-customizingviewer/c-html5-20-ecatalog-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> Spunti CSS </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Questo pulsante supporta `state` selettore di attributi, che può essere utilizzato per applicare interfacce diverse a stati di pulsante diversi.

È possibile localizzare la descrizione comando del pulsante Chiudi e il titolo della finestra di dialogo. Consulta [Localizzazione degli elementi dell’interfaccia utente](../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) per ulteriori informazioni.

Esempio: per impostare l&#39;intestazione della finestra di dialogo con spaziatura interna, l&#39;icona 24 x 17 pixel e il titolo in grassetto a 16 punti. Infine, un pulsante Chiudi di 28 x 28 pixel posizionato due pixel dalla parte superiore e due pixel dalla parte destra del contenitore della finestra di dialogo:

```
.s7ecatalogviewer .s7emaildialog .s7dialogheader { 
 padding: 10px; 
} 
.s7ecatalogviewer .s7emaildialog .s7dialogheader .s7dialogline { 
 padding: 10px 10px 2px; 
} 
.s7ecatalogviewer .s7emaildialog .s7dialogheadericon { 
    background-image: url("images/sdk/dlgemail_cap.png"); 
    height: 17px; 
    width: 24px; 
} 
.s7ecatalogviewer .s7emaildialog .s7dialogheadertext { 
    font-size: 16pt; 
    font-weight: bold; 
    padding-left: 16px; 
} 
.s7ecatalogviewer .s7emaildialog .s7closebutton { 
 top:2px; 
 right:2px; 
 padding:8px; 
 width:28px; 
 height:28px; 
} 
.s7ecatalogviewer .s7emaildialog .s7closebutton[state='up'] { 
 background-image:url(images/sdk/close_up.png); 
} 
.s7ecatalogviewer .s7emaildialog .s7closebutton[state='over'] { 
 background-image:url(images/sdk/close_over.png); 
} 
.s7ecatalogviewer .s7emaildialog .s7closebutton[state='down'] { 
 background-image:url(images/sdk/close_down.png); 
} 
.s7ecatalogviewer .s7emaildialog .s7closebutton[state='disabled'] { 
 background-image:url(images/sdk/close_disabled.png); 
}
```

Il piè di pagina della finestra di dialogo è costituito dai pulsanti Annulla e Invia e-mail. Il contenitore piè di pagina è controllato dal seguente selettore di classe CSS:

```
.s7ecatalogviewer .s7emaildialog .s7dialogfooter
```

**Proprietà CSS del ** piè di pagina della finestra di dialogo

<table id="table_0AF7AAAB846A46D690896AFD68575669"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> bordo </span> </p> </td> 
   <td colname="col2"> <p> Bordo che consente di separare visivamente il piè di pagina dal resto della finestra di dialogo. </p> </td> 
  </tr> 
 </tbody> 
</table>

Il piè di pagina contiene un contenitore interno che contiene entrambi i pulsanti. Viene controllata con il seguente selettore di classe CSS:

```
.s7ecatalogviewer .s7emaildialog .s7dialogbuttoncontainer
```

**Proprietà CSS del contenitore del pulsante della finestra di dialogo**

<table id="table_C34906888A8145C7A61E503DFC6B08A9"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> riempimento </span> </p> </td> 
   <td colname="col2"> <p> Spaziatura interna tra piè di pagina e pulsanti. </p> </td> 
  </tr> 
 </tbody> 
</table>

Il pulsante Annulla è controllato dal seguente selettore di classe CSS:

```
.s7ecatalogviewer .s7emaildialog .s7dialogcancelbutton
```

**Proprietà CSS del pulsante Annulla della finestra di dialogo**

<table id="table_3DFA90B012F345A3A2A123D6856BE08A"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Larghezza pulsante. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Altezza pulsante. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color </span> </p> </td> 
   <td colname="col2"> <p> Colore testo pulsante per ogni stato. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p> Colore di sfondo pulsante per ogni stato. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Questo pulsante supporta `state` selettore di attributi, che può essere utilizzato per applicare interfacce diverse a stati di pulsante diversi.

Il pulsante Invia e-mail è controllato dal seguente selettore di classe CSS:

```
.s7ecatalogviewer .s7emaildialog .s7dialogactionbutton
```

**Proprietà CSS del pulsante di azione della finestra di dialogo**

<table id="table_91C75B2470A24DC2AD3973A91FA8B325"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Larghezza pulsante. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Altezza pulsante. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color </span> </p> </td> 
   <td colname="col2"> <p> Colore testo pulsante per ogni stato. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p> Colore di sfondo pulsante per ogni stato. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Questo pulsante supporta `state` selettore di attributi, che può essere utilizzato per applicare interfacce diverse a stati di pulsante diversi.

Inoltre, entrambi i pulsanti condividono la stessa classe CSS che può contenere impostazioni CSS identiche a quelle degli altri pulsanti della finestra di dialogo:

```
.s7ecatalogviewer .s7emaildialog .s7dialogfooter .s7button
```

**Proprietà CSS del pulsante**

<table id="table_E735E5EDFC1E4F8A962CEA533A88DD4E"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-weight </span> </p> </td> 
   <td colname="col2"> <p>Spessore font pulsante. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size </span> </p> </td> 
   <td colname="col2"> <p>Dimensione font pulsante. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family </span> </p> </td> 
   <td colname="col2"> <p>Famiglia font pulsante. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> line-height </span> </p> </td> 
   <td colname="col2"> <p> Altezza del testo all'interno del pulsante. Influisce sull'allineamento verticale. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> box-shadow </span> </p> </td> 
   <td colname="col2"> <p>Ombra esterna. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margine destro </span> </p> </td> 
   <td colname="col2"> <p>Margine pulsante destro. </p> </td> 
  </tr> 
 </tbody> 
</table>

Le descrizioni comandi di questo pulsante possono essere localizzate. Consulta [Localizzazione degli elementi dell’interfaccia utente](../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) per ulteriori informazioni.

Esempio: per impostare un piè di pagina della finestra di dialogo con il pulsante Annulla 64 x 34 e il pulsante Invia e-mail 82 x 34. Il colore del testo e il colore di sfondo sono diversi per ogni stato del pulsante:

```
.s7ecatalogviewer .s7emaildialog .s7dialogfooter { 
    border-top: 1px solid #909090; 
} 
.s7ecatalogviewer .s7emaildialog .s7dialogbuttoncontainer { 
    padding-bottom: 6px; 
    padding-top: 10px; 
} 
.s7ecatalogviewer .s7emaildialog .s7dialogfooter .s7button { 
    box-shadow: 1px 1px 1px #999999; 
    color: #FFFFFF; 
    font-size: 9pt; 
    font-weight: bold; 
    line-height: 34px; 
    margin-right: 10px; 
} 
.s7ecatalogviewer .s7emaildialog .s7dialogcancelbutton { 
 width:64px; 
 height:34px; 
} 
.s7ecatalogviewer .s7emaildialog .s7dialogcancelbutton[state='up'] { 
 background-color:#666666; 
 color:#dddddd; 
} 
.s7ecatalogviewer .s7emaildialog .s7dialogcancelbutton[state='down'] { 
 background-color:#555555; 
 color:#ffffff; 
} 
.s7ecatalogviewer .s7emaildialog .s7dialogcancelbutton[state='over'] { 
 background-color:#555555; 
 color:#ffffff; 
} 
.s7ecatalogviewer .s7emaildialog .s7dialogcancelbutton[state='disabled'] { 
 background-color:#b2b2b2; 
 color:#dddddd; 
} 
.s7ecatalogviewer .s7emaildialog .s7dialogactionbutton { 
 width:82px; 
 height:34px; 
} 
.s7ecatalogviewer .s7emaildialog .s7dialogactionbutton[state='up'] { 
 background-color:#333333; 
 color:#dddddd; 
} 
.s7ecatalogviewer .s7emaildialog .s7dialogactionbutton[state='down'] { 
 background-color:#222222; 
 color:#cccccc; 
} 
.s7ecatalogviewer .s7emaildialog .s7dialogactionbutton[state='over'] { 
 background-color:#222222; 
 color:#cccccc; 
} 
.s7ecatalogviewer .s7emaildialog .s7dialogactionbutton[state='disabled'] { 
 background-color:#b2b2b2; 
 color:#dddddd; 
}
```

L’area della finestra di dialogo principale (tra l’intestazione e il piè di pagina) contiene il contenuto della finestra di dialogo e il pannello di scorrimento a destra. In tutti i casi in cui il componente gestisce la larghezza di quest’area, non è possibile impostarla in CSS. L’area della finestra di dialogo principale è controllata dal seguente selettore di classe CSS:

```
.s7ecatalogviewer .s7emaildialog .s7dialogviewarea
```

**Proprietà CSS della finestra di dialogo ** area di visualizzazione

<table id="table_3FF4691D848A4C4D8EF060B7E79DEEDE"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p> Altezza della finestra di dialogo principale. Deve essere specificato solo quando la finestra di dialogo funziona in modalità desktop. Non è applicabile quando la finestra di dialogo viene ridimensionata per occupare l'intera finestra del browser. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p>Colore di sfondo dell'area della finestra di dialogo principale. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margine </span> </p> </td> 
   <td colname="col2"> <p>Margine esterno. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>L&#39;area della finestra di dialogo principale supporta l&#39;opzione `state` selettore di attributi. È impostato su `sendsuccess` quando il modulo e-mail viene inviato e nella finestra di dialogo viene visualizzato un messaggio di conferma. Se il messaggio di conferma è piccolo, questo selettore di attributi può essere utilizzato per ridurre l’altezza della finestra di dialogo quando viene visualizzato tale messaggio di conferma.

Esempio: per impostare l&#39;area della finestra di dialogo principale su un&#39;altezza iniziale di 300 pixel e su un&#39;altezza di 100 pixel quando viene visualizzato il messaggio di conferma, impostate un margine di dieci pixel e utilizzate uno sfondo bianco:

```
.s7ecatalogviewer .s7emaildialog .s7dialogviewarea { 
 background-color:#ffffff; 
 margin:10px; 
 height:300px; 
} 
.s7ecatalogviewer .s7emaildialog .s7dialogviewarea[state='sendsuccess'] { 
 height:100px; 
}
```

Tutto il contenuto del modulo (come etichette e campi di input) si trova all’interno di un contenitore controllato con il seguente selettore di classe CSS:

```
.s7ecatalogviewer .s7emaildialog .s7dialogbody
```

Se l’altezza del contenitore risulta maggiore dell’area della finestra di dialogo principale, il componente abilita automaticamente uno scorrimento verticale.

**Proprietà CSS del ** del corpo della finestra di dialogo

<table id="table_5D77F3D5B8CD4B798AA85F722B277F56"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> riempimento </span> </p> </td> 
   <td colname="col2"> <p>Spaziatura interna. </p> </td> 
  </tr> 
 </tbody> 
</table>

Esempio: per impostare il contenuto del modulo su una spaziatura di dieci pixel:

```
.s7ecatalogviewer .s7emaildialog .s7dialogbody { 
    padding: 10px; 
}
```

Il modulo della finestra di dialogo viene compilato riga per riga, dove ogni riga contiene una parte del contenuto del modulo, ad esempio un&#39;etichetta e un campo di immissione testo. Una singola riga di modulo è controllata con il seguente selettore di classe CSS:

```
.s7ecatalogviewer .s7emaildialog .s7dialogbody .s7dialogline
```

**Proprietà CSS della riga della finestra di dialogo**

<table id="table_2CCCC71B45B444A8B9CE2894129C9C02"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> riempimento </span> </p> </td> 
   <td colname="col2"> <p>Spaziatura interna riga. </p> </td> 
  </tr> 
 </tbody> 
</table>

Esempio: per impostare una maschera di finestra di dialogo con una spaziatura di dieci pixel per ogni linea:

```
.s7ecatalogviewer .s7emaildialog .s7dialogbody .s7dialogline { 
    padding: 10px; 
}
```

Tutte le etichette statiche nel modulo della finestra di dialogo sono controllate con il seguente selettore di classe CSS:

```
.s7ecatalogviewer .s7emaildialog .s7dialoglabel
```

Questa classe non è adatta per controllare le dimensioni o la posizione delle etichette, poiché può essere applicata a testi in varie posizioni dell&#39;interfaccia utente del modulo.

**Proprietà CSS dell&#39;etichetta della finestra di dialogo. **

<table id="table_13C7874807314ADD83A23075ABB4C340"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-weight </span> </p> </td> 
   <td colname="col2"> <p>Spessore font etichetta. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size </span> </p> </td> 
   <td colname="col2"> <p>Dimensione font etichetta. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family </span> </p> </td> 
   <td colname="col2"> <p>Famiglia font etichetta. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color </span> </p> </td> 
   <td colname="col2"> <p>Colore testo etichetta. </p> </td> 
  </tr> 
 </tbody> 
</table>

Le etichette delle finestre di dialogo possono essere localizzate. Consulta [Localizzazione degli elementi dell’interfaccia utente](../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) per ulteriori informazioni.

Esempio: per impostare tutte le etichette in grigio, grassetto, con un carattere di nove pixel:

```
.s7ecatalogviewer .s7emaildialog .s7dialoglabel { 
    color: #666666; 
    font-size: 9pt; 
    font-weight: bold; 
}
```

Tutte le etichette statiche visualizzate a sinistra dei campi di input del modulo sono controllate da:

```
.s7ecatalogviewer .s7emaildialog .s7dialoginputlabel
```

**Proprietà CSS dell&#39;etichetta di input della finestra di dialogo**

<table id="table_B5CF02837BAA42C7B79B6D9DA20792DF"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Larghezza dell'etichetta statica. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> text-align </span> </p> </td> 
   <td colname="col2"> <p>Allineamento orizzontale del testo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margine </span> </p> </td> 
   <td colname="col2"> <p>Margine etichetta statico. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> riempimento </span> </p> </td> 
   <td colname="col2"> <p>Spaziatura per etichette statiche. </p> </td> 
  </tr> 
 </tbody> 
</table>

Esempio: per impostare le etichette dei campi di input su una larghezza di 50 pixel, allineate a destra, con dieci pixel di spaziatura interna e un margine di dieci pixel a destra:

```
.s7ecatalogviewer .s7emaildialog .s7dialoginputlabel { 
    margin-right: 10px; 
    padding: 10px; 
    text-align: right; 
    width: 50px; 
}
```

Ogni campo di input del modulo viene racchiuso nel contenitore, che consente di applicare un bordo personalizzato attorno al campo di input. Viene controllata con il seguente selettore di classe CSS:

```
.s7ecatalogviewer .s7emaildialog .s7dialoginputcontainer
```

**Proprietà CSS del contenitore di input della finestra di dialogo**

<table id="table_7BC1C5919A54483F8121D928DC63233A"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> bordo </span> </p> </td> 
   <td colname="col2"> <p>Bordo intorno al contenitore del campo di input. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> riempimento </span> </p> </td> 
   <td colname="col2"> <p>Spaziatura interna. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Il contenitore del campo di input supporta gli elementi facoltativi `state` selettore di attributi. È impostato su `verifyerror` quando l’utente commette un errore nel formato dei dati di input e la convalida in linea non riesce. Questo selettore di attributi può essere utilizzato per evidenziare un input utente errato nel modulo.

La maggior parte dei campi di input che si estendono dall&#39;etichetta a sinistra fino al bordo destro del corpo della finestra di dialogo (che include il campo Da e il campo Messaggio) sono controllati dal seguente selettore di classe CSS:

```
.s7ecatalogviewer .s7emaildialog .s7dialoginputwide
```

**Proprietà CSS del campo a livello di input della finestra di dialogo**

<table id="table_7275B4365DFA4C0386FA2BDB7204A517"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Larghezza campo di input. </p> </td> 
  </tr> 
 </tbody> 
</table>

Il campo A è più ristretto perché alloca spazio per il pulsante Rimuovi e-mail a destra. Viene controllata con il seguente selettore di classe CSS:

```
.s7ecatalogviewer .s7emaildialog .s7dialoginputshort
```

**Proprietà CSS del campo breve di input della finestra di dialogo**

<table id="table_DFA9059209FF4184BD483A529424E97F"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Larghezza campo di input. </p> </td> 
  </tr> 
 </tbody> 
</table>

Esempio: per impostare un modulo con un bordo grigio di un pixel con nove pixel di spaziatura attorno a tutti i campi di input. Per avere lo stesso bordo in rosso per i campi che non superano la convalida. Per avere 250 pixel di larghezza nel campo A. Infine, il resto dei campi di input ha una larghezza di 300 pixel:

```
.s7ecatalogviewer .s7emaildialog .s7dialoginputcontainer { 
    border: 1px solid #CCCCCC; 
    padding: 9px; 
} 
.s7ecatalogviewer .s7emaildialog .s7dialoginputcontainer[state="verifyerror"] { 
    border: 1px solid #FF0000; 
} 
.s7ecatalogviewer .s7emaildialog .s7dialoginputshort { 
    width: 250px; 
} 
.s7ecatalogviewer .s7emaildialog .s7dialoginputwide { 
    width: 300px; 
}
```

Il campo di input del messaggio e-mail è controllato anche con:

```
.s7ecatalogviewer .s7emaildialog .s7dialogmessage
```

Questa classe consente di impostare proprietà specifiche per il sottostante `TEXTAREA` elemento.

**Proprietà CSS del messaggio della finestra di dialogo**

<table id="table_9E9D5A0C3CDB45739615C4C07F8DC046"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Altezza del messaggio. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ritorno a capo automatico </span> </p> </td> 
   <td colname="col2"> <p>Stile a capo automatico. </p> </td> 
  </tr> 
 </tbody> 
</table>

Esempio: per impostare un messaggio e-mail con un’altezza di 50 pixel e utilizzare `break-word` ritorno a capo automatico:

```
.s7ecatalogviewer .s7emaildialog .s7dialogmessage { 
    height: 50px; 
    word-wrap: break-word; 
}
```

Il pulsante Aggiungi un altro indirizzo e-mail consente a un utente di aggiungere più di un destinatario nel modulo e-mail. Viene controllata con il seguente selettore di classe CSS:

```
.s7ecatalogviewer .s7emaildialog .s7dialogaddemailbutton
```

**Proprietà CSS della finestra di dialogo pulsante Aggiungi indirizzo e-mail**

<table id="table_8829DC0694684E8BA427DFB821F7433D"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Altezza pulsante. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color </span> </p> </td> 
   <td colname="col2"> <p>Colore testo pulsante per ogni stato. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image </span> </p> </td> 
   <td colname="col2"> <p>Immagine pulsante per ogni stato. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p>Posizione dell'immagine del pulsante all'interno dell'area del pulsante. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-weight </span> </p> </td> 
   <td colname="col2"> <p>Spessore font pulsante. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size </span> </p> </td> 
   <td colname="col2"> <p>Dimensione font pulsante. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family </span> </p> </td> 
   <td colname="col2"> <p>Famiglia font pulsante. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> line-height </span> </p> </td> 
   <td colname="col2"> <p>Altezza del testo all'interno del pulsante. Influisce sull'allineamento verticale. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> text-align </span> </p> </td> 
   <td colname="col2"> <p>Allineamento orizzontale del testo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> riempimento </span> </p> </td> 
   <td colname="col2"> <p>Spaziatura interna. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Questo pulsante supporta `state` selettore di attributi, che può essere utilizzato per applicare interfacce diverse a stati di pulsante diversi.

La descrizione comando del pulsante può essere localizzata. Consulta [Localizzazione degli elementi dell’interfaccia utente](../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) per ulteriori informazioni.

Esempio: per impostare il pulsante &quot;Aggiungi un altro indirizzo e-mail&quot; ad un’altezza di 25 pixel, utilizza un font in grassetto a 12 punti con allineamento a destra e un colore di testo e un’immagine diversi per ogni stato:

```
.s7ecatalogviewer .s7emaildialog .s7dialogaddemailbutton { 
 text-align:right; 
 font-size:12pt; 
 font-weight:bold; 
 background-position:left center; 
 line-height:25px; 
 padding-left:30px; 
 height:25px; 
} 
.s7ecatalogviewer .s7emaildialog .s7dialogaddemailbutton[state='up'] { 
 color:#666666; 
 background-image:url(images/sdk/dlgaddplus_up.png); 
} 
.s7ecatalogviewer .s7emaildialog .s7dialogaddemailbutton[state='down'] { 
 color:#000000; 
 background-image:url(images/sdk/dlgaddplus_over.png); 
} 
.s7ecatalogviewer .s7emaildialog .s7dialogaddemailbutton[state='over'] { 
 color:#000000; 
 text-decoration:underline; 
 background-image:url(images/sdk/dlgaddplus_over.png); 
} 
.s7ecatalogviewer .s7emaildialog .s7dialogaddemailbutton[state='disabled'] { 
 color:#666666; 
 background-image:url(images/sdk/dlgaddplus_up.png); 
}
```

Il pulsante Rimuovi consente a un utente di rimuovere indirizzi aggiuntivi dal modulo e-mail. Viene controllata con il seguente selettore di classe CSS:

```
.s7ecatalogviewer .s7emaildialog .s7dialogremoveemailbutton
```

**Proprietà CSS della finestra di dialogo Rimuovi pulsante e-mail**

<table id="table_79E4C65741E64859B9C9E9DCCB3D050B"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Larghezza pulsante. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Altezza pulsante. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image </span> </p> </td> 
   <td colname="col2"> <p>Immagine pulsante per ogni stato. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> Posizionate all'interno dello sprite del disegno, se vengono utilizzati gli sprite CSS. </p> <p>Vedi anche <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-customizingviewer/c-html5-20-ecatalog-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> Spunti CSS </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Questo pulsante supporta `state` selettore di attributi, che può essere utilizzato per applicare interfacce diverse a stati di pulsante diversi.

La descrizione comando del pulsante può essere localizzata. Consulta [Localizzazione degli elementi dell’interfaccia utente](../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) per ulteriori informazioni.

Esempio - per impostare un pulsante di rimozione di 25 x 25 pixel e utilizzare un&#39;immagine diversa per ogni stato:

```
.s7ecatalogviewer .s7emaildialog .s7dialogremoveemailbutton { 
 width:25px; 
 height:25px; 
} 
.s7ecatalogviewer .s7emaildialog .s7dialogremoveemailbutton[state='up'] { 
 background-image:url(images/sdk/dlgremove_up.png); 
} 
.s7ecatalogviewer .s7emaildialog .s7dialogremoveemailbutton[state='over'] { 
 background-image:url(images/sdk/dlgremove_over.png); 
} 
.s7ecatalogviewer .s7emaildialog .s7dialogremoveemailbutton[state='down'] { 
 background-image:url(images/sdk/dlgremove_over.png); 
} 
.s7ecatalogviewer .s7emaildialog .s7dialogremoveemailbutton[state='disabled'] { 
 background-image:url(images/sdk/dlgremove_up.png); 
}
```

Il contenuto condiviso viene visualizzato nella parte inferiore del corpo della finestra di dialogo e include una miniatura, un titolo, un URL di origine e una descrizione. Viene racchiuso in un contenitore controllato con il seguente selettore di classe CSS:

```
.s7ecatalogviewer .s7emaildialog .s7dialogbody .s7dialogcontent
```

**Proprietà CSS della finestra di dialogo ** contenuto

<table id="table_9C5CBFC2482E4A46BE837573B0B02FE4"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> bordo </span> </p> </td> 
   <td colname="col2"> <p>Bordo contenitore. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> riempimento </span> </p> </td> 
   <td colname="col2"> <p>Spaziatura interna. </p> </td> 
  </tr> 
 </tbody> 
</table>

Esempio: per impostare un contenitore inferiore con un bordo punteggiato di un pixel e senza spaziatura interna:

```
.s7ecatalogviewer .s7emaildialog .s7dialogbody .s7dialogcontent { 
    border: 1px dotted #A0A0A0; 
    padding: 0; 
}
```

L’immagine miniatura viene controllata con il seguente selettore di classe CSS:

```
.s7ecatalogviewer .s7emaildialog .s7dialogthumbnail
```

Il `background-image` viene impostata dalla logica del componente.

**Proprietà CSS dell&#39;immagine miniatura della finestra di dialogo**

<table id="table_4C614FF2CEB149DAB5B7D7BC38CD3CAE"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Larghezza miniatura. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Altezza miniature. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Allineamento verticale </span> </p> </td> 
   <td colname="col2"> <p>Miniatura allineamento verticale. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> riempimento </span> </p> </td> 
   <td colname="col2"> <p>Spaziatura interna. </p> </td> 
  </tr> 
 </tbody> 
</table>

Esempio: per impostare la miniatura su 90 x 60 pixel e allineata in alto con dieci pixel di spaziatura interna:

```
.s7ecatalogviewer .s7emaildialog .s7dialogthumbnail { 
    height: 60px; 
    padding: 10px; 
    vertical-align: top; 
    width: 90px; 
}
```

Il titolo, l’origine e la descrizione del contenuto sono ulteriormente raggruppati in un pannello a destra della miniatura del contenuto. Viene controllata con il seguente selettore di classe CSS:

```
.s7ecatalogviewer .s7emaildialog .s7dialoginfopanel
```

**Proprietà CSS del pannello informazioni della finestra di dialogo**

<table id="table_EDFA6229D8C3468E989E7EC05F23EF3B"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Larghezza pannello. </p> </td> 
  </tr> 
 </tbody> 
</table>

Esempio: per impostare una larghezza di 300 pixel per il pannello informazioni contenuto:

```
.s7ecatalogviewer .s7emaildialog .s7dialoginfopanel { 
    width: 300px; 
}
```

Il titolo del contenuto è controllato dal seguente selettore di classe CSS:

```
.s7ecatalogviewer .s7emaildialog .s7dialogtitle
```

**Proprietà CSS del titolo della finestra di dialogo**

<table id="table_E83C149E66EC474092DF8A180DA9A550"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margine </span> </p> </td> 
   <td colname="col2"> <p>Margine esterno. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-weight </span> </p> </td> 
   <td colname="col2"> <p>Spessore font. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size </span> </p> </td> 
   <td colname="col2"> <p>Dimensione font. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family </span> </p> </td> 
   <td colname="col2"> <p>Famiglia di caratteri. </p> </td> 
  </tr> 
 </tbody> 
</table>

Esempio: per impostare un titolo di contenuto con font in grassetto e un margine di dieci pixel:

```
.s7ecatalogviewer .s7emaildialog .s7dialogtitle { 
    font-weight: bold; 
    margin: 10px; 
}
```

L’origine del contenuto è controllata con il seguente selettore di classe CSS:

```
.s7ecatalogviewer .s7emaildialog .s7dialogorigin
```

**Proprietà CSS della finestra di dialogo ** origine contenuto

<table id="table_51763B532A9C4AE8AE54B69933A8C0B5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margine </span> </p> </td> 
   <td colname="col2"> <p>Margine esterno. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-weight </span> </p> </td> 
   <td colname="col2"> <p>Spessore font. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size </span> </p> </td> 
   <td colname="col2"> <p>Dimensione font. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family </span> </p> </td> 
   <td colname="col2"> <p>Famiglia di caratteri. </p> </td> 
  </tr> 
 </tbody> 
</table>

Esempio: per impostare l’origine del contenuto con un margine di dieci pixel:

```
.s7ecatalogviewer .s7emaildialog .s7dialogorigin { 
    margin: 10px; 
}
```

La descrizione del contenuto è controllata dal seguente selettore di classe CSS:

```
.s7ecatalogviewer .s7emaildialog .s7dialogdescription
```

**Proprietà CSS della descrizione del contenuto della finestra di dialogo**

<table id="table_F0F917ED3D1D4FCE974F48214D287E14"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margine </span> </p> </td> 
   <td colname="col2"> <p>Margine esterno. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-weight </span> </p> </td> 
   <td colname="col2"> <p>Spessore font. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size </span> </p> </td> 
   <td colname="col2"> <p>Dimensione font. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family </span> </p> </td> 
   <td colname="col2"> <p>Famiglia di caratteri. </p> </td> 
  </tr> 
 </tbody> 
</table>

Esempio: per impostare una descrizione del contenuto con un margine di dieci pixel e utilizzare un font a nove punti:

```
.s7ecatalogviewer .s7emaildialog .s7dialogdescription { 
    font-size: 9pt; 
    margin: 10px; 
}
```

Quando un utente immette dati di input errati e la convalida in linea non riesce. In alternativa, quando la finestra di dialogo deve visualizzare un errore o un messaggio di conferma al momento dell&#39;invio del modulo, nella parte superiore del corpo della finestra di dialogo viene visualizzato un messaggio. Viene controllata con il seguente selettore di classe CSS:

```
.s7ecatalogviewer .s7emaildialog .s7dialogerrormessage
```

**Messaggio di errore Proprietà CSS della finestra di dialogo**

<table id="table_C114E1004C334D339C25A3438E8E6614"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image </span> </p> </td> 
   <td colname="col2"> <p> Icona di errore. Il valore predefinito è un punto esclamativo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> Posizione dell'icona di errore all'interno dell'area messaggi. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color </span> </p> </td> 
   <td colname="col2"> <p>Colore testo messaggio. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-weight </span> </p> </td> 
   <td colname="col2"> <p>Spessore font. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size </span> </p> </td> 
   <td colname="col2"> <p>Dimensione font. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family </span> </p> </td> 
   <td colname="col2"> <p>Famiglia di caratteri. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> line-height </span> </p> </td> 
   <td colname="col2"> <p> Altezza del testo nel messaggio. Influisce sull'allineamento verticale. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> riempimento </span> </p> </td> 
   <td colname="col2"> <p>Spaziatura interna. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Questo messaggio supporta `state` selettore di attributi con i seguenti valori possibili: `verifyerror`, `senderror`, e `sendsuccess`. Il valore `verifyerror` è impostato quando un messaggio viene visualizzato a causa di un errore di convalida dell’input in linea. Il valore `senderror` è impostato quando un servizio e-mail back-end segnala un errore. Il valore  `sendsuccess` è impostato quando l’e-mail viene inviata correttamente. In questo modo è possibile assegnare al messaggio uno stile diverso a seconda dello stato della finestra di dialogo.

La descrizione comando del pulsante può essere localizzata. Consulta [Localizzazione degli elementi dell’interfaccia utente](../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) per ulteriori informazioni.

Esempio: per impostare un messaggio per l’utilizzo di un font in grassetto a dieci punti, utilizza un’altezza della linea di 25 pixel, una spaziatura interna di 20 pixel a sinistra e un’icona con un punto esclamativo. Infine, testo rosso in caso di errore e nessuna icona e testo verde in caso di successo:

```
.s7ecatalogviewer .s7emaildialog .s7dialogerrormessage[state="verifyerror"] { 
    background-image: url("images/sdk/dlgerrimg.png"); 
    color: #FF0000; 
} 
.s7ecatalogviewer .s7emaildialog .s7dialogerrormessage[state="senderror"] { 
    background-image: url("images/sdk/dlgerrimg.png"); 
    color: #FF0000; 
} 
.s7ecatalogviewer .s7emaildialog .s7dialogerrormessage[state="sendsuccess"] { 
    background-image: none; 
    color: #00B200; 
} 
.s7ecatalogviewer .s7emaildialog .s7dialogerrormessage { 
    background-position: left center; 
    font-size: 10pt; 
    font-weight: bold; 
    line-height: 25px; 
    padding-left: 20px; 
}
```

Se è necessario lo scorrimento verticale, la barra di scorrimento viene riprodotta nel pannello vicino al bordo destro della finestra di dialogo, che è controllata dal seguente selettore di classe CSS:

```
.s7ecatalogviewer .s7emaildialog .s7dialogscrollpanel
```

**Proprietà CSS del pannello di scorrimento della finestra di dialogo**

<table id="table_A0C3AC7E00544FFBB8E1364F4CDDB371"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Larghezza pannello di scorrimento. </p> </td> 
  </tr> 
 </tbody> 
</table>

Esempio: per impostare un pannello di scorrimento con una larghezza di 44 pixel:

```
.s7ecatalogviewer .s7emaildialog .s7dialogscrollpanel { 
    width: 44px; 
}
```

L’aspetto dell’area della barra di scorrimento è controllato dal seguente selettore di classe CSS:

```
.s7ecatalogviewer .s7emaildialog .s7scrollbar
```

**Proprietà CSS della barra di scorrimento**

<table id="table_2BF74CF43E9B42D79F99A3F5208D7051"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p> Larghezza della barra di scorrimento. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> top </span> </p> </td> 
   <td colname="col2"> <p> Scostamento della barra di scorrimento verticale dalla parte superiore del pannello di scorrimento. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> bottom </span> </p> </td> 
   <td colname="col2"> <p> Scostamento della barra di scorrimento verticale dalla parte inferiore del pannello di scorrimento. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> destra </span> </p> </td> 
   <td colname="col2"> <p> Scostamento della barra di scorrimento orizzontale dal bordo destro del pannello di scorrimento. </p> </td> 
  </tr> 
 </tbody> 
</table>

Esempio: per impostare una barra di scorrimento larga 28 pixel, con un margine di otto pixel dalla parte superiore, destra e inferiore del pannello di scorrimento:

```
.s7ecatalogviewer .s7emaildialog .s7scrollbar { 
    bottom: 8px; 
    right: 8px; 
    top: 8px; 
    width: 28px; 
}
```

La traccia della barra di scorrimento è l&#39;area compresa tra i pulsanti di scorrimento superiore e inferiore. Il componente imposta automaticamente la posizione e l&#39;altezza della traccia. Il brano è controllato con il seguente selettore di classe CSS:

```
.s7ecatalogviewer .s7emaildialog .s7scrollbar .s7scrolltrack
```

**Proprietà CSS del brano di scorrimento**

<table id="table_EE990E7A342843619EDD84BAD29C6F2A"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Larghezza della traccia. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p>Colore di sfondo del brano. </p> </td> 
  </tr> 
 </tbody> 
</table>

Esempio: per impostare una traccia della barra di scorrimento larga 28 pixel e con sfondo grigio:

```
.s7ecatalogviewer .s7emaildialog .s7scrollbar .s7scrolltrack { 
width:28px; 
background-color: #B2B2B2; 
}
```

Il pollice della barra di scorrimento si sposta verticalmente all&#39;interno dell&#39;area della traccia di scorrimento. La sua posizione verticale è completamente controllata dalla logica del componente, tuttavia l’altezza del pollice non cambia in modo dinamico a seconda della quantità di contenuto. Puoi configurare l’altezza del pollice e altri aspetti con il seguente selettore di classe CSS:

```
.s7ecatalogviewer .s7emaildialog .s7scrollbar .s7scrollthumb
```

**Proprietà CSS del cursore della barra di scorrimento**

<table id="table_5A4A283A50044A51881D997885674BDF"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Larghezza del pollice. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Altezza del pollice. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> riempimento superiore </span> </p> </td> 
   <td colname="col2"> <p> Spaziatura verticale tra la parte superiore del brano. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> padding-bottom </span> </p> </td> 
   <td colname="col2"> <p> Spaziatura verticale tra la parte inferiore del brano. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image </span> </p> </td> 
   <td colname="col2"> <p>Immagine visualizzata per un determinato stato del pollice. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> Posizionate all'interno dello sprite del disegno, se vengono utilizzati gli sprite CSS. </p> <p>Vedi anche <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-customizingviewer/c-html5-20-ecatalog-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> Spunti CSS </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Il miniatura supporta `state` selettore di attributi, che può essere utilizzato per applicare skin diversi a stati miniatura diversi: `up`, `down`, `over`, e `disabled`.

Esempio: per impostare il pollice della barra di scorrimento che è di 28 x 45 pixel, ha un margine di dieci pixel in alto e in basso e ha un disegno diverso per ogni stato:

```
.s7ecatalogviewer .s7emaildialog .s7scrollbar .s7scrollthumb { 
    height: 45px; 
    padding-bottom: 10px; 
    padding-top: 10px; 
    width: 28px; 
} 
.s7ecatalogviewer .s7emaildialog .s7scrollbar .s7scrollthumb[state="up"] { 
 background-image:url("images/sdk/scrollbar_thumb_up.png"); 
} 
.s7ecatalogviewer .s7emaildialog .s7scrollbar .s7scrollthumb[state="down"] { 
 background-image:url("images/sdk/scrollbar_thumb_down.png"); 
} 
.s7ecatalogviewer .s7emaildialog .s7scrollbar .s7scrollthumb[state="over"] { 
 background-image:url("images/sdk/scrollbar_thumb_over.png"); 
} 
.s7ecatalogviewer .s7emaildialog .s7scrollbar .s7scrollthumb[state="disabled"] { 
 background-image:url("images/sdk/scrollbar_thumb_disabled.png"); 
}
```

L’aspetto dei pulsanti di scorrimento superiore e inferiore è controllato dai seguenti selettori di classi CSS:

```
.s7ecatalogviewer .s7emaildialog .s7scrollbar .s7scrollupbutton
```

```
.s7ecatalogviewer .s7emaildialog .s7scrollbar .s7scrolldownbutton
```

Non è possibile posizionare i pulsanti di scorrimento utilizzando CSS `top`, `left`, `bottom`, e `right` proprietà. Al contrario, la logica di visualizzazione li posiziona automaticamente.

**Proprietà CSS dei pulsanti di scorrimento superiore e inferiore**

<table id="table_EB853317E08941979B0E141C3C9B2C49"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Larghezza pulsante. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Altezza pulsante. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image </span> </p> </td> 
   <td colname="col2"> <p>Immagine visualizzata per un determinato stato del pulsante. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> Posizionate all'interno dello sprite del disegno, se vengono utilizzati gli sprite CSS. </p> <p>Vedi anche <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-customizingviewer/c-html5-20-ecatalog-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> Spunti CSS </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Questi pulsanti supportano `state` selettore di attributi, che può essere utilizzato per applicare skin diversi a stati di pulsante diversi: `up`, `down`, `over`, e `disabled`.

La descrizione comando del pulsante può essere localizzata. Consulta [Localizzazione degli elementi dell’interfaccia utente](../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) per ulteriori informazioni.

Esempio - per impostare pulsanti di scorrimento di 28 x 32 pixel con grafica diversa per ogni stato:

```
.s7ecatalogviewer .s7emaildialog .s7scrollbar .s7scrollupbutton { 
 width:28px; 
 height:32px; 
} 
.s7ecatalogviewer .s7emaildialog .s7scrollbar .s7scrollupbutton[state='up'] { 
background-image:url(images/sdk/scroll_up_up.png); 
} 
.s7ecatalogviewer .s7emaildialog .s7scrollbar .s7scrollupbutton[state='over'] { 
 background-image:url(images/sdk/scroll_up_over.png); 
} 
.s7ecatalogviewer .s7emaildialog .s7scrollbar .s7scrollupbutton[state='down'] { 
 background-image:url(images/sdk/scroll_up_down.png); 
} 
.s7ecatalogviewer .s7emaildialog .s7scrollbar .s7scrollupbutton[state='disabled'] { 
 background-image:url(images/sdk/scroll_up_disabled.png); 
} 
.s7ecatalogviewer .s7emaildialog .s7scrollbar .s7scrolldownbutton { 
 width:28px; 
 height:32px; 
} 
.s7ecatalogviewer .s7emaildialog .s7scrollbar .s7scrolldownbutton[state='up'] { 
 background-image:url(images/sdk/scroll_down_up.png); 
} 
.s7ecatalogviewer .s7emaildialog .s7scrollbar .s7scrolldownbutton[state='over'] { 
 background-image:url(images/sdk/scroll_down_over.png); 
} 
.s7ecatalogviewer .s7emaildialog .s7scrollbar .s7scrolldownbutton[state='down'] { 
 background-image:url(images/sdk/scroll_down_down.png); 
} 
.s7ecatalogviewer .s7emaildialog .s7scrollbar .s7scrolldownbutton[state='disabled'] { 
 background-image:url(images/sdk/scroll_down_disabled.png); 
}
```
