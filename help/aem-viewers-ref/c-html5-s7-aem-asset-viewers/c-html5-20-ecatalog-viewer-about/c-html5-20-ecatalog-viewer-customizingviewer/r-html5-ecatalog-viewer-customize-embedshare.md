---
description: Lo strumento Incorpora condivisione è costituito da un pulsante aggiunto al pannello Condivisione social network e dalla finestra di dialogo modale visualizzata quando lo strumento è attivato. La posizione del pulsante è gestita completamente dallo strumento di condivisione mediante social network.
seo-description: Lo strumento Incorpora condivisione è costituito da un pulsante aggiunto al pannello Condivisione social network e dalla finestra di dialogo modale visualizzata quando lo strumento è attivato. La posizione del pulsante è gestita completamente dallo strumento di condivisione mediante social network.
seo-title: Incorpora condivisione
solution: Experience Manager
title: Incorpora condivisione
topic: Dynamic media
uuid: 59a21a90-5f34-4e1f-90e7-cce18aed5e6b
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef

---


# Incorpora condivisione{#embed-share}

Lo strumento Incorpora condivisione è costituito da un pulsante aggiunto al pannello Condivisione social network e dalla finestra di dialogo modale visualizzata quando lo strumento è attivato. La posizione del pulsante è gestita completamente dallo strumento di condivisione mediante social network.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

L&#39;aspetto del pulsante di condivisione incorporato è controllato dal seguente selettore di classe CSS:

```
.s7ecatalogviewer .s7embedshare
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
   <td colname="col1"> <p> <span class="codeph"> background-image </span> </p> </td> 
   <td colname="col2"> <p> Immagine visualizzata per un determinato stato del pulsante. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> Posizionare all'interno dello sprite della grafica, se vengono utilizzati gli spriti CSS. </p> <p>Consultate anche <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-customizingviewer/c-html5-20-ecatalog-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> CSS Sprite </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Questo pulsante supporta il selettore `state` di attributi, che può essere utilizzato per applicare interfacce diverse a stati di pulsante diversi.

È possibile rimuovere il pulsante dal pannello Condivisione social network impostando la proprietà `display:none` CSS della classe CSS.

La descrizione del pulsante può essere localizzata. Per ulteriori informazioni, consultate [Localizzazione degli elementi](../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) dell&#39;interfaccia utente.

Esempio: per impostare un pulsante di condivisione per incorporamento di 28 x 28 pixel e visualizzare un’immagine diversa per ciascuno dei quattro stati del pulsante:

```
.s7ecatalogviewer .s7embedshare { 
 width:28px; 
 height:28px; 
} 
.s7ecatalogviewer .s7embedshare[state='up'] { 
background-image:url(images/v2/EmbedShare_dark_up.png); 
} 
.s7ecatalogviewer .s7embedshare[state='over'] { 
background-image:url(images/v2/EmbedShare_dark_over.png); 
} 
.s7ecatalogviewer .s7embedshare[state='down'] { 
background-image:url(images/v2/EmbedShare_dark_down.png); 
} 
.s7ecatalogviewer .s7embedshare[state='disabled'] { 
background-image:url(images/v2/EmbedShare_dark_disabled.png); 
}
```

La sovrapposizione di sfondo che copre la pagina Web quando la finestra di dialogo è attiva è controllata dal seguente selettore di classe CSS:

```
.s7ecatalogviewer .s7embeddialog .s7backoverlay
```

**Proprietà CSS della sovrapposizione di sfondo**

<table id="table_DB4183CE8061425084D495A355A941F8"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> opacità </span> </p> </td> 
   <td colname="col2"> <p>Opacità sovrapposizione sfondo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p>Colore di sovrapposizione sfondo. </p> </td> 
  </tr> 
 </tbody> 
</table>

Esempio: per impostare una sovrapposizione di sfondo grigia con opacità del 70%:

```
.s7ecatalogviewer .s7embeddialog .s7backoverlay { 
 opacity:0.7; 
 background-color:#222222; 
}
```

Per impostazione predefinita, la finestra di dialogo modale viene visualizzata centrata sullo schermo sui sistemi desktop e occupa l’intera area della pagina Web sui dispositivi touch. In tutti i casi, il posizionamento e il ridimensionamento della finestra di dialogo vengono gestiti dal componente. La finestra di dialogo è controllata dal seguente selettore di classe CSS:

```
.s7embeddialog .s7dialog
```

**Proprietà CSS della finestra di dialogo**

<table id="table_E31711ADF4C7446182549244362199A3"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> border-radius </span> </p> </td> 
   <td colname="col2"> <p> Raggio del bordo della finestra di dialogo, se la finestra di dialogo non utilizza l'intero browser. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p>Colore di sfondo della finestra di dialogo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Deve essere disimpostata o impostata su 100%, nel qual caso la finestra di dialogo utilizza l’intera finestra del browser (questa modalità è preferita per i dispositivi touch). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Deve essere disimpostata o impostata su 100%, nel qual caso la finestra di dialogo utilizza l’intera finestra del browser (questa modalità è preferita per i dispositivi touch). </p> </td> 
  </tr> 
 </tbody> 
</table>

Esempio: per impostare la finestra di dialogo in modo che utilizzi l’intera finestra del browser e che abbia uno sfondo bianco sui dispositivi touch:

```
.s7ecatalogviewer .s7touchinput .s7embeddialog .s7dialog { 
 width:100%; 
 height:100%; 
background-color: #ffffff; 
}
```

L&#39;intestazione della finestra di dialogo è composta da un&#39;icona, un testo del titolo e un pulsante Chiudi. Il contenitore di intestazione è controllato con

```
.s7ecatalogviewer .s7embeddialog .s7dialogheader
```

**Proprietà CSS dell&#39;intestazione della finestra di dialogo**

<table id="table_E407E844C9BD4B5DA8B5BBDE0554F9CA"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> spaziatura </span> </p> </td> 
   <td colname="col2"> <p> Spaziatura interna per il contenuto dell’intestazione. </p> </td> 
  </tr> 
 </tbody> 
</table>

L&#39;icona e il testo del titolo sono racchiusi in un contenitore aggiuntivo controllato da

```
.s7ecatalogviewer .s7embeddialog .s7dialogheader .s7dialogline
```

**Proprietà CSS della riga di dialogo**

<table id="table_5B03CF843F0D4B1295A3FC1EB50C56F1"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> spaziatura </span> </p> </td> 
   <td colname="col2"> <p> Spaziatura interna per l’icona dell’intestazione e il titolo </p> </td> 
  </tr> 
 </tbody> 
</table>

L&#39;icona dell&#39;intestazione è controllata dal seguente selettore di classe CSS

```
.s7ecatalogviewer .s7embeddialog .s7dialogheadericon
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
   <td colname="col2"> <p> Posizionare all'interno dello sprite della grafica, se vengono utilizzati gli spriti CSS. </p> <p>Consultate anche <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-customizingviewer/c-html5-20-ecatalog-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> CSS Sprite </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

