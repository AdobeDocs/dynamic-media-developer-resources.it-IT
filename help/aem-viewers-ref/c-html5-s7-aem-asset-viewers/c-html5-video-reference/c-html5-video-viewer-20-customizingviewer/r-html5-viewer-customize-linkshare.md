---
description: Lo strumento di condivisione dei collegamenti è costituito da un pulsante aggiunto al pannello Condivisione social e dalla finestra di dialogo modale che viene visualizzata quando lo strumento viene attivato. La posizione del pulsante è completamente gestita dallo strumento di condivisione social network.
solution: Experience Manager
title: Condivisione collegamenti
feature: Dynamic Media Classic,Visualizzatori,SDK/API,Video
role: Developer,User
exl-id: a80b47fd-0399-4d0a-8c11-cfa4acc5a713
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '1382'
ht-degree: 1%

---

# Condivisione collegamenti{#link-share}

Lo strumento di condivisione dei collegamenti è costituito da un pulsante aggiunto al pannello Condivisione social e dalla finestra di dialogo modale che viene visualizzata quando lo strumento viene attivato. La posizione del pulsante è completamente gestita dallo strumento di condivisione social network.

<!--<a id="section_ADDF98E91AF24F618289D1682A5FB13A"></a>-->

L&#39;aspetto del pulsante di condivisione del collegamento è controllato con il seguente selettore di classe CSS:

```
.s7videoviewer .s7linkshare
```

**Proprietà CSS dello strumento di condivisione dei collegamenti**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Larghezza pulsante. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Altezza del pulsante. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> immagine di sfondo  </span> </p> </td> 
   <td colname="col2"> <p> Immagine visualizzata per un determinato stato del pulsante. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> posizione di sfondo  </span> </p> </td> 
   <td colname="col2"> <p> Posizione all’interno dello sprite di un’immagine, se vengono utilizzati gli spriti CSS. </p> <p>Consulta <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-customizingviewer/c-html5-video-viewer-20-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> Sprite CSS </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Questo pulsante supporta il selettore di attributi `state` , che può essere utilizzato per applicare interfacce diverse a diversi stati del pulsante.

È possibile rimuovere il pulsante dal pannello Condivisione social impostando la proprietà `display:none` CSS nella relativa classe CSS.

