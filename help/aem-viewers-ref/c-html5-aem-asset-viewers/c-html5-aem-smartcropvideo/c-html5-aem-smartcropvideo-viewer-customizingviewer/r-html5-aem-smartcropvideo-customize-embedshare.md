---
title: Incorpora condivisione
description: Lo strumento di incorporamento della condivisione è costituito da un pulsante aggiunto al pannello Condivisione social e dalla finestra di dialogo modale visualizzata quando lo strumento viene attivato. La posizione del pulsante è completamente gestita dallo strumento Condivisione social.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
exl-id: d5f8db82-f1f9-45be-990d-ebfef97507b6
source-git-commit: 97fbf820590b53de5a1e6ce904e44d6b0ef9a214
workflow-type: tm+mt
source-wordcount: '2621'
ht-degree: 0%

---

# Incorpora condivisione{#embed-share}

Lo strumento di incorporamento della condivisione è costituito da un pulsante aggiunto al pannello Condivisione social e dalla finestra di dialogo modale visualizzata quando lo strumento viene attivato. La posizione del pulsante è completamente gestita dallo strumento Condivisione social.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

L’aspetto del pulsante di incorporamento della condivisione è controllato dal seguente selettore di classe CSS:

```
.s7smartcropvideoviewer .s7embedshare
```

**Proprietà CSS dello strumento di condivisione da incorporare**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> larghezza </span> </p> </td> 
   <td colname="col2"> <p>Larghezza pulsante. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> altezza </span> </p> </td> 
   <td colname="col2"> <p>Altezza pulsante. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> immagine di sfondo </span> </p> </td> 
   <td colname="col2"> <p> Immagine visualizzata per un determinato stato del pulsante. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> Posizionate all'interno dello sprite del disegno, se vengono utilizzati gli sprite CSS. </p> <p>Vedere <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-smartcropvideo/c-html5-aem-smartcropvideo-viewer-customizingviewer/c-html5-aem-smartcropvideo-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> sprite CSS </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Questo pulsante supporta il selettore di attributi `state`, che può essere utilizzato per applicare interfacce diverse a diversi stati di pulsante.

È possibile rimuovere il pulsante dal pannello Condivisione social impostando la proprietà CSS `display:none` sulla relativa classe CSS.

