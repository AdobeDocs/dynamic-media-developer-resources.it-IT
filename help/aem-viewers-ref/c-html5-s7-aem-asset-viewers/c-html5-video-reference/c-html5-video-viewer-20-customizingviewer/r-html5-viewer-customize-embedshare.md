---
description: Lo strumento di condivisione di incorporamento è costituito da un pulsante aggiunto al pannello Condivisione social e dalla finestra di dialogo modale visualizzata quando lo strumento viene attivato. La posizione del pulsante è completamente gestita dallo strumento di condivisione social network.
solution: Experience Manager
title: Quota di incorporamento
feature: Dynamic Media Classic,Viewers,SDK/API,Video
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '2590'
ht-degree: 1%

---


# Embed share{#embed-share}

Lo strumento di condivisione di incorporamento è costituito da un pulsante aggiunto al pannello Condivisione social e dalla finestra di dialogo modale visualizzata quando lo strumento viene attivato. La posizione del pulsante è completamente gestita dallo strumento di condivisione social network.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

L&#39;aspetto del pulsante di condivisione di incorporamento è controllato con il seguente selettore di classe CSS:

```
.s7videoviewer .s7embedshare
```

**Proprietà CSS dello strumento di condivisione incorporato**

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

Esempio: per impostare un pulsante di condivisione di incorporamento di 28 x 28 pixel e visualizzare un’immagine diversa per ciascuno dei quattro stati dei pulsanti:

```
.s7videoviewer .s7embedshare { 
 width:28px; 
 height:28px; 
} 
.s7videoviewer .s7embedshare[state='up'] { 
background-image:url(images/v2/EmbedShare_dark_up.png); 
} 
.s7videoviewer .s7embedshare[state='over'] { 
background-image:url(images/v2/EmbedShare_dark_over.png); 
} 
.s7videoviewer .s7embedshare[state='down'] { 
background-image:url(images/v2/EmbedShare_dark_down.png); 
} 
.s7videoviewer .s7embedshare[state='disabled'] { 
background-image:url(images/v2/EmbedShare_dark_disabled.png); 
}
```

La sovrapposizione di sfondo che copre la pagina web quando la finestra di dialogo è attiva è controllata con il seguente selettore di classe CSS:

```
.s7videoviewer .s7embeddialog .s7backoverlay
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
.s7videoviewer .s7embeddialog .s7backoverlay { 
 opacity:0.7; 
 background-color:#222222; 
}
```

Per impostazione predefinita, la finestra di dialogo modale viene visualizzata centrata sullo schermo sui sistemi desktop e occupa l’intera area della pagina web sui dispositivi touch. In tutti i casi, il posizionamento e il dimensionamento della finestra di dialogo vengono gestiti dal componente. La finestra di dialogo viene controllata con il seguente selettore di classe CSS:

```
.s7videoviewer .s7embeddialog .s7dialog
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
.s7videoviewer .s7touchinput .s7embeddialog .s7dialog { 
 width:100%; 
 height:100%; 
background-color: #ffffff; 
}
```

L’intestazione della finestra di dialogo è costituita da un’icona, un testo del titolo e un pulsante Chiudi. Il contenitore di intestazione è controllato con