Il titolo dell&#39;intestazione è controllato dal seguente selettore di classe CSS:

```
.s7ecatalogviewer .s7embeddialog .s7dialogheadertext
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
   <td colname="col2"> <p>Altezza del font. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family </span> </p> </td> 
   <td colname="col2"> <p>Famiglia di font. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> spaziatura </span> </p> </td> 
   <td colname="col2"> <p>Spaziatura interna del testo. </p> </td> 
  </tr> 
 </tbody> 
</table>

Il pulsante Chiudi è controllato dal seguente selettore di classe CSS:

```
.s7ecatalogviewer .s7embeddialog .s7closebutton
```

**Proprietà CSS del pulsante di chiusura **

<table id="table_FAECBC489FC442588E50E3DA0AC16DD7"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> top </span> </p> </td> 
   <td colname="col2"> <p> Posizione del pulsante verticale rispetto al contenitore dell’intestazione. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> right </span> </p> </td> 
   <td colname="col2"> <p> Posizione del pulsante orizzontale rispetto al contenitore dell'intestazione. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Larghezza pulsante. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Altezza del pulsante. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> spaziatura </span> </p> </td> 
   <td colname="col2"> <p>Spaziatura interna del pulsante. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image </span> </p> </td> 
   <td colname="col2"> <p>Immagine pulsante per ogni stato. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> Posizionare all'interno dello sprite della grafica, se vengono utilizzati gli spriti CSS. </p> <p>Consultate anche <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-customizingviewer/c-html5-20-ecatalog-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> CSS Sprite </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Questo pulsante supporta il selettore `state` di attributi, che può essere utilizzato per applicare interfacce diverse a stati di pulsante diversi.

La descrizione del pulsante può essere localizzata. Per ulteriori informazioni, consultate [Localizzazione degli elementi](../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) dell&#39;interfaccia utente.

Esempio: per impostare l’intestazione della finestra di dialogo con la spaziatura, l’icona da 24 x 14 pixel, il titolo in grassetto da 16 punti e il pulsante Chiudi da 28 x 28 pixel, posizionati due pixel dalla parte superiore e due pixel dalla parte destra del contenitore della finestra di dialogo:

```
.s7ecatalogviewer .s7embeddialog .s7dialogheader { 
 padding: 10px; 
} 
.s7ecatalogviewer .s7embeddialog .s7dialogheader .s7dialogline { 
 padding: 10px 10px 2px; 
} 
.s7ecatalogviewer .s7embeddialog .s7dialogheadericon { 
    background-image: url("images/sdk/dlgembed_cap.png"); 
    height: 14px; 
    width: 24px; 
} 
.s7ecatalogviewer .s7embeddialog .s7dialogheadertext { 
    font-size: 16pt; 
    font-weight: bold; 
    padding-left: 16px; 
} 
.s7ecatalogviewer .s7embeddialog .s7closebutton { 
 top:2px; 
 right:2px; 
 padding:8px; 
 width:28px; 
 height:28px; 
} 
.s7ecatalogviewer .s7embeddialog .s7closebutton[state='up'] { 
 background-image:url(images/sdk/close_up.png); 
} 
.s7ecatalogviewer .s7embeddialog .s7closebutton[state='over'] { 
 background-image:url(images/sdk/close_over.png); 
} 
.s7ecatalogviewer .s7embeddialog .s7closebutton[state='down'] { 
 background-image:url(images/sdk/close_down.png); 
} 
.s7ecatalogviewer .s7embeddialog .s7closebutton[state='disabled'] { 
 background-image:url(images/sdk/close_disabled.png); 
}
```

Il piè di pagina della finestra di dialogo è costituito dal pulsante &quot;cancel&quot;. Il contenitore piè di pagina è controllato dal seguente selettore di classe CSS:

```
.s7ecatalogviewer .s7embeddialog .s7dialogfooter
```

**Proprietà CSS del piè di pagina della finestra di dialogo **

<table id="table_0AF7AAAB846A46D690896AFD68575669"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> border </span> </p> </td> 
   <td colname="col2"> <p> Bordo che è possibile utilizzare per separare visivamente il piè di pagina dal resto della finestra di dialogo. </p> </td> 
  </tr> 
 </tbody> 
</table>

Il piè di pagina dispone di un contenitore interno che mantiene il pulsante. È controllato dal seguente selettore di classe CSS:

```
.s7ecatalogviewer .s7embeddialog .s7dialogbuttoncontainer
```

**Proprietà CSS del contenitore pulsanti della finestra di dialogo**

<table id="table_C34906888A8145C7A61E503DFC6B08A9"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> spaziatura </span> </p> </td> 
   <td colname="col2"> <p> Margine interno tra il piè di pagina e il pulsante. </p> </td> 
  </tr> 
 </tbody> 
</table>

Il pulsante Seleziona tutto è controllato dal seguente selettore di classe CSS:

```
.s7ecatalogviewer .s7embeddialog .s7dialogactionbutton
```

Il pulsante è disponibile solo sui sistemi desktop.

**Proprietà CSS del pulsante Seleziona tutto**

<table id="table_021D0467632F49FEBFDF4CF96D2D67C7"> 
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
   <td colname="col1"> <p> <span class="codeph"> color </span> </p> </td> 
   <td colname="col2"> <p> Colore del testo del pulsante per ogni stato. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p> Colore di sfondo del pulsante per ogni stato. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Il pulsante Seleziona tutto supporta il selettore `state` di attributi, che può essere utilizzato per applicare interfacce diverse a stati di pulsante differenti.

Il pulsante Annulla è controllato dal seguente selettore di classe CSS:

```
.s7ecatalogviewer .s7embeddialog .s7dialogcancelbutton
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
   <td colname="col2"> <p>Altezza del pulsante. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color </span> </p> </td> 
   <td colname="col2"> <p> Colore del testo del pulsante per ogni stato. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p> Colore di sfondo del pulsante per ogni stato. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Questo pulsante supporta il selettore `state` di attributi, che può essere utilizzato per applicare interfacce diverse a stati di pulsante diversi.