La descrizione comando del pulsante può essere localizzata. Per ulteriori informazioni, vedere [Localizzazione degli elementi dell&#39;interfaccia utente](../../../c-html5-aem-asset-viewers/c-html5-aem-smartcropvideo/r-html5-aem-smartcropvideo-viewer-localization.md#concept-1d5ca2d8480f4064a51eddba13940aad).

Esempio: per impostare un pulsante di condivisione da incorporare di 28 x 28 pixel e visualizzare un&#39;immagine diversa per ciascuno dei quattro stati dei pulsanti:

```
.s7smartcropvideoviewer .s7embedshare { 
 width:28px; 
 height:28px; 
} 
.s7smartcropvideoviewer .s7embedshare[state='up'] { 
background-image:url(images/v2/EmbedShare_dark_up.png); 
} 
.s7smartcropvideoviewer .s7embedshare[state='over'] { 
background-image:url(images/v2/EmbedShare_dark_over.png); 
} 
.s7smartcropvideoviewer .s7embedshare[state='down'] { 
background-image:url(images/v2/EmbedShare_dark_down.png); 
} 
.s7smartcropvideoviewer .s7embedshare[state='disabled'] { 
background-image:url(images/v2/EmbedShare_dark_disabled.png); 
}
```

La sovrapposizione di sfondo che copre la pagina web quando la finestra di dialogo è attiva è controllata dal seguente selettore di classe CSS:

```
.s7smartcropvideoviewer .s7embeddialog .s7backoverlay
```

**Proprietà CSS della sovrapposizione in background**

<table id="table_DB4183CE8061425084D495A355A941F8"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> opacità </span> </p> </td> 
   <td colname="col2"> <p>Opacità sovrapposizione sfondo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> colore di sfondo </span> </p> </td> 
   <td colname="col2"> <p>Colore di sovrapposizione sfondo. </p> </td> 
  </tr> 
 </tbody> 
</table>

Esempio: per impostare la sovrapposizione di sfondo su grigio con opacità 70%:

```
.s7smartcropvideoviewer .s7embeddialog .s7backoverlay { 
 opacity:0.7; 
 background-color:#222222; 
}
```

Per impostazione predefinita, la finestra di dialogo modale viene visualizzata centrata sullo schermo dei sistemi desktop e occupa l’intera area della pagina web sui dispositivi touch. In tutti i casi, il posizionamento e il ridimensionamento della finestra di dialogo vengono gestiti dal componente. La finestra di dialogo è controllata dal seguente selettore di classe CSS:

```
.s7smartcropvideoviewer .s7embeddialog .s7dialog
```

**Proprietà CSS della finestra di dialogo**

<table id="table_E31711ADF4C7446182549244362199A3"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> raggio bordo </span> </p> </td> 
   <td colname="col2"> <p> Raggio del bordo della finestra di dialogo, nel caso in cui la finestra di dialogo non occupi l'intero browser. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> colore di sfondo </span> </p> </td> 
   <td colname="col2"> <p>Colore di sfondo della finestra di dialogo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> larghezza </span> </p> </td> 
   <td colname="col2"> <p>Deve essere disattivato o impostato su 100%, nel qual caso la finestra di dialogo occupa l'intera finestra del browser (questa modalità è preferita sui dispositivi touch). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> altezza </span> </p> </td> 
   <td colname="col2"> <p>Deve essere disattivato o impostato su 100%, nel qual caso la finestra di dialogo occupa l'intera finestra del browser (questa modalità è preferita sui dispositivi touch). </p> </td> 
  </tr> 
 </tbody> 
</table>

Esempio: per impostare la finestra di dialogo in modo da utilizzare l&#39;intera finestra del browser e avere uno sfondo bianco sui dispositivi touch:

```
.s7smartcropvideoviewer .s7touchinput .s7embeddialog .s7dialog { 
 width:100%; 
 height:100%; 
background-color: #ffffff; 
}
```

L&#39;intestazione della finestra di dialogo è costituita da un&#39;icona, un testo del titolo e un pulsante di chiusura. Il contenitore di intestazione è controllato con

```
.s7smartcropvideoviewer .s7embeddialog .s7dialogheader
```

**Proprietà CSS dell&#39;intestazione della finestra di dialogo**

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
.s7smartcropvideoviewer .s7embeddialog .s7dialogheader .s7dialogline
```

**Proprietà CSS della riga di dialogo**

<table id="table_5B03CF843F0D4B1295A3FC1EB50C56F1"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> riempimento </span> </p> </td> 
   <td colname="col2"> <p> Spaziatura interna per l'icona e il titolo dell'intestazione </p> </td> 
  </tr> 
 </tbody> 
</table>

L’icona dell’intestazione è controllata dal seguente selettore di classe CSS

```
.s7smartcropvideoviewer .s7embeddialog .s7dialogheadericon
```

**Proprietà CSS dell&#39;icona dell&#39;intestazione della finestra di dialogo**

<table id="table_DD4B0413721B49CE8E21B4A55BDE8F7D"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> larghezza </span> </p> </td> 
   <td colname="col2"> <p>Larghezza icona. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> altezza </span> </p> </td> 
   <td colname="col2"> <p>Altezza icona. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> immagine di sfondo </span> </p> </td> 
   <td colname="col2"> <p>Immagine icona. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> Posizionate all'interno dello sprite del disegno, se vengono utilizzati gli sprite CSS. </p> <p>Vedere <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-smartcropvideo/c-html5-aem-smartcropvideo-viewer-customizingviewer/c-html5-aem-smartcropvideo-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> sprite CSS </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

Il titolo dell’intestazione è controllato dal seguente selettore di classe CSS:

```
.s7smartcropvideoviewer .s7embeddialog .s7dialogheadertext
```

**Proprietà CSS del testo dell&#39;intestazione della finestra di dialogo**

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
   <td colname="col1"> <p> <span class="codeph"> famiglia di caratteri </span> </p> </td> 
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
.s7smartcropvideoviewer .s7embeddialog .s7closebutton
```

**Proprietà CSS del &#x200B;** del pulsante Chiudi

<table id="table_FAECBC489FC442588E50E3DA0AC16DD7"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> primi </span> </p> </td> 
   <td colname="col2"> <p> Posizione verticale del pulsante rispetto al contenitore di intestazione. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> a destra </span> </p> </td> 
   <td colname="col2"> <p> Posizione del pulsante orizzontale relativa al contenitore di intestazione. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> larghezza </span> </p> </td> 
   <td colname="col2"> <p>Larghezza pulsante. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> altezza </span> </p> </td> 
   <td colname="col2"> <p>Altezza pulsante. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> riempimento </span> </p> </td> 
   <td colname="col2"> <p>Spaziatura interna del pulsante. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> immagine di sfondo </span> </p> </td> 
   <td colname="col2"> <p>Immagine pulsante per ogni stato. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> Posizionate all'interno dello sprite del disegno, se vengono utilizzati gli sprite CSS. </p> <p>Vedere <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-smartcropvideo/c-html5-aem-smartcropvideo-viewer-customizingviewer/c-html5-aem-smartcropvideo-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> sprite CSS </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Questo pulsante supporta il selettore di attributi `state`, che può essere utilizzato per applicare interfacce diverse a diversi stati di pulsante.

È possibile localizzare la descrizione comando del pulsante Chiudi e il titolo della finestra di dialogo. Per ulteriori informazioni, vedere [Localizzazione degli elementi dell&#39;interfaccia utente](../../../c-html5-aem-asset-viewers/c-html5-aem-smartcropvideo/r-html5-aem-smartcropvideo-viewer-localization.md#concept-1d5ca2d8480f4064a51eddba13940aad).

Esempio: per impostare un&#39;intestazione di finestra di dialogo con spaziatura interna, icona 24 x 14 pixel, titolo in grassetto a 16 punti e pulsante Chiudi 28 x 28 pixel. Posizionare infine due pixel dalla parte superiore e due pixel dalla parte destra del contenitore della finestra di dialogo:

```
.s7smartcropvideoviewer .s7embeddialog .s7dialogheader { 
 padding: 10px; 
} 
.s7smartcropvideoviewer .s7embeddialog .s7dialogheader .s7dialogline { 
 padding: 10px 10px 2px; 
} 
.s7smartcropvideoviewer .s7embeddialog .s7dialogheadericon { 
    background-image: url("images/sdk/dlgembed_cap.png"); 
    height: 14px; 
    width: 24px; 
} 
.s7smartcropvideoviewer .s7embeddialog .s7dialogheadertext { 
    font-size: 16pt; 
    font-weight: bold; 
    padding-left: 16px; 
} 
.s7smartcropvideoviewer .s7embeddialog .s7closebutton { 
 top:2px; 
 right:2px; 
 padding:8px; 
 width:28px; 
 height:28px; 
} 
.s7smartcropvideoviewer .s7embeddialog .s7closebutton[state='up'] { 
 background-image:url(images/sdk/close_up.png); 
} 
.s7smartcropvideoviewer .s7embeddialog .s7closebutton[state='over'] { 
 background-image:url(images/sdk/close_over.png); 
} 
.s7smartcropvideoviewer .s7embeddialog .s7closebutton[state='down'] { 
 background-image:url(images/sdk/close_down.png); 
} 
.s7smartcropvideoviewer .s7embeddialog .s7closebutton[state='disabled'] { 
 background-image:url(images/sdk/close_disabled.png); 
}
```

Il piè di pagina della finestra di dialogo è costituito dal pulsante Annulla. Il contenitore piè di pagina è controllato dal seguente selettore di classe CSS:

```
.s7smartcropvideoviewer .s7embeddialog .s7dialogfooter
```

**Proprietà CSS del &#x200B;** piè di pagina della finestra di dialogo

<table id="table_0AF7AAAB846A46D690896AFD68575669"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> bordo </span> </p> </td> 
   <td colname="col2"> <p> Bordo che consente di separare visivamente il piè di pagina dal resto della finestra di dialogo. </p> </td> 
  </tr> 
 </tbody> 
</table>

Il piè di pagina contiene un contenitore interno che mantiene il pulsante. Viene controllata con il seguente selettore di classe CSS:

```
.s7smartcropvideoviewer .s7embeddialog .s7dialogbuttoncontainer
```

**Proprietà CSS del contenitore del pulsante della finestra di dialogo**

<table id="table_C34906888A8145C7A61E503DFC6B08A9"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> riempimento </span> </p> </td> 
   <td colname="col2"> <p> Spaziatura interna tra piè di pagina e pulsante. </p> </td> 
  </tr> 
 </tbody> 
</table>

Il pulsante Seleziona tutto è controllato dal seguente selettore di classe CSS:

```
.s7smartcropvideoviewer .s7embeddialog .s7dialogactionbutton
```

Il pulsante è disponibile solo sui sistemi desktop.

**Proprietà CSS del pulsante Seleziona tutto**

<table id="table_021D0467632F49FEBFDF4CF96D2D67C7"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> larghezza </span> </p> </td> 
   <td colname="col2"> <p>Larghezza pulsante. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> altezza </span> </p> </td> 
   <td colname="col2"> <p>Altezza pulsante. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> colore </span> </p> </td> 
   <td colname="col2"> <p> Colore testo pulsante per ogni stato. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> colore di sfondo </span> </p> </td> 
   <td colname="col2"> <p> Colore di sfondo pulsante per ogni stato. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Il pulsante Seleziona tutto supporta il selettore di attributi `state`, che può essere utilizzato per applicare interfacce diverse a diversi stati dei pulsanti.

Il pulsante Annulla è controllato dal seguente selettore di classe CSS:

```
.s7smartcropvideoviewer .s7embeddialog .s7dialogcancelbutton
```

**Proprietà CSS del pulsante Annulla della finestra di dialogo**

<table id="table_3DFA90B012F345A3A2A123D6856BE08A"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> larghezza </span> </p> </td> 
   <td colname="col2"> <p>Larghezza pulsante. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> altezza </span> </p> </td> 
   <td colname="col2"> <p>Altezza pulsante. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> colore </span> </p> </td> 
   <td colname="col2"> <p> Colore testo pulsante per ogni stato. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> colore di sfondo </span> </p> </td> 
   <td colname="col2"> <p> Colore di sfondo pulsante per ogni stato. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Il pulsante Annulla supporta il selettore di attributi `state`, che può essere utilizzato per applicare interfacce diverse a diversi stati di pulsante.

Inoltre, entrambi i pulsanti condividono la stessa classe CSS che può contenere impostazioni CSS identiche a quelle degli altri pulsanti della finestra di dialogo:

```
.s7smartcropvideoviewer .s7embeddialog .s7dialogfooter .s7button
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
   <td colname="col1"> <p> <span class="codeph"> famiglia di caratteri </span> </p> </td> 
   <td colname="col2"> <p>Famiglia font pulsante. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> altezza riga </span> </p> </td> 
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

Le descrizioni dei pulsanti possono essere localizzate. Per ulteriori informazioni, vedere [Localizzazione degli elementi dell&#39;interfaccia utente](../../../c-html5-aem-asset-viewers/c-html5-aem-smartcropvideo/r-html5-aem-smartcropvideo-viewer-localization.md#concept-1d5ca2d8480f4064a51eddba13940aad).

Esempio: per impostare un piè di pagina della finestra di dialogo con un pulsante Annulla 64 x 34, con un colore del testo e un colore di sfondo diversi per ogni stato del pulsante:

```
.s7smartcropvideoviewer .s7embeddialog .s7dialogfooter { 
    border-top: 1px solid #909090; 
} 
.s7smartcropvideoviewer .s7embeddialog .s7dialogbuttoncontainer { 
    padding-bottom: 6px; 
    padding-top: 10px; 
} 
.s7smartcropvideoviewer .s7embeddialog .s7dialogfooter .s7button { 
    box-shadow: 1px 1px 1px #999999; 
    color: #FFFFFF; 
    font-size: 9pt; 
    font-weight: bold; 
    line-height: 34px; 
    margin-right: 10px; 
} 
.s7smartcropvideoviewer .s7embeddialog .s7dialogcancelbutton { 
 width:64px; 
 height:34px; 
} 
.s7smartcropvideoviewer .s7embeddialog .s7dialogcancelbutton[state='up'] { 
 background-color:#666666; 
 color:#dddddd; 
} 
.s7smartcropvideoviewer .s7embeddialog .s7dialogcancelbutton[state='down'] { 
 background-color:#555555; 
 color:#ffffff; 
} 
.s7smartcropvideoviewer .s7embeddialog .s7dialogcancelbutton[state='over'] { 
 background-color:#555555; 
 color:#ffffff; 
} 
.s7smartcropvideoviewer .s7embeddialog .s7dialogcancelbutton[state='disabled'] { 
 background-color:#b2b2b2; 
 color:#dddddd; 
} 
.s7smartcropvideoviewer .s7embeddialog .s7dialogactionbutton { 
 width:82px; 
 height:34px; 
} 
.s7smartcropvideoviewer .s7embeddialog .s7dialogactionbutton[state='up'] { 
 background-color:#333333; 
 color:#dddddd; 
} 
.s7smartcropvideoviewer .s7embeddialog .s7dialogactionbutton[state='down'] { 
 background-color:#222222; 
 color:#cccccc; 
} 
.s7smartcropvideoviewer .s7embeddialog .s7dialogactionbutton[state='over'] { 
 background-color:#222222; 
 color:#cccccc; 
} 
.s7smartcropvideoviewer .s7embeddialog .s7dialogactionbutton[state='disabled'] { 
 background-color:#b2b2b2; 
 color:#dddddd; 
}
```

L’area della finestra di dialogo principale, tra l’intestazione e il piè di pagina, contiene il contenuto della finestra di dialogo con scorrimento e il pannello di scorrimento a destra. In tutti i casi in cui il componente gestisce la larghezza di quest’area, non è possibile impostarla in CSS. L’area della finestra di dialogo principale è controllata dal seguente selettore di classe CSS:

```
.s7smartcropvideoviewer .s7embeddialog .s7dialogviewarea
```

**Proprietà CSS della finestra di dialogo &#x200B;** area di visualizzazione

<table id="table_3FF4691D848A4C4D8EF060B7E79DEEDE"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> altezza </span> </p> </td> 
   <td colname="col2"> <p> Altezza della finestra di dialogo principale. Deve essere specificato solo quando la finestra di dialogo funziona in modalità desktop. Non è applicabile quando la finestra di dialogo viene ridimensionata per occupare l'intera finestra del browser. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> colore di sfondo </span> </p> </td> 
   <td colname="col2"> <p>Colore di sfondo dell'area della finestra di dialogo principale. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margine </span> </p> </td> 
   <td colname="col2"> <p>Margine esterno. </p> </td> 
  </tr> 
 </tbody> 
</table>

Esempio: per impostare un&#39;area della finestra di dialogo principale di 300 pixel, avere un margine di dieci pixel e utilizzare uno sfondo bianco:

```
.s7smartcropvideoviewer .s7embeddialog .s7dialogviewarea { 
 background-color:#ffffff; 
 margin:10px; 
 height:300px; 
}
```

Tutto il contenuto del modulo (come etichette e campi di input) si trova all’interno di un contenitore controllato con

```
.s7smartcropvideoviewer .s7embeddialog .s7dialogbody
```

Se l’altezza del contenitore risulta maggiore dell’area della finestra di dialogo principale, il componente abilita automaticamente uno scorrimento verticale.

**Proprietà CSS del &#x200B;** del corpo della finestra di dialogo

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
.s7smartcropvideoviewer .s7embeddialog .s7dialogbody { 
    padding: 10px; 
}
```

Tutte le etichette statiche nel modulo della finestra di dialogo sono controllate da

```
.s7smartcropvideoviewer .s7embeddialog .s7dialoglabel
```

Questa classe non è adatta per controllare la dimensione o la posizione dell&#39;etichetta perché può essere applicata a testi in varie posizioni dell&#39;interfaccia utente del modulo.

**Proprietà CSS dell&#39;etichetta della finestra di dialogo. &#x200B;**

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
   <td colname="col1"> <p> <span class="codeph"> famiglia di caratteri </span> </p> </td> 
   <td colname="col2"> <p>Famiglia font etichetta. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> colore </span> </p> </td> 
   <td colname="col2"> <p>Colore testo etichetta. </p> </td> 
  </tr> 
 </tbody> 
</table>

Le descrizioni comandi delle etichette delle finestre di dialogo possono essere localizzate. Per ulteriori informazioni, vedere [Localizzazione degli elementi dell&#39;interfaccia utente](../../../c-html5-aem-asset-viewers/c-html5-aem-smartcropvideo/r-html5-aem-smartcropvideo-viewer-localization.md#concept-1d5ca2d8480f4064a51eddba13940aad).

Esempio: per impostare tutte le etichette come grigie, in grassetto con un carattere di nove pixel:

```
.s7smartcropvideoviewer .s7embeddialog .s7dialoglabel { 
    color: #666666; 
    font-size: 9pt; 
    font-weight: bold; 
}
```

La dimensione della copia di testo visualizzata sopra il codice di incorporamento è controllata con il seguente selettore di classe CSS:

```
.s7smartcropvideoviewer .s7embeddialog .s7dialoginputwide
```

**Proprietà CSS del campo a livello di input della finestra di dialogo**

<table id="table_7275B4365DFA4C0386FA2BDB7204A517"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> larghezza </span> </p> </td> 
   <td colname="col2"> <p>Larghezza campo di input. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> riempimento </span> </p> </td> 
   <td colname="col2"> <p>Spaziatura interna. </p> </td> 
  </tr> 
 </tbody> 
</table>

Esempio: per impostare una copia di testo larga 430 pixel e con una spaziatura di dieci pixel nella parte inferiore:

```
.s7smartcropvideoviewer .s7embeddialog .s7dialoginputwide { 
    padding-bottom: 10px; 
    width: 430px; 
}
```

Il codice di incorporamento viene racchiuso nel contenitore e controllato con il seguente selettore di classe CSS:

```
.s7smartcropvideoviewer .s7embeddialog .s7dialoginputcontainer
```

**Proprietà CSS del contenitore di input della finestra di dialogo**

<table id="table_7BC1C5919A54483F8121D928DC63233A"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> larghezza </span> </p> </td> 
   <td colname="col2"> <p>Larghezza del contenitore del codice di incorporamento. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> bordo </span> </p> </td> 
   <td colname="col2"> <p>Bordo intorno al contenitore del codice di incorporamento. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> riempimento </span> </p> </td> 
   <td colname="col2"> <p>Spaziatura interna. </p> </td> 
  </tr> 
 </tbody> 
</table>

Esempio: per impostare un bordo grigio di un pixel attorno al testo del codice da incorporare, impostalo con una larghezza di 430 pixel e una spaziatura di dieci pixel:

```
.s7smartcropvideoviewer .s7embeddialog .s7dialoginputcontainer { 
    border: 1px solid #CCCCCC; 
    padding: 10px; 
    width: 430px; 
}
```

Il testo effettivo del codice di incorporamento è controllato con il seguente selettore di classe CSS:

```
.s7smartcropvideoviewer .s7embeddialog .s7dialoginputcontainer
```

**Proprietà CSS del contenitore di input della finestra di dialogo**

<table id="table_FEEF66150C69489BB42A2408EBFCE928"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ritorno a capo automatico </span> </p> </td> 
   <td colname="col2"> <p>Stile a capo automatico. </p> </td> 
  </tr> 
 </tbody> 
</table>

Esempio - Per impostare il codice di incorporamento per l&#39;utilizzo del ritorno a capo automatico `break-word`:

```
.s7smartcropvideoviewer .s7embeddialog .s7dialogmessage { 
    word-wrap: break-word; 
}
```

L’etichetta della dimensione di incorporamento e l’elenco a discesa si trovano nella parte inferiore della finestra di dialogo e vengono inseriti in un contenitore controllato con il seguente selettore di classe CSS:

```
.s7smartcropvideoviewer .s7embeddialog .s7dialogembedsizepanel
```

**Proprietà CSS del pannello dimensioni incorporamento della finestra di dialogo**

<table id="table_6BA2769361BA4EC4AB7D250EC9486CB2"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> riempimento </span> </p> </td> 
   <td colname="col2"> <p>Spaziatura interna. </p> </td> 
  </tr> 
 </tbody> 
</table>

Esempio: per impostare un pannello di dimensioni da incorporare con dieci pixel di spaziatura interna:

```
.s7smartcropvideoviewer .s7embeddialog .s7dialogembedsizepanel { 
    padding: 10px; 
}
```

Le dimensioni e l’allineamento dell’etichetta delle dimensioni di incorporamento sono controllati con il seguente selettore di classe CSS:

```
.s7smartcropvideoviewer .s7embeddialog .s7dialogembedsizepanel
```

**Proprietà CSS del pannello dimensioni incorporamento della finestra di dialogo**

<table id="table_8E50C63C9B1349999251CDB5E5AD3D1D"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> allineamento verticale </span> </p> </td> 
   <td colname="col2"> <p>Allineamento verticale delle etichette. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> larghezza </span> </p> </td> 
   <td colname="col2"> <p>Larghezza etichetta. </p> </td> 
  </tr> 
 </tbody> 
</table>

Esempio: per impostare l’etichetta della dimensione di incorporamento in modo che sia allineata in alto e larga 80 pixel:

```
.s7smartcropvideoviewer .s7embeddialog .s7dialogembedsizelabel { 
    vertical-align: top; 
    width: 80px; 
}
```

La larghezza della casella combinata Dimensione incorporamento è controllata dal seguente selettore di classe CSS:

```
.s7smartcropvideoviewer .s7embeddialog .s7combobox
```

**Proprietà CSS della casella combinata**

<table id="table_C0FEA0C7353F40039204641BB3F1AE14"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> larghezza </span> </p> </td> 
   <td colname="col2"> <p>Larghezza casella combinata. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>La casella combinata supporta il selettore di attributi `expanded` con valori possibili di `true` e `false`. Il valore `true` viene utilizzato quando la casella combinata visualizza una delle dimensioni di incorporamento predefinite, pertanto dovrebbe occupare tutta la larghezza disponibile. Il valore `false` viene utilizzato quando nella casella combinata è selezionata l&#39;opzione di dimensione personalizzata, pertanto deve essere ridotto per consentire lo spazio per i campi di input personalizzati per larghezza e altezza.

Esempio: per impostare la casella combinata Dimensione incorporamento su una larghezza di 300 pixel quando si visualizza un elemento predefinito e su una larghezza di 110 pixel quando si visualizza una dimensione personalizzata:

```
.s7smartcropvideoviewer .s7embeddialog .s7combobox[expanded="true"] { 
    width: 300px; 
} 
.s7smartcropvideoviewer .s7embeddialog .s7combobox[expanded="false"] { 
    width: 110px; 
}
```

L’altezza del testo della casella combinata è definita da un elemento interno speciale ed è controllata dal seguente selettore di classe CSS:

```
.s7smartcropvideoviewer .s7embeddialog .s7combobox .s7comboboxtext
```

**Proprietà CSS del testo della casella combinata**

<table id="table_AB60032BF337433F8455DE20AFBA29AB"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> altezza </span> </p> </td> 
   <td colname="col2"> <p>Altezza testo casella combinata. </p> </td> 
  </tr> 
 </tbody> 
</table>

Esempio - per impostare su 40 pixel l&#39;altezza del testo della casella combinata delle dimensioni di incorporamento:

```
.s7smartcropvideoviewer .s7embeddialog .s7combobox .s7comboboxtext { 
    height: 40px; 
}
```

La casella combinata ha un pulsante &quot;a discesa&quot; a destra ed è controllata dal seguente selettore di classe CSS:

```
.s7smartcropvideoviewer .s7embeddialog .s7combobox .s7comboboxbutton
```

**Proprietà CSS del pulsante Casella combinata**

<table id="table_70E127FA21264366AD5DBBD7DF40EBAA"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> primi </span> </p> </td> 
   <td colname="col2"> <p>Posizione del pulsante verticale all'interno della casella combinata. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> a destra </span> </p> </td> 
   <td colname="col2"> <p>Posizione orizzontale del pulsante all'interno della casella combinata. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> larghezza </span> </p> </td> 
   <td colname="col2"> <p>Larghezza pulsante. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> altezza </span> </p> </td> 
   <td colname="col2"> <p>Altezza pulsante. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> immagine di sfondo </span> </p> </td> 
   <td colname="col2"> <p>Immagine pulsante per ogni stato. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> Posizionate all'interno dello sprite del disegno, se vengono utilizzati gli sprite CSS. </p> <p>Vedere <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-smartcropvideo/c-html5-aem-smartcropvideo-viewer-customizingviewer/c-html5-aem-smartcropvideo-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> sprite CSS </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

Questo pulsante supporta il selettore di attributi `state`, che può essere utilizzato per applicare interfacce diverse a diversi stati di pulsante.

Esempio: per impostare un pulsante &quot;a discesa&quot; su 28 x 28 pixel e avere un’immagine separata per ogni stato:

```
.s7smartcropvideoviewer .s7embeddialog .s7combobox .s7comboboxbutton { 
 width:28px; 
 height:28px; 
} 
.s7smartcropvideoviewer .s7embeddialog .s7combobox .s7comboboxbutton[state='up'] { 
 background-image:url(images/sdk/cboxbtndn_up.png); 
} 
.s7smartcropvideoviewer .s7embeddialog .s7combobox .s7comboboxbutton[state='over'] { 
 background-image:url(images/sdk/cboxbtndn_over.png); 
} 
.s7smartcropvideoviewer .s7embeddialog .s7combobox .s7comboboxbutton[state='down'] { 
 background-image:url(images/sdk/cboxbtndn_over.png); 
} 
.s7smartcropvideoviewer .s7embeddialog .s7combobox .s7comboboxbutton[state='disabled'] { 
 background-image:url(images/sdk/cboxbtndn_up.png); 
}
```

Il pannello con l’elenco delle dimensioni di incorporamento visualizzate all’apertura della casella combinata è controllato dal seguente selettore di classe CSS:

```
.s7smartcropvideoviewer .s7embeddialog .s7comboboxdropdown
```

Le dimensioni e la posizione del pannello sono controllate dal componente. Non è possibile modificarlo tramite CSS.

**Proprietà CSS del menu a discesa della casella combinata**

<table id="table_FA7345321C6A4E63B4B78ECF81CE18DB"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> bordo </span> </p> </td> 
   <td colname="col2"> <p>Bordo del pannello. </p> </td> 
  </tr> 
 </tbody> 
</table>

Esempio: per impostare il pannello della casella combinata su un bordo grigio di un pixel:

```
.s7smartcropvideoviewer .s7embeddialog .s7comboboxdropdown { 
    border: 1px solid #CCCCCC; 
}
```

Un singolo elemento in un pannello a discesa controllato con il seguente selettore di classe CSS:

```
.s7smartcropvideoviewer .s7embeddialog .s7dropdownitemanchor
```

**Proprietà CSS dell&#39;ancoraggio elemento a discesa**

<table id="table_FD42FDD56F89463A97FD292FAA04DA5A"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> colore di sfondo </span> </p> </td> 
   <td colname="col2"> <p>Sfondo elemento. </p> </td> 
  </tr> 
 </tbody> 
</table>

Esempio: per impostare l&#39;elemento del pannello della casella combinata su uno sfondo bianco:

```
.s7smartcropvideoviewer .s7embeddialog .s7dropdownitemanchor { 
    background-color: #FFFFFF; 
}
```

Un segno di spunta visualizzato a sinistra dell’elemento selezionato all’interno del pannello della casella combinata controllato con il seguente selettore di classe CSS:

```
.s7smartcropvideoviewer .s7embeddialog .s7checkmark
```

**Proprietà CSS della casella segno di spunta**

<table id="table_8E01F5461CD04AC18B2C3725A961476A"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> larghezza </span> </p> </td> 
   <td colname="col2"> <p>Larghezza icona. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> altezza </span> </p> </td> 
   <td colname="col2"> <p>Altezza icona. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> immagine di sfondo </span> </p> </td> 
   <td colname="col2"> <p>Immagine dell'elemento. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> Posizionate all'interno dello sprite del disegno, se vengono utilizzati gli sprite CSS. </p> <p>Vedere <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-smartcropvideo/c-html5-aem-smartcropvideo-viewer-customizingviewer/c-html5-aem-smartcropvideo-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> sprite CSS </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

Esempio - per impostare l&#39;icona del segno di spunta su 25 x 25 pixel:

```
.s7smartcropvideoviewer .s7embeddialog .s7checkmark { 
    background-image: url("images/sdk/cboxchecked.png"); 
    height: 25px; 
    width: 25px; 
}
```

Quando l&#39;opzione &quot;Dimensioni personalizzate&quot; è selezionata nella casella combinata Dimensione incorporamento, la finestra di dialogo visualizza due campi di input aggiuntivi a destra per consentire all&#39;utente di immettere una dimensione di incorporamento personalizzata. Tali campi sono racchiusi in un contenitore controllato con il seguente selettore di classe CSS:

```
.s7smartcropvideoviewer .s7embeddialog .s7dialogcustomsizepanel
```

**Proprietà CSS del pannello dimensioni personalizzate della finestra di dialogo**

<table id="table_B00829EA550F4E5E8F51B1C6ADACCD34"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ha lasciato </span> </p> </td> 
   <td colname="col2"> <p> Distanza dalla casella combinata dimensione incorporamento. </p> </td> 
  </tr> 
 </tbody> 
</table>

Esempio: per impostare la dimensione personalizzata del pannello dei campi di input su 20 pixel a destra della casella combinata:

```
.s7smartcropvideoviewer .s7embeddialog .s7dialogcustomsizepanel { 
    left: 20px; 
}
```

Ogni campo di input delle dimensioni personalizzate viene racchiuso in un contenitore che esegue il rendering di un bordo e imposta il margine tra i campi. Viene controllata con il seguente selettore di classe CSS:

```
.s7smartcropvideoviewer .s7embeddialog .s7dialogcustomsize
```

**Proprietà CSS della finestra di dialogo dimensione personalizzata**

<table id="table_A8A04BE1988641618D0A412B8AEEE1C5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> bordo </span> </p> </td> 
   <td colname="col2"> <p>Bordo intorno al campo di input. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> larghezza </span> </p> </td> 
   <td colname="col2"> <p> Larghezza campo di input. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margine </span> </p> </td> 
   <td colname="col2"> <p> Margine campo di input. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> riempimento </span> </p> </td> 
   <td colname="col2"> <p> Spaziatura interna campo di input. </p> </td> 
  </tr> 
 </tbody> 
</table>

Esempio: per impostare le dimensioni personalizzate dei campi di input in modo che abbiano un bordo, un margine, una spaziatura interna di un pixel e una larghezza di 70 pixel:

```
.s7smartcropvideoviewer .s7embeddialog .s7dialogcustomsize { 
    border: 1px solid #CCCCCC; 
    margin-right: 20px; 
    padding-left: 2px; 
    padding-right: 2px; 
    width: 70px; 
}
```

Se è necessario lo scorrimento verticale, la barra di scorrimento viene rappresentata nel pannello accanto al bordo destro della finestra di dialogo, che è controllata dal seguente selettore di classe CSS:

```
.s7smartcropvideoviewer .s7embeddialog .s7dialogscrollpanel
```

**Proprietà CSS del pannello di scorrimento della finestra di dialogo**

<table id="table_BA37E577E0884C919383F84080E2DD28"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> larghezza </span> </p> </td> 
   <td colname="col2"> <p>Larghezza pannello di scorrimento. </p> </td> 
  </tr> 
 </tbody> 
</table>

Esempio: per impostare una larghezza di 44 pixel per il pannello di scorrimento

```
.s7smartcropvideoviewer .s7embeddialog .s7dialogscrollpanel { 
    width: 44px; 
}
```

L’aspetto dell’area della barra di scorrimento è controllato dal seguente selettore di classe CSS:

```
.s7smartcropvideoviewer .s7embeddialog .s7scrollbar
```

**Proprietà CSS della barra di scorrimento**

<table id="table_066492417FCA43929017993D7326CDB8"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> larghezza </span> </p> </td> 
   <td colname="col2"> <p>Larghezza barra di scorrimento. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> primi </span> </p> </td> 
   <td colname="col2"> <p> Scostamento della barra di scorrimento verticale dalla parte superiore del pannello di scorrimento. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> in basso </span> </p> </td> 
   <td colname="col2"> <p> Scostamento della barra di scorrimento verticale dalla parte inferiore del pannello di scorrimento. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> a destra </span> </p> </td> 
   <td colname="col2"> <p> Scostamento della barra di scorrimento orizzontale dal bordo destro del pannello di scorrimento. </p> </td> 
  </tr> 
 </tbody> 
</table>

Esempio: per impostare una barra di scorrimento larga 28 pixel con un margine di otto pixel dall’alto, dal basso e dal destro del pannello di scorrimento:

```
.s7smartcropvideoviewer .s7embeddialog .s7scrollbar { 
    bottom: 8px; 
    right: 8px; 
    top: 8px; 
    width: 28px; 
}
```

La traccia della barra di scorrimento è l&#39;area compresa tra i pulsanti di scorrimento superiore e inferiore. Il componente imposta automaticamente la posizione e l&#39;altezza della traccia. Il brano è controllato con il seguente selettore di classe CSS

```
.s7smartcropvideoviewer .s7embeddialog .s7scrollbar .s7scrolltrack
```

**Proprietà CSS del brano della barra di scorrimento**

<table id="table_19CF5503C1D34ED9998D4F4A6DA7D5D5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> larghezza </span> </p> </td> 
   <td colname="col2"> <p>Larghezza del binario. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> colore di sfondo </span> </p> </td> 
   <td colname="col2"> <p> Tracciare il colore di sfondo. </p> </td> 
  </tr> 
 </tbody> 
</table>

Esempio: per impostare una traccia della barra di scorrimento larga 28 pixel e con sfondo grigio:

```
.s7smartcropvideoviewer .s7embeddialog .s7scrollbar .s7scrolltrack { 
width:28px; 
background-color: #B2B2B2; 
}
```

Il pollice della barra di scorrimento si sposta verticalmente all&#39;interno dell&#39;area della traccia di scorrimento. La sua posizione verticale è completamente controllata dalla logica del componente. Tuttavia, l’altezza del pollice non cambia in modo dinamico a seconda della quantità di contenuto. L’altezza del pollice e altri aspetti possono essere configurati con il seguente selettore di classe CSS:

```
.s7smartcropvideoviewer .s7embeddialog .s7scrollbar .s7scrollthumb
```

**Proprietà CSS della barra di scorrimento**

<table id="table_90BC468FE138441C9DBAB1EB109F3DB0"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> larghezza </span> </p> </td> 
   <td colname="col2"> <p>Larghezza miniature. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> altezza </span> </p> </td> 
   <td colname="col2"> <p>Altezza miniature. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> riempimento superiore </span> </p> </td> 
   <td colname="col2"> <p>Spaziatura verticale tra la parte superiore del brano. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> riempimento inferiore </span> </p> </td> 
   <td colname="col2"> <p> Spaziatura verticale tra la parte inferiore del brano. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> immagine di sfondo </span> </p> </td> 
   <td colname="col2"> <p> Immagine visualizzata per un determinato stato del pollice. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>La miniatura supporta il selettore di attributi `state`, che può essere utilizzato per applicare interfacce diverse a diversi stati della miniatura: `up`, `down`, `over` e `disabled`.

Esempio: per impostare una barra di scorrimento di 28 x 45 pixel con un margine di dieci pixel in alto e in basso e un disegno diverso per ciascuno stato:

```
.s7smartcropvideoviewer .s7embeddialog .s7scrollbar .s7scrollthumb { 
    height: 45px; 
    padding-bottom: 10px; 
    padding-top: 10px; 
    width: 28px; 
} 
.s7smartcropvideoviewer .s7embeddialog .s7scrollbar .s7scrollthumb[state="up"] { 
 background-image:url("images/sdk/scrollbar_thumb_up.png"); 
} 
.s7smartcropvideoviewer .s7embeddialog .s7scrollbar .s7scrollthumb[state="down"] { 
 background-image:url("images/sdk/scrollbar_thumb_down.png"); 
} 
.s7smartcropvideoviewer .s7embeddialog .s7scrollbar .s7scrollthumb[state="over"] { 
 background-image:url("images/sdk/scrollbar_thumb_over.png"); 
} 
.s7smartcropvideoviewer .s7embeddialog .s7scrollbar .s7scrollthumb[state="disabled"] { 
 background-image:url("images/sdk/scrollbar_thumb_disabled.png"); 
}
```

L’aspetto dei pulsanti di scorrimento superiore e inferiore è controllato dai seguenti selettori di classi CSS:

```
.s7smartcropvideoviewer .s7embeddialog .s7scrollbar .s7scrollupbutton 
```

```
.s7smartcropvideoviewer .s7embeddialog .s7scrollbar .s7scrolldownbutton
```

Non è possibile posizionare i pulsanti di scorrimento utilizzando le proprietà CSS top, left, bottom e right. Al contrario, la logica di visualizzazione li posiziona automaticamente.

**Proprietà CSS dei pulsanti di scorrimento superiore e inferiore**

<table id="table_554BFCFEAF4F43A9AE5F741DC126F833"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> larghezza </span> </p> </td> 
   <td colname="col2"> <p>Larghezza pulsante. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> altezza </span> </p> </td> 
   <td colname="col2"> <p>Altezza pulsante. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> immagine di sfondo </span> </p> </td> 
   <td colname="col2"> <p> Immagine visualizzata per un determinato stato del pulsante. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> Posizionate all'interno dello sprite del disegno, se vengono utilizzati gli sprite CSS. </p> <p>Vedere <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-smartcropvideo/c-html5-aem-smartcropvideo-viewer-customizingviewer/c-html5-aem-smartcropvideo-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> sprite CSS </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Questi pulsanti supportano il selettore di attributi `state`, che può essere utilizzato per applicare interfacce diverse a diversi stati di pulsanti: `up`, `down`, `over` e `disabled`.

Le descrizioni dei pulsanti possono essere localizzate. Per ulteriori informazioni, vedere [Localizzazione degli elementi dell&#39;interfaccia utente](../../../c-html5-aem-asset-viewers/c-html5-aem-smartcropvideo/r-html5-aem-smartcropvideo-viewer-localization.md#concept-1d5ca2d8480f4064a51eddba13940aad).

Esempio - per impostare pulsanti di scorrimento di 28 x 32 pixel con grafica diversa per ogni stato:

```
.s7smartcropvideoviewer .s7embeddialog .s7scrollbar .s7scrollupbutton { 
 width:28px; 
 height:32px; 
} 
.s7smartcropvideoviewer .s7embeddialog .s7scrollbar .s7scrollupbutton[state='up'] { 
background-image:url(images/sdk/scroll_up_up.png); 
} 
.s7smartcropvideoviewer .s7embeddialog .s7scrollbar .s7scrollupbutton[state='over'] { 
 background-image:url(images/sdk/scroll_up_over.png); 
} 
.s7smartcropvideoviewer .s7embeddialog .s7scrollbar .s7scrollupbutton[state='down'] { 
 background-image:url(images/sdk/scroll_up_down.png); 
} 
.s7smartcropvideoviewer .s7embeddialog .s7scrollbar .s7scrollupbutton[state='disabled'] { 
 background-image:url(images/sdk/scroll_up_disabled.png); 
} 
.s7smartcropvideoviewer .s7embeddialog .s7scrollbar .s7scrolldownbutton { 
 width:28px; 
 height:32px; 
} 
.s7smartcropvideoviewer .s7embeddialog .s7scrollbar .s7scrolldownbutton[state='up'] { 
 background-image:url(images/sdk/scroll_down_up.png); 
} 
.s7smartcropvideoviewer .s7embeddialog .s7scrollbar .s7scrolldownbutton[state='over'] { 
 background-image:url(images/sdk/scroll_down_over.png); 
} 
.s7smartcropvideoviewer .s7embeddialog .s7scrollbar .s7scrolldownbutton[state='down'] { 
 background-image:url(images/sdk/scroll_down_down.png); 
} 
.s7smartcropvideoviewer .s7embeddialog .s7scrollbar .s7scrolldownbutton[state='disabled'] { 
 background-image:url(images/sdk/scroll_down_disabled.png); 
}
```