```
.s7videoviewer .s7embeddialog .s7dialogheader
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
.s7videoviewer .s7embeddialog .s7dialogheader .s7dialogline
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
.s7videoviewer .s7embeddialog .s7dialogheadericon
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
.s7videoviewer .s7embeddialog .s7dialogheadertext
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
.s7videoviewer .s7embeddialog .s7closebutton
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

Esempio: per impostare l’intestazione della finestra di dialogo con spaziatura, icona 24 x 14 pixel, titolo in grassetto a 16 punti e pulsante di chiusura a 28 x 28 pixel, posizionato due pixel dalla parte superiore e due pixel dalla parte destra del contenitore di dialogo:

```
.s7videoviewer .s7embeddialog .s7dialogheader { 
 padding: 10px; 
} 
.s7videoviewer .s7embeddialog .s7dialogheader .s7dialogline { 
 padding: 10px 10px 2px; 
} 
.s7videoviewer .s7embeddialog .s7dialogheadericon { 
    background-image: url("images/sdk/dlgembed_cap.png"); 
    height: 14px; 
    width: 24px; 
} 
.s7videoviewer .s7embeddialog .s7dialogheadertext { 
    font-size: 16pt; 
    font-weight: bold; 
    padding-left: 16px; 
} 
.s7videoviewer .s7embeddialog .s7closebutton { 
 top:2px; 
 right:2px; 
 padding:8px; 
 width:28px; 
 height:28px; 
} 
.s7videoviewer .s7embeddialog .s7closebutton[state='up'] { 
 background-image:url(images/sdk/close_up.png); 
} 
.s7videoviewer .s7embeddialog .s7closebutton[state='over'] { 
 background-image:url(images/sdk/close_over.png); 
} 
.s7videoviewer .s7embeddialog .s7closebutton[state='down'] { 
 background-image:url(images/sdk/close_down.png); 
} 
.s7videoviewer .s7embeddialog .s7closebutton[state='disabled'] { 
 background-image:url(images/sdk/close_disabled.png); 
}
```

Il piè di pagina della finestra di dialogo è costituito dal pulsante &quot;Annulla&quot;. Il contenitore piè di pagina è controllato con il seguente selettore di classe CSS:

```
.s7videoviewer .s7embeddialog .s7dialogfooter
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
.s7videoviewer .s7embeddialog .s7dialogbuttoncontainer
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
.s7videoviewer .s7embeddialog .s7dialogactionbutton
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
.s7videoviewer .s7embeddialog .s7dialogcancelbutton
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
>Il pulsante Annulla supporta il selettore di attributi `state` , che può essere utilizzato per applicare interfacce diverse a diversi stati del pulsante.

Inoltre, entrambi i pulsanti condividono la stessa classe CSS comune che può contenere impostazioni CSS uguali per altri pulsanti della finestra di dialogo:

```
.s7videoviewer .s7embeddialog .s7dialogfooter .s7button
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
.s7videoviewer .s7embeddialog .s7dialogfooter { 
    border-top: 1px solid #909090; 
} 
.s7videoviewer .s7embeddialog .s7dialogbuttoncontainer { 
    padding-bottom: 6px; 
    padding-top: 10px; 
} 
.s7videoviewer .s7embeddialog .s7dialogfooter .s7button { 
    box-shadow: 1px 1px 1px #999999; 
    color: #FFFFFF; 
    font-size: 9pt; 
    font-weight: bold; 
    line-height: 34px; 
    margin-right: 10px; 
} 
.s7videoviewer .s7embeddialog .s7dialogcancelbutton { 
 width:64px; 
 height:34px; 
} 
.s7videoviewer .s7embeddialog .s7dialogcancelbutton[state='up'] { 
 background-color:#666666; 
 color:#dddddd; 
} 
.s7videoviewer .s7embeddialog .s7dialogcancelbutton[state='down'] { 
 background-color:#555555; 
 color:#ffffff; 
} 
.s7videoviewer .s7embeddialog .s7dialogcancelbutton[state='over'] { 
 background-color:#555555; 
 color:#ffffff; 
} 
.s7videoviewer .s7embeddialog .s7dialogcancelbutton[state='disabled'] { 
 background-color:#b2b2b2; 
 color:#dddddd; 
} 
.s7videoviewer .s7embeddialog .s7dialogactionbutton { 
 width:82px; 
 height:34px; 
} 
.s7videoviewer .s7embeddialog .s7dialogactionbutton[state='up'] { 
 background-color:#333333; 
 color:#dddddd; 
} 
.s7videoviewer .s7embeddialog .s7dialogactionbutton[state='down'] { 
 background-color:#222222; 
 color:#cccccc; 
} 
.s7videoviewer .s7embeddialog .s7dialogactionbutton[state='over'] { 
 background-color:#222222; 
 color:#cccccc; 
} 
.s7videoviewer .s7embeddialog .s7dialogactionbutton[state='disabled'] { 
 background-color:#b2b2b2; 
 color:#dddddd; 
}
```