Inoltre, entrambi i pulsanti condividono la stessa classe CSS comune che può contenere impostazioni CSS identiche per gli altri pulsanti delle finestre di dialogo:

```
.s7ecatalogviewer .s7embeddialog .s7dialogfooter .s7button
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
   <td colname="col2"> <p>Dimensione del font del pulsante. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family </span> </p> </td> 
   <td colname="col2"> <p>Famiglia di font per i pulsanti. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> line-height </span> </p> </td> 
   <td colname="col2"> <p> Altezza del testo all'interno del pulsante. Interessa l’allineamento verticale. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> box-shadow </span> </p> </td> 
   <td colname="col2"> <p>Ombra esterna. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin-right </span> </p> </td> 
   <td colname="col2"> <p>Margine destro del pulsante. </p> </td> 
  </tr> 
 </tbody> 
</table>

La descrizione del pulsante può essere localizzata. Per ulteriori informazioni, consultate [Localizzazione degli elementi](../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) dell&#39;interfaccia utente.

Esempio: per impostare un piè di pagina di una finestra di dialogo con un pulsante Annulla 64x34, un pulsante Seleziona tutto 82x34 e un colore di testo e sfondo diverso per ogni stato del pulsante:

```
.s7ecatalogviewer .s7embeddialog .s7dialogfooter { 
    border-top: 1px solid #909090; 
} 
.s7ecatalogviewer .s7embeddialog .s7dialogbuttoncontainer { 
    padding-bottom: 6px; 
    padding-top: 10px; 
} 
.s7ecatalogviewer .s7embeddialog .s7dialogfooter .s7button { 
    box-shadow: 1px 1px 1px #999999; 
    color: #FFFFFF; 
    font-size: 9pt; 
    font-weight: bold; 
    line-height: 34px; 
    margin-right: 10px; 
} 
.s7ecatalogviewer .s7embeddialog .s7dialogcancelbutton { 
 width:64px; 
 height:34px; 
} 
.s7ecatalogviewer .s7embeddialog .s7dialogcancelbutton[state='up'] { 
 background-color:#666666; 
 color:#dddddd; 
} 
.s7ecatalogviewer .s7embeddialog .s7dialogcancelbutton[state='down'] { 
 background-color:#555555; 
 color:#ffffff; 
} 
.s7ecatalogviewer .s7embeddialog .s7dialogcancelbutton[state='over'] { 
 background-color:#555555; 
 color:#ffffff; 
} 
.s7ecatalogviewer .s7embeddialog .s7dialogcancelbutton[state='disabled'] { 
 background-color:#b2b2b2; 
 color:#dddddd; 
} 
.s7ecatalogviewer .s7embeddialog .s7dialogactionbutton { 
 width:82px; 
 height:34px; 
} 
.s7ecatalogviewer .s7embeddialog .s7dialogactionbutton[state='up'] { 
 background-color:#333333; 
 color:#dddddd; 
} 
.s7ecatalogviewer .s7embeddialog .s7dialogactionbutton[state='down'] { 
 background-color:#222222; 
 color:#cccccc; 
} 
.s7ecatalogviewer .s7embeddialog .s7dialogactionbutton[state='over'] { 
 background-color:#222222; 
 color:#cccccc; 
} 
.s7ecatalogviewer .s7embeddialog .s7dialogactionbutton[state='disabled'] { 
 background-color:#b2b2b2; 
 color:#dddddd; 
}
```

L’area della finestra di dialogo principale (tra l’intestazione e il piè di pagina) contiene il contenuto della finestra di dialogo scorrevole e il pannello di scorrimento a destra. In tutti i casi, il componente gestisce la larghezza dell’area, non è possibile impostarla in CSS. L&#39;area di dialogo principale è controllata dal seguente selettore di classe CSS:

```
.s7ecatalogviewer .s7embeddialog .s7dialogviewarea
```

**Proprietà CSS dell&#39;area di visualizzazione della finestra di dialogo **

<table id="table_3FF4691D848A4C4D8EF060B7E79DEEDE"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p> Altezza dell'area della finestra di dialogo principale. Deve essere specificato solo quando la finestra di dialogo funziona in modalità desktop. Non è applicabile quando le dimensioni della finestra di dialogo consentono di occupare l’intera finestra del browser. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p>Colore di sfondo dell'area della finestra di dialogo principale. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin </span> </p> </td> 
   <td colname="col2"> <p>Margine esterno. </p> </td> 
  </tr> 
 </tbody> 
</table>

Esempio: per impostare un&#39;area della finestra di dialogo principale pari a 300 pixel di altezza, avere un margine di dieci pixel e utilizzare uno sfondo bianco:

```
.s7ecatalogviewer .s7embeddialog .s7dialogviewarea { 
 background-color:#ffffff; 
 margin:10px; 
 height:300px; 
}
```

Tutto il contenuto del modulo (come etichette e campi di input) risiede all&#39;interno di un contenitore controllato dal seguente selettore di classe CSS:

```
.s7ecatalogviewer .s7embeddialog .s7dialogbody
```

Se l&#39;altezza di questo contenitore sembra essere maggiore dell&#39;area della finestra di dialogo principale, il componente attiva automaticamente uno scorrimento verticale.

**Proprietà CSS del corpo della finestra di dialogo **

<table id="table_5D77F3D5B8CD4B798AA85F722B277F56"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> spaziatura </span> </p> </td> 
   <td colname="col2"> <p>Spaziatura interna. </p> </td> 
  </tr> 
 </tbody> 
</table>

Esempio: per impostare il contenuto del modulo in modo che abbia una spaziatura di dieci pixel:

```
.s7ecatalogviewer .s7embeddialog .s7dialogbody { 
    padding: 10px; 
}
```

Tutte le etichette statiche nel modulo della finestra di dialogo sono controllate tramite

```
.s7ecatalogviewer .s7embeddialog .s7dialoglabel
```

Questa classe non è adatta per controllare la dimensione o la posizione dell&#39;etichetta, perché può essere applicata a testi in varie aree dell&#39;interfaccia utente del modulo.

**Proprietà CSS dell&#39;etichetta della finestra di dialogo. **

<table id="table_13C7874807314ADD83A23075ABB4C340"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-weight </span> </p> </td> 
   <td colname="col2"> <p>Etichetta spessore font. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size </span> </p> </td> 
   <td colname="col2"> <p>Etichetta dimensione font. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family </span> </p> </td> 
   <td colname="col2"> <p>Etichetta famiglia di font. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color </span> </p> </td> 
   <td colname="col2"> <p>Colore del testo dell’etichetta. </p> </td> 
  </tr> 
 </tbody> 
</table>

Le etichette delle finestre di dialogo possono essere localizzate. Per ulteriori informazioni, consultate [Localizzazione degli elementi](../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) dell&#39;interfaccia utente.

Esempio: per impostare tutte le etichette in modo che siano grigie, grassetto con un font di nove pixel:

```
.s7ecatalogviewer .s7embeddialog .s7dialoglabel { 
    color: #666666; 
    font-size: 9pt; 
    font-weight: bold; 
}
```

La dimensione della copia di testo visualizzata sopra al codice da incorporare è controllata dal seguente selettore di classe CSS:

```
.s7ecatalogviewer .s7embeddialog .s7dialoginputwide
```

**Proprietà CSS del campo di immissione per l&#39;intero della finestra di dialogo**

<table id="table_7275B4365DFA4C0386FA2BDB7204A517"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Larghezza campo di input. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> spaziatura </span> </p> </td> 
   <td colname="col2"> <p>Spaziatura interna. </p> </td> 
  </tr> 
 </tbody> 
</table>

Esempio: per impostare la copia di testo su una larghezza di 430 pixel e disporre di una spaziatura di 10 pixel nella parte inferiore:

```
.s7ecatalogviewer .s7embeddialog .s7dialoginputwide { 
    padding-bottom: 10px; 
    width: 430px; 
}
```

Il codice da incorporare viene racchiuso in un contenitore e controllato con il seguente selettore di classe CSS:

```
.s7ecatalogviewer .s7embeddialog .s7dialoginputcontainer
```

**Proprietà CSS del contenitore di input della finestra di dialogo**

<table id="table_7BC1C5919A54483F8121D928DC63233A"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Larghezza del contenitore del codice da incorporare. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> border </span> </p> </td> 
   <td colname="col2"> <p>Bordo intorno al contenitore del codice da incorporare. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> spaziatura </span> </p> </td> 
   <td colname="col2"> <p>Spaziatura interna. </p> </td> 
  </tr> 
 </tbody> 
</table>

Esempio: per impostare un bordo grigio di un pixel attorno al testo del codice da incorporare, renderlo largo 430 pixel e avere una spaziatura di dieci pixel:

```
.s7ecatalogviewer .s7embeddialog .s7dialoginputcontainer { 
    border: 1px solid #CCCCCC; 
    padding: 10px; 
    width: 430px; 
}
```

Il testo effettivo del codice da incorporare è controllato dal seguente selettore di classe CSS:

```
.s7ecatalogviewer .s7embeddialog .s7dialoginputcontainer
```

**Proprietà CSS del contenitore di input della finestra di dialogo**

<table id="table_FEEF66150C69489BB42A2408EBFCE928"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ritorno a capo automatico </span> </p> </td> 
   <td colname="col2"> <p>Stile di ritorno a capo. </p> </td> 
  </tr> 
 </tbody> 
</table>

Esempio: per impostare il codice da incorporare in modo che venga utilizzato il ritorno a capo automatico `break-word` :

```
.s7ecatalogviewer .s7embeddialog .s7dialogmessage { 
    word-wrap: break-word; 
}
```

Le etichette delle dimensioni da incorporare e l&#39;elenco a discesa si trovano nella parte inferiore della finestra di dialogo e vengono inserite in un contenitore controllato dal seguente selettore di classe CSS:

```
.s7ecatalogviewer .s7embeddialog .s7dialogembedsizepanel
```

**Proprietà CSS del pannello Dimensione incorporamento della finestra di dialogo**

<table id="table_6BA2769361BA4EC4AB7D250EC9486CB2"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> spaziatura </span> </p> </td> 
   <td colname="col2"> <p>Spaziatura interna. </p> </td> 
  </tr> 
 </tbody> 
</table>

Esempio: per impostare un pannello delle dimensioni di incorporamento con dieci pixel di spaziatura:

```
.s7ecatalogviewer .s7embeddialog .s7dialogembedsizepanel { 
    padding: 10px; 
}
```

Le dimensioni e l&#39;allineamento dell&#39;etichetta della dimensione di incorporamento sono controllati dal seguente selettore di classe CSS:

```
.s7ecatalogviewer .s7embeddialog .s7dialogembedsizepanel
```

**Proprietà CSS del pannello Dimensione incorporamento della finestra di dialogo**

<table id="table_8E50C63C9B1349999251CDB5E5AD3D1D"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> vertical-align </span> </p> </td> 
   <td colname="col2"> <p>Allineamento dell'etichetta verticale. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Larghezza etichetta. </p> </td> 
  </tr> 
 </tbody> 
</table>

Esempio: per impostare l’etichetta delle dimensioni di incorporamento in modo che sia allineata in alto e larga 80 pixel:

```
.s7ecatalogviewer .s7embeddialog .s7dialogembedsizelabel { 
    vertical-align: top; 
    width: 80px; 
}
```

La larghezza della casella combinata Dimensione incorporamento è controllata dal seguente selettore di classe CSS:

```
.s7ecatalogviewer .s7embeddialog .s7combobox
```

**Proprietà CSS della casella combinata**

<table id="table_C0FEA0C7353F40039204641BB3F1AE14"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Larghezza casella combinata. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>La casella combinata supporta il selettore `expanded` di attributi con possibili valori di `true` e `false`. `true` viene utilizzato quando la casella combinata visualizza una delle dimensioni predefinite per l&#39;incorporamento, che deve quindi avere tutta la larghezza disponibile. `false` viene utilizzata quando nella casella combinata è selezionata l&#39;opzione relativa alle dimensioni personalizzate, in modo che lo spazio disponibile nei campi di immissione larghezza e altezza sia ridotto.

Esempio: per impostare la casella combinata delle dimensioni di incorporamento su una larghezza di 300 pixel quando viene visualizzata una voce predefinita e di 110 pixel in larghezza quando viene visualizzata una dimensione personalizzata:

```
.s7ecatalogviewer .s7embeddialog .s7combobox[expanded="true"] { 
    width: 300px; 
} 
.s7ecatalogviewer .s7embeddialog .s7combobox[expanded="false"] { 
    width: 110px; 
}
```

L&#39;altezza del testo della casella combinata è definita da un elemento interno speciale ed è controllata dal seguente selettore di classe CSS:

```
.s7ecatalogviewer .s7embeddialog .s7combobox .s7comboboxtext
```

**Proprietà CSS del testo della casella combinata**

<table id="table_AB60032BF337433F8455DE20AFBA29AB"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Altezza del testo della casella combinata. </p> </td> 
  </tr> 
 </tbody> 
</table>

Esempio: per impostare l&#39;altezza del testo della casella combinata delle dimensioni dell&#39;incorporamento su 40 pixel:

```
.s7ecatalogviewer .s7embeddialog .s7combobox .s7comboboxtext { 
    height: 40px; 
}
```

La casella combinata ha un pulsante a discesa a destra ed è controllata con il seguente selettore di classe CSS:

```
.s7ecatalogviewer .s7embeddialog .s7combobox .s7comboboxbutton
```

**Proprietà CSS del pulsante Casella combinata**

<table id="table_70E127FA21264366AD5DBBD7DF40EBAA"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> top </span> </p> </td> 
   <td colname="col2"> <p>Posizione del pulsante verticale all'interno della casella combinata. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> right </span> </p> </td> 
   <td colname="col2"> <p>Posizione del pulsante orizzontale all'interno della casella combinata. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Larghezza pulsante. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Altezza del pulsante. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image </span> </p> </td> 
   <td colname="col2"> <p>Immagine pulsante per ogni stato. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> Posizionare all'interno dello sprite della grafica, se vengono utilizzati gli spriti CSS. </p> <p>Consultate anche <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-customizingviewer/c-html5-20-ecatalog-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> CSS Sprite </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Questo pulsante supporta il selettore `state` di attributi, che può essere utilizzato per applicare interfacce diverse a stati di pulsante diversi.

Esempio: per impostare un pulsante a discesa su 28x28 pixel e ottenere un’immagine separata per ogni stato:

```
.s7ecatalogviewer .s7embeddialog .s7combobox .s7comboboxbutton { 
 width:28px; 
 height:28px; 
} 
.s7ecatalogviewer .s7embeddialog .s7combobox .s7comboboxbutton[state='up'] { 
 background-image:url(images/sdk/cboxbtndn_up.png); 
} 
.s7ecatalogviewer .s7embeddialog .s7combobox .s7comboboxbutton[state='over'] { 
 background-image:url(images/sdk/cboxbtndn_over.png); 
} 
.s7ecatalogviewer .s7embeddialog .s7combobox .s7comboboxbutton[state='down'] { 
 background-image:url(images/sdk/cboxbtndn_over.png); 
} 
.s7ecatalogviewer .s7embeddialog .s7combobox .s7comboboxbutton[state='disabled'] { 
 background-image:url(images/sdk/cboxbtndn_up.png); 
}
```

Il pannello con l&#39;elenco delle dimensioni di incorporamento visualizzato all&#39;apertura della casella combinata è controllato dal seguente selettore di classe CSS:

```
.s7ecatalogviewer .s7embeddialog .s7comboboxdropdown
```

Le dimensioni e la posizione del pannello sono controllate dal componente. Non è possibile modificarlo tramite CSS.

**Proprietà CSS dell&#39;elenco a discesa della casella combinata**

<table id="table_FA7345321C6A4E63B4B78ECF81CE18DB"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> border </span> </p> </td> 
   <td colname="col2"> <p>Bordo del pannello. </p> </td> 
  </tr> 
 </tbody> 
</table>

Esempio: per impostare il pannello della casella combinata su un bordo grigio di un pixel:

```
.s7ecatalogviewer .s7embeddialog .s7comboboxdropdown { 
    border: 1px solid #CCCCCC; 
}
```

Un singolo elemento in un pannello a discesa controllato dal seguente selettore di classe CSS:

```
.s7ecatalogviewer .s7embeddialog .s7dropdownitemanchor
```

**Proprietà CSS dell&#39;ancoraggio elemento a discesa**

<table id="table_FD42FDD56F89463A97FD292FAA04DA5A"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p>Sfondo elemento. </p> </td> 
  </tr> 
 </tbody> 
</table>

Esempio: per impostare l&#39;elemento del pannello della casella combinata su uno sfondo bianco:

```
.s7ecatalogviewer .s7embeddialog .s7dropdownitemanchor { 
    background-color: #FFFFFF; 
}
```

Un segno di spunta visualizzato a sinistra dell&#39;elemento selezionato all&#39;interno del pannello della casella combinata controllato dal seguente selettore di classe CSS:

```
.s7ecatalogviewer .s7embeddialog .s7checkmark
```

**Proprietà CSS della casella del segno di spunta**

<table id="table_8E01F5461CD04AC18B2C3725A961476A"> 
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
   <td colname="col2"> <p>Immagine elemento. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> Posizionare all'interno dello sprite della grafica, se vengono utilizzati gli spriti CSS. </p> <p>Consultate anche <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-customizingviewer/c-html5-20-ecatalog-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> CSS Sprite </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

Esempio: per impostare l’icona del segno di spunta su 25 x 25 pixel:

```
.s7ecatalogviewer .s7embeddialog .s7checkmark { 
    background-image: url("images/sdk/cboxchecked.png"); 
    height: 25px; 
    width: 25px; 
}
```

Quando l&#39;opzione &quot;Dimensioni personalizzate&quot; è selezionata nella casella combinata Dimensione incorporamento, nella finestra di dialogo vengono visualizzati due campi di input aggiuntivi a destra per consentire all&#39;utente di immettere una dimensione di incorporamento personalizzata. Tali campi sono racchiusi in un contenitore controllato dal seguente selettore di classe CSS:

```
.s7ecatalogviewer .s7embeddialog .s7dialogcustomsizepanel
```

**Proprietà CSS del pannello delle dimensioni personalizzate della finestra di dialogo**

<table id="table_B00829EA550F4E5E8F51B1C6ADACCD34"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> left </span> </p> </td> 
   <td colname="col2"> <p> Distanza dalla casella combinata Dimensione incorpora. </p> </td> 
  </tr> 
 </tbody> 
</table>

Esempio: per impostare la dimensione personalizzata del pannello dei campi di immissione su 20 pixel a destra della casella combinata:

```
.s7ecatalogviewer .s7embeddialog .s7dialogcustomsizepanel { 
    left: 20px; 
}
```

Ogni campo di immissione delle dimensioni personalizzate viene racchiuso in un contenitore che esegue il rendering di un bordo e imposta il margine tra i campi. È controllato dal seguente selettore di classe CSS:

```
.s7ecatalogviewer .s7embeddialog .s7dialogcustomsize
```

**Dimensioni personalizzate delle proprietà CSS della finestra di dialogo**

<table id="table_A8A04BE1988641618D0A412B8AEEE1C5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> border </span> </p> </td> 
   <td colname="col2"> <p>Bordo intorno al campo di input. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p> Larghezza campo di input. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin </span> </p> </td> 
   <td colname="col2"> <p> Margine campo di input. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> spaziatura </span> </p> </td> 
   <td colname="col2"> <p> Margine campo di input. </p> </td> 
  </tr> 
 </tbody> 
</table>

Esempio: per impostare i campi di immissione delle dimensioni personalizzate in modo che abbiano un bordo grigio di un pixel, un margine, una spaziatura e una larghezza di 70 pixel:

```
.s7ecatalogviewer .s7embeddialog .s7dialogcustomsize { 
    border: 1px solid #CCCCCC; 
    margin-right: 20px; 
    padding-left: 2px; 
    padding-right: 2px; 
    width: 70px; 
}
```

Se è necessario lo scorrimento verticale, la barra di scorrimento viene riprodotta nel pannello vicino al bordo destro della finestra di dialogo, controllata dal seguente selettore di classe CSS:

```
.s7ecatalogviewer .s7embeddialog .s7dialogscrollpanel
```

**Proprietà CSS del pannello di scorrimento della finestra di dialogo**

<table id="table_BA37E577E0884C919383F84080E2DD28"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Larghezza del pannello di scorrimento. </p> </td> 
  </tr> 
 </tbody> 
</table>

Esempio: per impostare un pannello di scorrimento con una larghezza di 44 pixel

```
.s7ecatalogviewer .s7embeddialog .s7dialogscrollpanel { 
    width: 44px; 
}
```

L&#39;aspetto dell&#39;area della barra di scorrimento è controllato dal seguente selettore di classe CSS:

```
.s7ecatalogviewer .s7embeddialog .s7scrollbar
```

**Proprietà CSS della barra di scorrimento**

<table id="table_066492417FCA43929017993D7326CDB8"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Larghezza barra di scorrimento. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> top </span> </p> </td> 
   <td colname="col2"> <p> L’offset verticale della barra di scorrimento dalla parte superiore del pannello di scorrimento. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> bottom </span> </p> </td> 
   <td colname="col2"> <p> L’offset verticale della barra di scorrimento dal fondo del pannello di scorrimento. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> right </span> </p> </td> 
   <td colname="col2"> <p> L’offset della barra di scorrimento orizzontale rispetto al bordo destro del pannello di scorrimento. </p> </td> 
  </tr> 
 </tbody> 
</table>

Esempio: per impostare una barra di scorrimento larga 28 pixel e con un margine di otto pixel rispetto ai lati superiore, destro e inferiore del pannello di scorrimento:

```
.s7ecatalogviewer .s7embeddialog .s7scrollbar { 
    bottom: 8px; 
    right: 8px; 
    top: 8px; 
    width: 28px; 
}
```

La traccia della barra di scorrimento è l&#39;area compresa tra i pulsanti di scorrimento superiore e inferiore. Il componente imposta automaticamente la posizione e l’altezza della traccia. La traccia è controllata con il seguente selettore di classe CSS

```
.s7ecatalogviewer .s7embeddialog .s7scrollbar .s7scrolltrack
```

**Proprietà CSS della traccia della barra di scorrimento**

<table id="table_19CF5503C1D34ED9998D4F4A6DA7D5D5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Larghezza traccia. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p> Colore di sfondo del brano. </p> </td> 
  </tr> 
 </tbody> 
</table>

Esempio: per impostare una traccia della barra di scorrimento larga 28 pixel e con uno sfondo grigio:

```
.s7ecatalogviewer .s7embeddialog .s7scrollbar .s7scrolltrack { 
width:28px; 
background-color: #B2B2B2; 
}
```

La barra di scorrimento si sposta verticalmente all’interno di un’area della traccia di scorrimento. La sua posizione verticale è completamente controllata dalla logica del componente. Tuttavia, l&#39;altezza delle miniature non cambia in modo dinamico a seconda della quantità di contenuto. L&#39;altezza del pollice e altri aspetti possono essere configurati con il seguente selettore di classe CSS:

```
.s7ecatalogviewer .s7embeddialog .s7scrollbar .s7scrollthumb
```

**Proprietà CSS della casella di scorrimento**

<table id="table_90BC468FE138441C9DBAB1EB109F3DB0"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Larghezza pollice. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Altezza pollice. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> riempimento superiore </span> </p> </td> 
   <td colname="col2"> <p>Spaziatura verticale tra la parte superiore della traccia. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> imbottitura in basso </span> </p> </td> 
   <td colname="col2"> <p> Spaziatura verticale tra il fondo della traccia. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image </span> </p> </td> 
   <td colname="col2"> <p> Immagine visualizzata per un determinato stato di pollice. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> Posizionare all'interno dello sprite della grafica, se vengono utilizzati gli spriti CSS. </p> <p>Consultate anche <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-customizingviewer/c-html5-20-ecatalog-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> CSS Sprite </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Il pulsante di opzione Miniatura supporta il selettore `state` attributo, che può essere utilizzato per applicare interfacce diverse a diversi stati dei pollici: `up`, `down`, `over`e `disabled`.

Esempio: per impostare una miniatura della barra di scorrimento di 28 x 45 pixel, ha un margine di dieci pixel in alto e in basso e un’immagine diversa per ogni stato:

```
.s7ecatalogviewer .s7embeddialog .s7scrollbar .s7scrollthumb { 
    height: 45px; 
    padding-bottom: 10px; 
    padding-top: 10px; 
    width: 28px; 
} 
.s7ecatalogviewer .s7embeddialog .s7scrollbar .s7scrollthumb[state="up"] { 
 background-image:url("images/sdk/scrollbar_thumb_up.png"); 
} 
.s7ecatalogviewer .s7embeddialog .s7scrollbar .s7scrollthumb[state="down"] { 
 background-image:url("images/sdk/scrollbar_thumb_down.png"); 
} 
.s7ecatalogviewer .s7embeddialog .s7scrollbar .s7scrollthumb[state="over"] { 
 background-image:url("images/sdk/scrollbar_thumb_over.png"); 
} 
.s7ecatalogviewer .s7embeddialog .s7scrollbar .s7scrollthumb[state="disabled"] { 
 background-image:url("images/sdk/scrollbar_thumb_disabled.png"); 
}
```

L&#39;aspetto dei pulsanti di scorrimento superiore e inferiore è controllato dai seguenti selettori di classe CSS:

```
.s7ecatalogviewer .s7embeddialog .s7scrollbar .s7scrollupbutton
```

```
.s7ecatalogviewer .s7embeddialog .s7scrollbar .s7scrolldownbutton
```

Non è possibile posizionare i pulsanti di scorrimento utilizzando CSS `top`, `left`, `bottom`e `right` proprietà. Al contrario, la logica del visualizzatore li posiziona automaticamente.

**Proprietà CSS dei pulsanti di scorrimento superiore e inferiore**

<table id="table_554BFCFEAF4F43A9AE5F741DC126F833"> 
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
   <td colname="col1"> <p> <span class="codeph"> background-image </span> </p> </td> 
   <td colname="col2"> <p> Immagine visualizzata per un determinato stato del pulsante. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> Posizionare all'interno dello sprite della grafica, se vengono utilizzati gli spriti CSS. </p> <p>Consultate anche <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-customizingviewer/c-html5-20-ecatalog-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> CSS Sprite </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Questi pulsanti supportano il selettore di `state` attributi, che può essere utilizzato per applicare interfacce diverse a diversi stati del pulsante: `up`, `down`, `over`e `disabled`.

Le descrizioni dei pulsanti possono essere localizzate. Per ulteriori informazioni, consultate [Localizzazione degli elementi](../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) dell&#39;interfaccia utente.

Esempio: per impostare pulsanti di scorrimento con 28 x 32 pixel e un’immagine diversa per ogni stato:

```
.s7ecatalogviewer .s7embeddialog .s7scrollbar .s7scrollupbutton { 
 width:28px; 
 height:32px; 
} 
.s7ecatalogviewer .s7embeddialog .s7scrollbar .s7scrollupbutton[state='up'] { 
background-image:url(images/sdk/scroll_up_up.png); 
} 
.s7ecatalogviewer .s7embeddialog .s7scrollbar .s7scrollupbutton[state='over'] { 
 background-image:url(images/sdk/scroll_up_over.png); 
} 
.s7ecatalogviewer .s7embeddialog .s7scrollbar .s7scrollupbutton[state='down'] { 
 background-image:url(images/sdk/scroll_up_down.png); 
} 
.s7ecatalogviewer .s7embeddialog .s7scrollbar .s7scrollupbutton[state='disabled'] { 
 background-image:url(images/sdk/scroll_up_disabled.png); 
} 
.s7ecatalogviewer .s7embeddialog .s7scrollbar .s7scrolldownbutton { 
 width:28px; 
 height:32px; 
} 
.s7ecatalogviewer .s7embeddialog .s7scrollbar .s7scrolldownbutton[state='up'] { 
 background-image:url(images/sdk/scroll_down_up.png); 
} 
.s7ecatalogviewer .s7embeddialog .s7scrollbar .s7scrolldownbutton[state='over'] { 
 background-image:url(images/sdk/scroll_down_over.png); 
} 
.s7ecatalogviewer .s7embeddialog .s7scrollbar .s7scrolldownbutton[state='down'] { 
 background-image:url(images/sdk/scroll_down_down.png); 
} 
.s7ecatalogviewer .s7embeddialog .s7scrollbar .s7scrolldownbutton[state='disabled'] { 
 background-image:url(images/sdk/scroll_down_disabled.png); 
}
```