La descrizione comando del pulsante può essere localizzata. Per ulteriori informazioni, consulta [Localizzazione degli elementi dell’interfaccia utente](../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/r-html5-video-viewer-20-localization.md#concept-1d5ca2d8480f4064a51eddba13940aad) .

Esempio : per impostare un pulsante di condivisione del collegamento che sia di 28 x 28 pixel e visualizzare un’immagine diversa per ciascuno dei quattro stati diversi del pulsante:

```
.s7videoviewer .s7linkshare { 
 width:28px; 
 height:28px; 
} 
.s7videoviewer .s7linkshare[state='up'] { 
background-image:url(images/v2/LinkShare_dark_up.png); 
} 
.s7videoviewer .s7linkshare[state='over'] { 
background-image:url(images/v2/LinkShare_dark_over.png); 
} 
.s7videoviewer .s7linkshare[state='down'] { 
background-image:url(images/v2/LinkShare_dark_down.png); 
} 
.s7videoviewer .s7linkshare[state='disabled'] { 
background-image:url(images/v2/LinkShare_dark_disabled.png); 
}
```

La sovrapposizione di sfondo che copre la pagina web quando la finestra di dialogo è attiva è controllata con il seguente selettore di classe CSS:

```
.s7videoviewer .s7linkdialog .s7backoverlay
```

**Proprietà CSS della sovrapposizione di sfondo**

<table id="table_DB4183CE8061425084D495A355A941F8"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> opacità  </span> </p> </td> 
   <td colname="col2"> <p>Opacità sovrapposizione sfondo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> colore di sfondo  </span> </p> </td> 
   <td colname="col2"> <p>Colore sovrapposizione sfondo. </p> </td> 
  </tr> 
 </tbody> 
</table>

Esempio: per impostare una sovrapposizione di sfondo grigio con opacità del 70%:

```
.s7videoviewer .s7linkdialog .s7backoverlay { 
 opacity:0.7; 
 background-color:#222222; 
}
```

Per impostazione predefinita, la finestra di dialogo modale viene visualizzata centrata sullo schermo sui sistemi desktop e occupa l’intera area della pagina web sui dispositivi touch. In tutti i casi, il posizionamento e il dimensionamento della finestra di dialogo vengono gestiti dal componente. La finestra di dialogo viene controllata con il seguente selettore di classe CSS:

```
.s7videoviewer .s7linkdialog .s7dialog
```

**Proprietà CSS della finestra di dialogo**

<table id="table_E31711ADF4C7446182549244362199A3"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> raggio bordo  </span> </p> </td> 
   <td colname="col2"> <p> Raggio del bordo della finestra di dialogo, nel caso in cui la finestra di dialogo non utilizzi l’intero browser. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> colore di sfondo  </span> </p> </td> 
   <td colname="col2"> <p>Colore di sfondo della finestra di dialogo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> larghezza  </span> </p> </td> 
   <td colname="col2"> <p>Deve essere disattivato o impostato su 100%, nel qual caso la finestra di dialogo prende l’intera finestra del browser (questa modalità è preferita per i dispositivi touch). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> altezza  </span> </p> </td> 
   <td colname="col2"> <p>Deve essere disattivato o impostato su 100%, nel qual caso la finestra di dialogo prende l’intera finestra del browser (questa modalità è preferita per i dispositivi touch). </p> </td> 
  </tr> 
 </tbody> 
</table>

Esempio: per impostare la finestra di dialogo in modo che utilizzi l’intera finestra del browser e che abbia uno sfondo bianco sui dispositivi touch:

```
.s7videoviewer .s7touchinput .s7linkdialog .s7dialog { 
 width:100%; 
 height:100%; 
background-color: #ffffff; 
}
```

L’intestazione della finestra di dialogo è costituita da un’icona, un testo del titolo e un pulsante Chiudi. Il contenitore di intestazione è controllato con

```
.s7videoviewer .s7linkdialog .s7dialogheader
```

**Proprietà CSS dell’intestazione della finestra di dialogo**

<table id="table_E407E844C9BD4B5DA8B5BBDE0554F9CA"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> spaziatura interna  </span> </p> </td> 
   <td colname="col2"> <p> Spaziatura interna per il contenuto dell’intestazione. </p> </td> 
  </tr> 
 </tbody> 
</table>

L’icona e il testo del titolo vengono racchiusi in un contenitore aggiuntivo controllato con

```
.s7videoviewer .s7linkdialog .s7dialogheader .s7dialogline
```

**Proprietà CSS della riga di dialogo**

<table id="table_5B03CF843F0D4B1295A3FC1EB50C56F1"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> spaziatura interna  </span> </p> </td> 
   <td colname="col2"> <p> Spaziatura interna per l’icona dell’intestazione e il titolo </p> </td> 
  </tr> 
 </tbody> 
</table>

L’icona Intestazione è controllata dal seguente selettore di classe CSS

```
.s7videoviewer .s7linkdialog .s7dialogheadericon
```

**Proprietà CSS dell’icona di intestazione della finestra di dialogo**

<table id="table_DD4B0413721B49CE8E21B4A55BDE8F7D"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> larghezza  </span> </p> </td> 
   <td colname="col2"> <p>Larghezza icona. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> altezza  </span> </p> </td> 
   <td colname="col2"> <p>Altezza icona. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> immagine di sfondo  </span> </p> </td> 
   <td colname="col2"> <p>Immagine icona. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> posizione di sfondo  </span> </p> </td> 
   <td colname="col2"> <p> Posizione all’interno dello sprite di un’immagine, se vengono utilizzati gli spriti CSS. </p> <p>Consulta <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-customizingviewer/c-html5-video-viewer-20-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> Sprite CSS </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

Il titolo dell’intestazione è controllato con il seguente selettore di classe CSS:

```
.s7videoviewer .s7linkdialog .s7dialogheadertext
```

**Proprietà CSS del testo dell’intestazione della finestra di dialogo**

<table id="table_207B4B13153E425EAB38FC61F382A05F"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-weight  </span> </p> </td> 
   <td colname="col2"> <p>Spessore del carattere. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size  </span> </p> </td> 
   <td colname="col2"> <p>Altezza carattere. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family  </span> </p> </td> 
   <td colname="col2"> <p>Famiglia di caratteri. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> spaziatura interna  </span> </p> </td> 
   <td colname="col2"> <p>Spaziatura interna del testo. </p> </td> 
  </tr> 
 </tbody> 
</table>

Il pulsante Chiudi è controllato con il seguente selettore di classe CSS:

```
.s7videoviewer .s7linkdialog .s7closebutton
```

**Proprietà CSS del pulsante di chiusura **

<table id="table_FAECBC489FC442588E50E3DA0AC16DD7"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> top  </span> </p> </td> 
   <td colname="col2"> <p> Posizione del pulsante verticale rispetto al contenitore di intestazione. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> right  </span> </p> </td> 
   <td colname="col2"> <p> Posizione del pulsante orizzontale rispetto al contenitore intestazione. </p> </td> 
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
   <td colname="col1"> <p> <span class="codeph"> spaziatura interna  </span> </p> </td> 
   <td colname="col2"> <p>Spaziatura interna del pulsante. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> immagine di sfondo  </span> </p> </td> 
   <td colname="col2"> <p>Immagine pulsante per ogni stato. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> posizione di sfondo  </span> </p> </td> 
   <td colname="col2"> <p> Posizione all’interno dello sprite di un’immagine, se vengono utilizzati gli spriti CSS. </p> <p>Consulta <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-customizingviewer/c-html5-video-viewer-20-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> Sprite CSS </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Questo pulsante supporta il selettore di attributi `state` , che può essere utilizzato per applicare interfacce diverse a diversi stati del pulsante.

È possibile localizzare la descrizione del pulsante Chiudi e il titolo della finestra di dialogo. Per ulteriori informazioni, consulta [Localizzazione degli elementi dell’interfaccia utente](../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/r-html5-video-viewer-20-localization.md#concept-1d5ca2d8480f4064a51eddba13940aad) .

Esempio: per impostare un’intestazione della finestra di dialogo con spaziatura, l’icona 22 x 12 pixel, il titolo in grassetto a 16 punti e un pulsante Chiudi a 28 x 28 pixel posizionato due pixel dalla parte superiore e due pixel dalla parte destra del contenitore della finestra di dialogo:

```
.s7videoviewer .s7linkdialog .s7dialogheader { 
 padding: 10px; 
} 
.s7videoviewer .s7linkdialog .s7dialogheader .s7dialogline { 
 padding: 10px 10px 2px; 
} 
.s7videoviewer .s7linkdialog .s7dialogheadericon { 
    background-image: url("images/sdk/dlglink_cap.png"); 
    height: 12px; 
    width: 22px; 
} 
.s7videoviewer .s7linkdialog .s7dialogheadertext { 
    font-size: 16pt; 
    font-weight: bold; 
    padding-left: 16px; 
} 
.s7videoviewer .s7linkdialog .s7closebutton { 
 top:2px; 
 right:2px; 
 padding:8px; 
 width:28px; 
 height:28px; 
} 
.s7videoviewer .s7linkdialog .s7closebutton[state='up'] { 
 background-image:url(images/sdk/close_up.png); 
} 
.s7videoviewer .s7linkdialog .s7closebutton[state='over'] { 
 background-image:url(images/sdk/close_over.png); 
} 
.s7videoviewer .s7linkdialog .s7closebutton[state='down'] { 
 background-image:url(images/sdk/close_down.png); 
} 
.s7videoviewer .s7linkdialog .s7closebutton[state='disabled'] { 
 background-image:url(images/sdk/close_disabled.png); 
}
```

Il piè di pagina della finestra di dialogo è costituito dal pulsante &quot;Annulla&quot;. Il contenitore piè di pagina è controllato con il seguente selettore di classe CSS:

```
.s7videoviewer .s7linkdialog .s7dialogfooter
```

**Proprietà CSS del piè di pagina della finestra di dialogo **

<table id="table_0AF7AAAB846A46D690896AFD68575669"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> border  </span> </p> </td> 
   <td colname="col2"> <p> Bordo che è possibile utilizzare per separare visivamente il piè di pagina dal resto della finestra di dialogo. </p> </td> 
  </tr> 
 </tbody> 
</table>

Il piè di pagina dispone di un contenitore interno che mantiene il pulsante. È controllato con il seguente selettore di classe CSS:

```
.s7videoviewer .s7linkdialog .s7dialogbuttoncontainer
```

**Proprietà CSS del contenitore pulsanti della finestra di dialogo**

<table id="table_C34906888A8145C7A61E503DFC6B08A9"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> spaziatura interna  </span> </p> </td> 
   <td colname="col2"> <p> Spaziatura interna tra il piè di pagina e il pulsante. </p> </td> 
  </tr> 
 </tbody> 
</table>

Il pulsante Seleziona tutto è controllato con il seguente selettore di classe CSS:

```
.s7videoviewer .s7linkdialog .s7dialogactionbutton
```

Il pulsante è disponibile solo sui sistemi desktop.

**Proprietà CSS del pulsante Seleziona tutto**

<table id="table_021D0467632F49FEBFDF4CF96D2D67C7"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> larghezza  </span> </p> </td> 
   <td colname="col2"> <p>Larghezza pulsante. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> altezza  </span> </p> </td> 
   <td colname="col2"> <p>Altezza del pulsante. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color </span> </p> </td> 
   <td colname="col2"> <p> Colore del testo del pulsante per ogni stato. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> colore di sfondo  </span> </p> </td> 
   <td colname="col2"> <p> Colore di sfondo del pulsante per ogni stato. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Il pulsante Seleziona tutto supporta il selettore di attributi `state` , che può essere utilizzato per applicare interfacce diverse a diversi stati del pulsante.

Il pulsante Annulla è controllato con il seguente selettore di classe CSS:

```
.s7videoviewer .s7linkdialog .s7dialogcancelbutton
```

**Proprietà CSS del pulsante Annulla della finestra di dialogo**

<table id="table_3DFA90B012F345A3A2A123D6856BE08A"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> larghezza  </span> </p> </td> 
   <td colname="col2"> <p>Larghezza pulsante. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> altezza  </span> </p> </td> 
   <td colname="col2"> <p>Altezza del pulsante. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color  </span> </p> </td> 
   <td colname="col2"> <p> Colore del testo del pulsante per ogni stato. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> colore di sfondo  </span> </p> </td> 
   <td colname="col2"> <p> Colore di sfondo del pulsante per ogni stato. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Questo pulsante supporta il selettore di attributi `state` , che può essere utilizzato per applicare interfacce diverse a diversi stati del pulsante.

Inoltre, entrambi i pulsanti condividono la stessa classe CSS comune che può contenere impostazioni CSS uguali per altri pulsanti della finestra di dialogo:

```
.s7videoviewer .s7linkdialog .s7dialogfooter .s7button
```

**Proprietà CSS del pulsante**

<table id="table_E735E5EDFC1E4F8A962CEA533A88DD4E"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-weight  </span> </p> </td> 
   <td colname="col2"> <p>Spessore font pulsante. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size  </span> </p> </td> 
   <td colname="col2"> <p>Dimensione del font del pulsante. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family  </span> </p> </td> 
   <td colname="col2"> <p>Famiglia di font per pulsanti. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> altezza riga  </span> </p> </td> 
   <td colname="col2"> <p> Altezza del testo all’interno del pulsante. Interessa l’allineamento verticale. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ombra  </span> </p> </td> 
   <td colname="col2"> <p>Ombra esterna. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margine destro  </span> </p> </td> 
   <td colname="col2"> <p>Margine del pulsante destro. </p> </td> 
  </tr> 
 </tbody> 
</table>

Le descrizioni dei pulsanti possono essere localizzate. Per ulteriori informazioni, consulta [Localizzazione degli elementi dell’interfaccia utente](../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/r-html5-video-viewer-20-localization.md#concept-1d5ca2d8480f4064a51eddba13940aad) .

Esempio: per impostare un piè di pagina di una finestra di dialogo con un pulsante Annulla 64 x 34, il cui colore di testo e sfondo sono diversi per ogni stato del pulsante:

```
.s7videoviewer .s7linkdialog .s7dialogfooter { 
    border-top: 1px solid #909090; 
} 
.s7videoviewer .s7linkdialog .s7dialogbuttoncontainer { 
    padding-bottom: 6px; 
    padding-top: 10px; 
} 
.s7videoviewer .s7linkdialog .s7dialogfooter .s7button { 
    box-shadow: 1px 1px 1px #999999; 
    color: #FFFFFF; 
    font-size: 9pt; 
    font-weight: bold; 
    line-height: 34px; 
    margin-right: 10px; 
} 
.s7videoviewer .s7linkdialog .s7dialogcancelbutton { 
 width:64px; 
 height:34px; 
} 
.s7videoviewer .s7linkdialog .s7dialogcancelbutton[state='up'] { 
 background-color:#666666; 
 color:#dddddd; 
} 
.s7videoviewer .s7linkdialog .s7dialogcancelbutton[state='down'] { 
 background-color:#555555; 
 color:#ffffff; 
} 
.s7videoviewer .s7linkdialog .s7dialogcancelbutton[state='over'] { 
 background-color:#555555; 
 color:#ffffff; 
} 
.s7videoviewer .s7linkdialog .s7dialogcancelbutton[state='disabled'] { 
 background-color:#b2b2b2; 
 color:#dddddd; 
} 
.s7videoviewer .s7linkdialog .s7dialogactionbutton { 
 width:82px; 
 height:34px; 
} 
.s7videoviewer .s7linkdialog .s7dialogactionbutton[state='up'] { 
 background-color:#333333; 
 color:#dddddd; 
} 
.s7videoviewer .s7linkdialog .s7dialogactionbutton[state='down'] { 
 background-color:#222222; 
 color:#cccccc; 
} 
.s7videoviewer .s7linkdialog .s7dialogactionbutton[state='over'] { 
 background-color:#222222; 
 color:#cccccc; 
} 
.s7videoviewer .s7linkdialog .s7dialogactionbutton[state='disabled'] { 
 background-color:#b2b2b2; 
 color:#dddddd; 
}
```

L’area della finestra di dialogo principale (tra l’intestazione e il piè di pagina) contiene il contenuto della finestra di dialogo. In tutti i casi, il componente gestisce la larghezza dell’area, non è possibile impostarla in CSS. L’area di dialogo principale è controllata dal seguente selettore di classe CSS:

```
.s7videoviewer .s7linkdialog .s7dialogviewarea
```

**Proprietà CSS dell’area di visualizzazione della finestra di dialogo **

<table id="table_3FF4691D848A4C4D8EF060B7E79DEEDE"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> altezza  </span> </p> </td> 
   <td colname="col2"> <p> Altezza dell'area della finestra di dialogo principale. Deve essere specificato solo quando la finestra di dialogo funziona in modalità desktop. Non è applicabile quando la finestra di dialogo viene ridimensionata in modo da occupare l’intera finestra del browser. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> colore di sfondo  </span> </p> </td> 
   <td colname="col2"> <p>Colore di sfondo dell'area della finestra di dialogo principale. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margine  </span> </p> </td> 
   <td colname="col2"> <p>Margine esterno. </p> </td> 
  </tr> 
 </tbody> 
</table>

Esempio: per impostare un’area della finestra di dialogo principale su un’altezza di 300 pixel, avere un margine di dieci pixel e utilizzare uno sfondo bianco:

```
.s7videoviewer .s7linkdialog .s7dialogviewarea { 
 background-color:#ffffff; 
 margin:10px; 
 height:300px; 
}
```

Tutto il contenuto del modulo (come etichette e campi di input) risiede all’interno di un contenitore controllato con

```
.s7videoviewer .s7linkdialog .s7dialogbody
```

**Proprietà CSS del corpo della finestra di dialogo **

<table id="table_5D77F3D5B8CD4B798AA85F722B277F56"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> spaziatura interna  </span> </p> </td> 
   <td colname="col2"> <p>Spaziatura interna. </p> </td> 
  </tr> 
 </tbody> 
</table>

Esempio: per impostare il contenuto del modulo con una spaziatura di dieci pixel:

```
.s7videoviewer .s7linkdialog .s7dialogbody { 
    padding: 10px; 
}
```

Tutte le etichette statiche nel modulo della finestra di dialogo vengono controllate con

```
.s7videoviewer .s7linkdialog .s7dialoglabel
```

Questa classe non è adatta per controllare la dimensione o la posizione dell&#39;etichetta perché è possibile applicarla a testi in varie posizioni dell&#39;interfaccia utente del modulo.

**Proprietà CSS dell’etichetta della finestra di dialogo. **

<table id="table_13C7874807314ADD83A23075ABB4C340"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-weight  </span> </p> </td> 
   <td colname="col2"> <p>Etichettare lo spessore del font. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size  </span> </p> </td> 
   <td colname="col2"> <p>Etichettare le dimensioni del font. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family  </span> </p> </td> 
   <td colname="col2"> <p>Famiglia di font etichetta. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color  </span> </p> </td> 
   <td colname="col2"> <p>Colore testo etichetta. </p> </td> 
  </tr> 
 </tbody> 
</table>

Le etichette della finestra di dialogo possono essere localizzate. Per ulteriori informazioni, consulta [Localizzazione degli elementi dell’interfaccia utente](../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/r-html5-video-viewer-20-localization.md#concept-1d5ca2d8480f4064a51eddba13940aad) .

Esempio: per impostare tutte le etichette in modo che siano grigie, in grassetto con un carattere di nove pixel:

```
.s7videoviewer .s7linkdialog .s7dialoglabel { 
    color: #666666; 
    font-size: 9pt; 
    font-weight: bold; 
}
```

La dimensione della copia di testo visualizzata sopra il collegamento è controllata dal seguente selettore di classe CSS:

```
.s7videoviewer .s7linkdialog .s7dialoginputwide
```

**Proprietà CSS del campo di input a livello di finestra di dialogo**

<table id="table_7275B4365DFA4C0386FA2BDB7204A517"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> larghezza  </span> </p> </td> 
   <td colname="col2"> <p>Larghezza del testo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> spaziatura interna  </span> </p> </td> 
   <td colname="col2"> <p>Spaziatura interna. </p> </td> 
  </tr> 
 </tbody> 
</table>

Esempio: per impostare una copia di testo con una larghezza di 430 pixel e una spaziatura di dieci pixel nella parte inferiore:

```
.s7videoviewer .s7linkdialog .s7dialoginputwide { 
    padding-bottom: 10px; 
    width: 430px; 
}
```

Il collegamento di condivisione viene racchiuso in un contenitore e controllato con il seguente selettore di classe CSS:

```
.s7videoviewer .s7linkdialog .s7dialoginputcontainer
```

**Proprietà CSS del contenitore di input della finestra di dialogo**

<table id="table_7BC1C5919A54483F8121D928DC63233A"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> border  </span> </p> </td> 
   <td colname="col2"> <p>Bordo intorno al contenitore di collegamento di condivisione. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> spaziatura interna  </span> </p> </td> 
   <td colname="col2"> <p>Spaziatura interna. </p> </td> 
  </tr> 
 </tbody> 
</table>

Esempio: per impostare un bordo grigio di un pixel intorno al testo del codice da incorporare e avere nove pixel di spaziatura:

```
.s7videoviewer .s7linkdialog .s7dialoginputcontainer { 
    border: 1px solid #CCCCCC; 
    padding: 9px; 
}
```

Il collegamento di condivisione stesso è controllato con il seguente selettore di classe CSS:

```
.s7videoviewer .s7linkdialog .s7dialoglink
```

**Proprietà CSS del collegamento di condivisione finestra di dialogo**

<table id="table_65CF778F5BDA45118208538DCBE203FB"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> larghezza  </span> </p> </td> 
   <td colname="col2"> <p>Condividi la larghezza del collegamento. </p> </td> 
  </tr> 
 </tbody> 
</table>

Esempio: per impostare il collegamento di condivisione su una larghezza di 450 pixel:

```
.s7videoviewer .s7linkdialog .s7dialoglink { 
    width: 450px; 
}
```