L’area della finestra di dialogo principale (tra intestazione e piè di pagina) contiene il contenuto della finestra di dialogo scorrevole e il pannello di scorrimento a destra. In tutti i casi, il componente gestisce la larghezza di quest’area, non è possibile impostarla in CSS. L’area di dialogo principale è controllata dal seguente selettore di classe CSS:

```
.s7videoviewer .s7embeddialog .s7dialogviewarea
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
.s7videoviewer .s7embeddialog .s7dialogviewarea { 
 background-color:#ffffff; 
 margin:10px; 
 height:300px; 
}
```

Tutto il contenuto del modulo (come etichette e campi di input) risiede all’interno di un contenitore controllato con

```
.s7videoviewer .s7embeddialog .s7dialogbody
```

Se l’altezza di questo contenitore sembra essere maggiore dell’area della finestra di dialogo principale, il componente attiva automaticamente lo scorrimento verticale.

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
.s7videoviewer .s7embeddialog .s7dialogbody { 
    padding: 10px; 
}
```

Tutte le etichette statiche nel modulo della finestra di dialogo vengono controllate con

```
.s7videoviewer .s7embeddialog .s7dialoglabel
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

Le descrizioni comandi della finestra di dialogo delle etichette possono essere localizzate. Per ulteriori informazioni, consulta [Localizzazione degli elementi dell’interfaccia utente](../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/r-html5-video-viewer-20-localization.md#concept-1d5ca2d8480f4064a51eddba13940aad) .

Esempio: per impostare tutte le etichette in modo che siano grigie, in grassetto con un carattere di nove pixel:

```
.s7videoviewer .s7embeddialog .s7dialoglabel { 
    color: #666666; 
    font-size: 9pt; 
    font-weight: bold; 
}
```

La dimensione della copia di testo visualizzata sopra il codice di incorporamento è controllata dal seguente selettore di classe CSS:

```
.s7videoviewer .s7embeddialog .s7dialoginputwide
```

**Proprietà CSS del campo di input a livello di finestra di dialogo**

<table id="table_7275B4365DFA4C0386FA2BDB7204A517"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> larghezza  </span> </p> </td> 
   <td colname="col2"> <p>Larghezza campo di input. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> spaziatura interna  </span> </p> </td> 
   <td colname="col2"> <p>Spaziatura interna. </p> </td> 
  </tr> 
 </tbody> 
</table>

Esempio: per impostare una copia di testo con una larghezza di 430 pixel e una spaziatura di dieci pixel nella parte inferiore:

```
.s7videoviewer .s7embeddialog .s7dialoginputwide { 
    padding-bottom: 10px; 
    width: 430px; 
}
```

Il codice di incorporamento viene racchiuso in un contenitore e controllato con il seguente selettore di classe CSS:

```
.s7videoviewer .s7embeddialog .s7dialoginputcontainer
```

**Proprietà CSS del contenitore di input della finestra di dialogo**

<table id="table_7BC1C5919A54483F8121D928DC63233A"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> larghezza  </span> </p> </td> 
   <td colname="col2"> <p>Larghezza del contenitore del codice di incorporamento. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> border  </span> </p> </td> 
   <td colname="col2"> <p>Bordo intorno al contenitore del codice di incorporamento. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> spaziatura interna  </span> </p> </td> 
   <td colname="col2"> <p>Spaziatura interna. </p> </td> 
  </tr> 
 </tbody> 
</table>

Esempio: per impostare un bordo grigio di un pixel intorno al testo del codice da incorporare, renderlo largo 430 pixel e avere una spaziatura di dieci pixel:

```
.s7videoviewer .s7embeddialog .s7dialoginputcontainer { 
    border: 1px solid #CCCCCC; 
    padding: 10px; 
    width: 430px; 
}
```

Il testo del codice di incorporamento effettivo è controllato con il seguente selettore di classe CSS:

```
.s7videoviewer .s7embeddialog .s7dialoginputcontainer
```

**Proprietà CSS del contenitore di input della finestra di dialogo**

<table id="table_FEEF66150C69489BB42A2408EBFCE928"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ritorno a capo  </span> </p> </td> 
   <td colname="col2"> <p>Stile di wrapping della parola. </p> </td> 
  </tr> 
 </tbody> 
</table>

Esempio: per impostare il codice di incorporamento per utilizzare il ritorno a capo automatico `break-word`:

```
.s7videoviewer .s7embeddialog .s7dialogmessage { 
    word-wrap: break-word; 
}
```

L’etichetta e l’elenco a discesa delle dimensioni di incorporamento si trovano nella parte inferiore della finestra di dialogo e vengono inseriti in un contenitore controllato con il seguente selettore di classe CSS:

```
.s7videoviewer .s7embeddialog .s7dialogembedsizepanel
```

**Proprietà CSS del pannello dimensione incorporamento della finestra di dialogo**

<table id="table_6BA2769361BA4EC4AB7D250EC9486CB2"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> spaziatura interna  </span> </p> </td> 
   <td colname="col2"> <p>Spaziatura interna. </p> </td> 
  </tr> 
 </tbody> 
</table>

Esempio: per impostare un pannello di dimensioni da incorporare con dieci pixel di spaziatura:

```
.s7videoviewer .s7embeddialog .s7dialogembedsizepanel { 
    padding: 10px; 
}
```

Le dimensioni e l’allineamento dell’etichetta delle dimensioni di incorporamento sono controllate dal seguente selettore di classe CSS:

```
.s7videoviewer .s7embeddialog .s7dialogembedsizepanel
```

**Proprietà CSS del pannello dimensione incorporamento della finestra di dialogo**

<table id="table_8E50C63C9B1349999251CDB5E5AD3D1D"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> allineamento verticale  </span> </p> </td> 
   <td colname="col2"> <p>Allineamento verticale delle etichette. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> larghezza  </span> </p> </td> 
   <td colname="col2"> <p>Larghezza etichetta. </p> </td> 
  </tr> 
 </tbody> 
</table>

Esempio: per impostare l’etichetta delle dimensioni da incorporare in modo che sia allineata in alto e larga 80 pixel:

```
.s7videoviewer .s7embeddialog .s7dialogembedsizelabel { 
    vertical-align: top; 
    width: 80px; 
}
```

La larghezza della casella combinata Dimensione incorporamento è controllata dal seguente selettore di classe CSS:

```
.s7videoviewer .s7embeddialog .s7combobox
```

**Proprietà CSS della casella combinata**

<table id="table_C0FEA0C7353F40039204641BB3F1AE14"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> larghezza  </span> </p> </td> 
   <td colname="col2"> <p>Larghezza casella combinata. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>La casella combinata supporta il selettore di attributi `expanded` con possibili valori di `true` e `false`. `true` viene utilizzato quando la casella combinata visualizza una delle dimensioni predefinite di incorporamento, quindi deve assumere tutta la larghezza disponibile. `false` viene utilizzato quando nella casella combinata è selezionata l’opzione per le dimensioni personalizzate, quindi dovrebbe ridursi per consentire lo spazio per i campi di input personalizzati di larghezza e altezza.

Esempio: per impostare la casella combinata Dimensione incorporamento su una larghezza di 300 pixel quando viene visualizzata una voce predefinita e larga 110 pixel quando viene visualizzata una dimensione personalizzata:

```
.s7videoviewer .s7embeddialog .s7combobox[expanded="true"] { 
    width: 300px; 
} 
.s7videoviewer .s7embeddialog .s7combobox[expanded="false"] { 
    width: 110px; 
}
```

L’altezza del testo della casella combinata è definita da un elemento interno speciale ed è controllata con il seguente selettore di classe CSS:

```
.s7videoviewer .s7embeddialog .s7combobox .s7comboboxtext
```

**Proprietà CSS del testo della casella combinata**

<table id="table_AB60032BF337433F8455DE20AFBA29AB"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> altezza  </span> </p> </td> 
   <td colname="col2"> <p>Altezza testo casella combinata. </p> </td> 
  </tr> 
 </tbody> 
</table>

Esempio: per impostare l&#39;altezza del testo della casella combinata delle dimensioni di incorporamento su 40 pixel:

```
.s7videoviewer .s7embeddialog .s7combobox .s7comboboxtext { 
    height: 40px; 
}
```

La casella combinata ha un pulsante &quot;a discesa&quot; a destra ed è controllata con il seguente selettore di classe CSS:

```
.s7videoviewer .s7embeddialog .s7combobox .s7comboboxbutton
```

**Proprietà CSS del pulsante Casella combinata**

<table id="table_70E127FA21264366AD5DBBD7DF40EBAA"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> top  </span> </p> </td> 
   <td colname="col2"> <p>Posizione del pulsante verticale all’interno della casella combinata. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> right  </span> </p> </td> 
   <td colname="col2"> <p>Posizione del pulsante orizzontale all’interno della casella combinata. </p> </td> 
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
   <td colname="col2"> <p>Immagine pulsante per ogni stato. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> posizione di sfondo  </span> </p> </td> 
   <td colname="col2"> <p> Posizione all’interno dello sprite di un’immagine, se vengono utilizzati gli spriti CSS. </p> <p>Consulta <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-customizingviewer/c-html5-video-viewer-20-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> Sprite CSS </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

Questo pulsante supporta il selettore di attributi `state` , che può essere utilizzato per applicare interfacce diverse a diversi stati del pulsante.

Esempio: per impostare un pulsante &quot;a discesa&quot; su 28 x 28 pixel e ottenere un’immagine separata per ogni stato:

```
.s7videoviewer .s7embeddialog .s7combobox .s7comboboxbutton { 
 width:28px; 
 height:28px; 
} 
.s7videoviewer .s7embeddialog .s7combobox .s7comboboxbutton[state='up'] { 
 background-image:url(images/sdk/cboxbtndn_up.png); 
} 
.s7videoviewer .s7embeddialog .s7combobox .s7comboboxbutton[state='over'] { 
 background-image:url(images/sdk/cboxbtndn_over.png); 
} 
.s7videoviewer .s7embeddialog .s7combobox .s7comboboxbutton[state='down'] { 
 background-image:url(images/sdk/cboxbtndn_over.png); 
} 
.s7videoviewer .s7embeddialog .s7combobox .s7comboboxbutton[state='disabled'] { 
 background-image:url(images/sdk/cboxbtndn_up.png); 
}
```

Il pannello con l’elenco delle dimensioni di incorporamento visualizzato all’apertura della casella combinata è controllato con il seguente selettore di classe CSS:

```
.s7videoviewer .s7embeddialog .s7comboboxdropdown
```

Le dimensioni e la posizione del pannello sono controllate dal componente. Non è possibile modificarlo tramite CSS.

**Proprietà CSS dell’elenco a discesa della casella combinata**

<table id="table_FA7345321C6A4E63B4B78ECF81CE18DB"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> border  </span> </p> </td> 
   <td colname="col2"> <p>Bordo del pannello. </p> </td> 
  </tr> 
 </tbody> 
</table>

Esempio: per impostare il pannello della casella combinata con un bordo grigio di un pixel:

```
.s7videoviewer .s7embeddialog .s7comboboxdropdown { 
    border: 1px solid #CCCCCC; 
}
```

Un singolo elemento in un pannello a discesa controllato con il seguente selettore di classe CSS:

```
.s7videoviewer .s7embeddialog .s7dropdownitemanchor
```

**Proprietà CSS dell’ancoraggio elemento a discesa**

<table id="table_FD42FDD56F89463A97FD292FAA04DA5A"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> colore di sfondo  </span> </p> </td> 
   <td colname="col2"> <p>Sfondo articolo. </p> </td> 
  </tr> 
 </tbody> 
</table>

Esempio: per impostare l’elemento del pannello della casella combinata su uno sfondo bianco:

```
.s7videoviewer .s7embeddialog .s7dropdownitemanchor { 
    background-color: #FFFFFF; 
}
```

Un segno di spunta visualizzato a sinistra dell’elemento selezionato all’interno del pannello della casella combinata controllato con il seguente selettore di classe CSS:

```
.s7videoviewer .s7embeddialog .s7checkmark
```

**Proprietà CSS della casella di spunta**

<table id="table_8E01F5461CD04AC18B2C3725A961476A"> 
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
   <td colname="col2"> <p>Immagine dell'elemento. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> posizione di sfondo  </span> </p> </td> 
   <td colname="col2"> <p> Posizione all’interno dello sprite di un’immagine, se vengono utilizzati gli spriti CSS. </p> <p>Consulta <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-customizingviewer/c-html5-video-viewer-20-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> Sprite CSS </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

Esempio: per impostare l’icona del segno di spunta su 25 x 25 pixel:

```
.s7videoviewer .s7embeddialog .s7checkmark { 
    background-image: url("images/sdk/cboxchecked.png"); 
    height: 25px; 
    width: 25px; 
}
```

Quando l&#39;opzione &quot;Dimensione personalizzata&quot; è selezionata nella casella combinata Dimensione incorporamento, nella finestra di dialogo vengono visualizzati due campi di input aggiuntivi a destra per consentire all&#39;utente di immettere una dimensione di incorporamento personalizzata. Tali campi sono racchiusi in un contenitore controllato con il seguente selettore di classe CSS:

```
.s7videoviewer .s7embeddialog .s7dialogcustomsizepanel
```

**Proprietà CSS del pannello dimensioni personalizzate della finestra di dialogo**

<table id="table_B00829EA550F4E5E8F51B1C6ADACCD34"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> sinistra  </span> </p> </td> 
   <td colname="col2"> <p> Distanza dalla casella combinata Dimensione di incorporamento. </p> </td> 
  </tr> 
 </tbody> 
</table>

Esempio: per impostare il pannello campi di input con dimensioni personalizzate su 20 pixel a destra della casella combinata:

```
.s7videoviewer .s7embeddialog .s7dialogcustomsizepanel { 
    left: 20px; 
}
```

Ogni campo di input con dimensioni personalizzate viene racchiuso in un contenitore che esegue il rendering di un bordo e imposta il margine tra i campi. È controllato con il seguente selettore di classe CSS:

```
.s7videoviewer .s7embeddialog .s7dialogcustomsize
```

**Proprietà CSS delle dimensioni personalizzate della finestra di dialogo**

<table id="table_A8A04BE1988641618D0A412B8AEEE1C5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> border  </span> </p> </td> 
   <td colname="col2"> <p>Bordo intorno al campo di input. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> larghezza  </span> </p> </td> 
   <td colname="col2"> <p> Larghezza campo di input. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margine  </span> </p> </td> 
   <td colname="col2"> <p> Margine del campo di input. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> spaziatura interna  </span> </p> </td> 
   <td colname="col2"> <p> Spaziatura dei campi di input. </p> </td> 
  </tr> 
 </tbody> 
</table>

Esempio: per impostare le dimensioni personalizzate dei campi di input in modo che abbiano un bordo grigio di un pixel, un margine, una spaziatura e una larghezza di 70 pixel:

```
.s7videoviewer .s7embeddialog .s7dialogcustomsize { 
    border: 1px solid #CCCCCC; 
    margin-right: 20px; 
    padding-left: 2px; 
    padding-right: 2px; 
    width: 70px; 
}
```

Se è necessario lo scorrimento verticale, la barra di scorrimento viene riprodotta nel pannello vicino al bordo destro della finestra di dialogo, controllata con il seguente selettore di classe CSS:

```
.s7videoviewer .s7embeddialog .s7dialogscrollpanel
```

**Proprietà CSS del pannello di scorrimento della finestra di dialogo**

<table id="table_BA37E577E0884C919383F84080E2DD28"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> larghezza  </span> </p> </td> 
   <td colname="col2"> <p>Larghezza del pannello di scorrimento. </p> </td> 
  </tr> 
 </tbody> 
</table>

Esempio: per impostare un pannello di scorrimento con larghezza di 44 pixel

```
.s7videoviewer .s7embeddialog .s7dialogscrollpanel { 
    width: 44px; 
}
```

L’aspetto dell’area della barra di scorrimento è controllato con il seguente selettore di classe CSS:

```
.s7videoviewer .s7embeddialog .s7scrollbar
```

**Proprietà CSS della barra di scorrimento**

<table id="table_066492417FCA43929017993D7326CDB8"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> larghezza  </span> </p> </td> 
   <td colname="col2"> <p>Larghezza barra di scorrimento. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> top  </span> </p> </td> 
   <td colname="col2"> <p> Offset della barra di scorrimento verticale dalla parte superiore del pannello di scorrimento. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> bottom  </span> </p> </td> 
   <td colname="col2"> <p> Offset della barra di scorrimento verticale dalla parte inferiore del pannello di scorrimento. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> right  </span> </p> </td> 
   <td colname="col2"> <p> Offset della barra di scorrimento orizzontale dal bordo destro del pannello di scorrimento. </p> </td> 
  </tr> 
 </tbody> 
</table>

Esempio: per impostare una barra di scorrimento larga 28 pixel e con un margine di otto pixel rispetto alla parte superiore, destra e inferiore del pannello di scorrimento:

```
.s7videoviewer .s7embeddialog .s7scrollbar { 
    bottom: 8px; 
    right: 8px; 
    top: 8px; 
    width: 28px; 
}
```

La traccia della barra di scorrimento è l’area compresa tra i pulsanti di scorrimento superiore e inferiore. Il componente imposta automaticamente la posizione e l&#39;altezza del brano. La traccia è controllata con il seguente selettore di classe CSS

```
.s7videoviewer .s7embeddialog .s7scrollbar .s7scrolltrack
```

**Proprietà CSS del brano della barra di scorrimento**

<table id="table_19CF5503C1D34ED9998D4F4A6DA7D5D5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> larghezza  </span> </p> </td> 
   <td colname="col2"> <p>Larghezza traccia. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> colore di sfondo  </span> </p> </td> 
   <td colname="col2"> <p> Colore di sfondo del brano. </p> </td> 
  </tr> 
 </tbody> 
</table>

Esempio: per impostare una traccia della barra di scorrimento larga 28 pixel e con sfondo grigio:

```
.s7videoviewer .s7embeddialog .s7scrollbar .s7scrolltrack { 
width:28px; 
background-color: #B2B2B2; 
}
```

Il pollice della barra di scorrimento si sposta verticalmente all’interno di un’area della traccia di scorrimento. La sua posizione verticale è completamente controllata dalla logica del componente. Tuttavia, l’altezza della miniatura non cambia dinamicamente a seconda della quantità di contenuto. L’altezza del pollice e altri aspetti possono essere configurati con il seguente selettore di classe CSS:

```
.s7videoviewer .s7embeddialog .s7scrollbar .s7scrollthumb
```

**Proprietà CSS della miniatura della barra di scorrimento**

<table id="table_90BC468FE138441C9DBAB1EB109F3DB0"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> larghezza  </span> </p> </td> 
   <td colname="col2"> <p>Larghezza pollice. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> altezza  </span> </p> </td> 
   <td colname="col2"> <p>Altezza del pollice. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> imbottitura superiore  </span> </p> </td> 
   <td colname="col2"> <p>Spaziatura verticale tra la parte superiore della traccia. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> imbottitura inferiore  </span> </p> </td> 
   <td colname="col2"> <p> Spaziatura verticale tra il fondo della traccia. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> immagine di sfondo  </span> </p> </td> 
   <td colname="col2"> <p> Immagine visualizzata per un dato stato pollice. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>La funzione Thumb supporta il selettore di attributi `state`, che può essere utilizzato per applicare skin diversi a diversi stati di pollice: `up`, `down`, `over` e `disabled`.

Esempio: per impostare un pollice della barra di scorrimento di 28 x 45 pixel, ha un margine di dieci pixel in alto e in basso e ha un’immagine diversa per ogni stato:

```
.s7videoviewer .s7embeddialog .s7scrollbar .s7scrollthumb { 
    height: 45px; 
    padding-bottom: 10px; 
    padding-top: 10px; 
    width: 28px; 
} 
.s7videoviewer .s7embeddialog .s7scrollbar .s7scrollthumb[state="up"] { 
 background-image:url("images/sdk/scrollbar_thumb_up.png"); 
} 
.s7videoviewer .s7embeddialog .s7scrollbar .s7scrollthumb[state="down"] { 
 background-image:url("images/sdk/scrollbar_thumb_down.png"); 
} 
.s7videoviewer .s7embeddialog .s7scrollbar .s7scrollthumb[state="over"] { 
 background-image:url("images/sdk/scrollbar_thumb_over.png"); 
} 
.s7videoviewer .s7embeddialog .s7scrollbar .s7scrollthumb[state="disabled"] { 
 background-image:url("images/sdk/scrollbar_thumb_disabled.png"); 
}
```

L’aspetto dei pulsanti di scorrimento superiore e inferiore è controllato con i seguenti selettori di classe CSS:

```
.s7videoviewer .s7embeddialog .s7scrollbar .s7scrollupbutton 
```

```
.s7videoviewer .s7embeddialog .s7scrollbar .s7scrolldownbutton
```

Non è possibile posizionare i pulsanti di scorrimento utilizzando le proprietà CSS in alto, a sinistra, in basso e a destra. Al contrario, la logica del visualizzatore li posiziona automaticamente.

**Proprietà CSS dei pulsanti di scorrimento superiore e inferiore**

<table id="table_554BFCFEAF4F43A9AE5F741DC126F833"> 
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
>Questi pulsanti supportano il selettore di attributi `state` , che può essere utilizzato per applicare interfacce diverse a diversi stati dei pulsanti: `up`, `down`, `over` e `disabled`.

Le descrizioni dei pulsanti possono essere localizzate. Per ulteriori informazioni, consulta [Localizzazione degli elementi dell’interfaccia utente](../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/r-html5-video-viewer-20-localization.md#concept-1d5ca2d8480f4064a51eddba13940aad) .

Esempio: per impostare pulsanti di scorrimento con 28 x 32 pixel e immagini diverse per ogni stato:

```
.s7videoviewer .s7embeddialog .s7scrollbar .s7scrollupbutton { 
 width:28px; 
 height:32px; 
} 
.s7videoviewer .s7embeddialog .s7scrollbar .s7scrollupbutton[state='up'] { 
background-image:url(images/sdk/scroll_up_up.png); 
} 
.s7videoviewer .s7embeddialog .s7scrollbar .s7scrollupbutton[state='over'] { 
 background-image:url(images/sdk/scroll_up_over.png); 
} 
.s7videoviewer .s7embeddialog .s7scrollbar .s7scrollupbutton[state='down'] { 
 background-image:url(images/sdk/scroll_up_down.png); 
} 
.s7videoviewer .s7embeddialog .s7scrollbar .s7scrollupbutton[state='disabled'] { 
 background-image:url(images/sdk/scroll_up_disabled.png); 
} 
.s7videoviewer .s7embeddialog .s7scrollbar .s7scrolldownbutton { 
 width:28px; 
 height:32px; 
} 
.s7videoviewer .s7embeddialog .s7scrollbar .s7scrolldownbutton[state='up'] { 
 background-image:url(images/sdk/scroll_down_up.png); 
} 
.s7videoviewer .s7embeddialog .s7scrollbar .s7scrolldownbutton[state='over'] { 
 background-image:url(images/sdk/scroll_down_over.png); 
} 
.s7videoviewer .s7embeddialog .s7scrollbar .s7scrolldownbutton[state='down'] { 
 background-image:url(images/sdk/scroll_down_down.png); 
} 
.s7videoviewer .s7embeddialog .s7scrollbar .s7scrolldownbutton[state='disabled'] { 
 background-image:url(images/sdk/scroll_down_disabled.png); 
}
```

