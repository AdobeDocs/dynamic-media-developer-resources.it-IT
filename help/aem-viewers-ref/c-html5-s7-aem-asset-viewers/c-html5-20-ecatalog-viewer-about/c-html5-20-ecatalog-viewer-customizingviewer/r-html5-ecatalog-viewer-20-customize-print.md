---
title: Stampa
description: Stampa strumento è costituito da un pulsante aggiunto alla barra di controllo e dalla finestra di dialogo modale che viene visualizzata quando viene attivato il strumento.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: 25057e72-f079-4221-91c2-760d99d30633
source-git-commit: 97fbf820590b53de5a1e6ce904e44d6b0ef9a214
workflow-type: tm+mt
source-wordcount: '1488'
ht-degree: 0%

---

# Stampa{#print}

Stampa strumento è costituito da un pulsante aggiunto alla barra di controllo e dalla finestra di dialogo modale che viene visualizzata quando viene attivato il strumento.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

L&#39;aspetto del pulsante di stampa è controllato con la seguente classe CSS selettore:

```
.s7ecatalogsearchviewer .s7print
```

**Proprietà CSS del pulsante di stampa**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Margine superiore </span> </p> </td> 
   <td colname="col2"> <p> Offset dalla parte superiore della barra di controllo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Margine sinistro </span> </p> </td> 
   <td colname="col2"> <p> La distanza dalla pulsante successiva a sinistra o sul lato sinistro della barra di controllo se è la prima pulsante di fila. </p> </td> 
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
   <td colname="col2"> <p> Immagine visualizzata per uno stato pulsante specificato. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> posizione sfondo </span> </p> </td> 
   <td colname="col2"> <p> Posizione all'interno dello sprite dell'illustrazione, se vengono utilizzati sprite CSS. </p> <p>Vedere anche <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-customizingviewer/c-html5-ecatsearch-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> sprite CSS </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Questo pulsante supporta il selettore di attributi `state`, che può essere utilizzato per applicare interfacce diverse a diversi stati di pulsante.

La descrizione comando del pulsante può essere localizzata. Per ulteriori informazioni, vedere [Localizzazione degli elementi dell&#39;interfaccia utente](../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74).

Esempio: per impostare un pulsante di stampa di 28 x 28 pixel e visualizzi un&#39;immagine diversa per ciascuno dei quattro diversi stati pulsante.

```
.s7ecatalogsearchviewer .s7print { 
margin-top: 4px; 
margin-left: 10px; 
 width:28px; 
 height:28px; 
} 
.s7ecatalogsearchviewer .s7print[state='up'] { 
background-image:url(images/v2/Print_dark_up.png); 
} 
.s7ecatalogsearchviewer .s7print[state='over'] { 
background-image:url(images/v2/Print_dark_over.png); 
} 
.s7ecatalogsearchviewer .s7print[state='down'] { 
background-image:url(images/v2/Print_dark_down.png); 
} 
.s7ecatalogsearchviewer .s7print[state='disabled'] { 
background-image:url(images/v2/Print_dark_disabled.png); 
}
```

Lo sfondo sovrapposizione che copre la pagina Web quando la finestra di dialogo è attiva, è controllato con la seguente classe CSS selettore:

```
.s7ecatalogsearchviewer .s7printdialog .s7backoverlay
```

**Proprietà CSS del sovrapposizione posteriore**

<table id="table_1A0C28D8C81D413C83D73DEAC53057C5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> opacità </span> </p> </td> 
   <td colname="col2"> <p> Sfondo sovrapposizione opacità. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> colore di sfondo </span> </p> </td> 
   <td colname="col2"> <p>Sfondo colore sovrapposizione. </p> </td> 
  </tr> 
 </tbody> 
</table>

Esempio: per impostare il sovrapposizione di sfondo in grigio con il 70% di opacità:

```
.s7ecatalogsearchviewer .s7printdialog .s7backoverlay { 
 opacity:0.7; 
 background-color:#222222; 
}
```

Per impostazione predefinita, la finestra di dialogo modale viene visualizzata centrata sullo schermo nei sistemi desktop. Il posizionamento e il ridimensionamento della finestra di dialogo sono gestiti dal componente. La finestra di dialogo è controllata con la seguente classe CSS selettore:

```
.s7ecatalogsearchviewer .s7kprintdialog .s7dialog
```

**Proprietà CSS della finestra di dialogo**

<table id="table_5272BC8EF9124018B4290356B95B5559"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> bordo raggio </span> </p> </td> 
   <td colname="col2"> <p> Finestra di dialogo bordo raggio. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> colore di sfondo </span> </p> </td> 
   <td colname="col2"> <p> Colore di sfondo della finestra di dialogo; </p> </td> 
  </tr> 
 </tbody> 
</table>

Esempio - per impostare una finestra di dialogo con uno sfondo grigio:

```
.s7ecatalogsearchviewer .s7printdialog .s7dialog { 
background-color: #dddddd; 
}
```

L&#39;intestazione della finestra di dialogo è costituita da un&#39;icona, un testo del titolo e un pulsante chiuso. Il contenitore dell&#39;intestazione è controllato con la seguente classe CSS selettore:

```
.s7ecatalogsearchviewer .s7printdialog .s7dialogheader
```

**Proprietà CSS dell&#39;intestazione della finestra di dialogo**

<table id="table_E407E844C9BD4B5DA8B5BBDE0554F9CA"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> imbottitura </span> </p> </td> 
   <td colname="col2"> <p> Spaziatura interna per contenuto di intestazione. </p> </td> 
  </tr> 
 </tbody> 
</table>

L&#39;icona e il testo del titolo vengono racchiusi in un contenitore aggiuntivo controllato con quanto segue:

```
.s7ecatalogsearchviewer .s7printdialog .s7dialogheader .s7dialogline
```

**Proprietà CSS della riga di dialogo**

<table id="table_5B03CF843F0D4B1295A3FC1EB50C56F1"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> riempimento </span> </p> </td> 
   <td colname="col2"> <p> Spaziatura interna per l'icona dell'intestazione e il titolo. </p> </td> 
  </tr> 
 </tbody> 
</table>

L&#39;icona dell&#39;intestazione è controllata con la seguente classe CSS selettore:

```
.s7ecatalogsearchviewer .s7printdialog .s7dialogheadericon
```

**Proprietà CSS dell&#39;icona dell&#39;intestazione della finestra di dialogo**

<table id="table_DD4B0413721B49CE8E21B4A55BDE8F7D"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Larghezza </span> </p> </td> 
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
   <td colname="col2"> <p> Posizionate all'interno dello sprite del disegno, se vengono utilizzati gli sprite CSS. </p> <p>Vedere anche <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-customizingviewer/c-html5-ecatsearch-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> sprite CSS </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

Il titolo dell’intestazione è controllato dal seguente selettore di classe CSS:

```
.s7ecatalogsearchviewer .s7printdialog .s7dialogheadertext
```

**Proprietà CSS del testo dell&#39;intestazione della finestra di dialogo**

<table id="table_207B4B13153E425EAB38FC61F382A05F"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-weight </span> </p> </td> 
   <td colname="col2"> <p>Spessore font. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Dimensioni font </span> </p> </td> 
   <td colname="col2"> <p>Altezza font. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-famiglia </span> </p> </td> 
   <td colname="col2"> <p>Famiglia di font. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> imbottitura </span> </p> </td> 
   <td colname="col2"> <p>Spaziatura interna del testo. </p> </td> 
  </tr> 
 </tbody> 
</table>

Chiudi pulsante è controllato con il seguente selettore di classe CSS:

```
.s7ecatalogsearchviewer .s7printdialog .s7closebutton
```

**Proprietà CSS della close pulsante &#x200B;**

<table id="table_FAECBC489FC442588E50E3DA0AC16DD7"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> In alto </span> </p> </td> 
   <td colname="col2"> <p> Posizione di pulsante verticale rispetto al contenitore dell'intestazione. </p> </td> 
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
   <td colname="col2"> <p>Altezza pulsanti. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> imbottitura </span> </p> </td> 
   <td colname="col2"> <p>Spaziatura interna del pulsante. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> immagine di sfondo </span> </p> </td> 
   <td colname="col2"> <p>Immagine pulsante per ogni stato. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> Posizione all'interno dello sprite dell'illustrazione, se vengono utilizzati sprite CSS. </p> <p>Vedere anche <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-customizingviewer/c-html5-ecatsearch-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> CSS Sprites </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Questo pulsante supporta l&#39;attributo `state` selettore, che può essere utilizzato per applicare interfacce diverse a diversi stati pulsante.

Il Chiudi pulsante strumento suggerimento e il titolo della finestra di dialogo può essere localizzato. Per ulteriori informazioni, consulta [Localizzazione di utente elementi](../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) dell&#39;interfaccia.

Esempio: per impostare un&#39;intestazione della finestra di dialogo con spaziatura interna, un&#39;icona di 22 x 22 pixel e un titolo in grassetto di 16 punti. Infine, un Chiudi da 28 x 28 pixel pulsante posizionato a due pixel dalla parte superiore e a due pixel dalla destra del contenitore della finestra di dialogo:

```
.s7ecatalogsearchviewer .s7printdialog .s7dialogheader { 
 padding: 10px; 
} 
.s7ecatalogsearchviewer .s7printdialog .s7dialogheader .s7dialogline { 
 padding: 10px 10px 2px; 
} 
.s7ecatalogsearchviewer .s7printdialog .s7dialogheadericon { 
    background-image: url("images/sdk/dlgprint_cap.png"); 
    height: 22px; 
    width: 22px; 
} 
.s7ecatalogsearchviewer .s7printdialog .s7dialogheadertext { 
    font-size: 16pt; 
    font-weight: bold; 
    padding-left: 16px; 
} 
.s7ecatalogsearchviewer .s7printdialog .s7closebutton { 
 top:2px; 
 right:2px; 
 padding:8px; 
 width:28px; 
 height:28px; 
} 
.s7ecatalogsearchviewer .s7printdialog .s7closebutton[state='up'] { 
 background-image:url(images/sdk/close_up.png); 
} 
.s7ecatalogsearchviewer .s7printdialog .s7closebutton[state='over'] { 
 background-image:url(images/sdk/close_over.png); 
} 
.s7ecatalogsearchviewer .s7printdialog .s7closebutton[state='down'] { 
 background-image:url(images/sdk/close_down.png); 
} 
.s7ecatalogsearchviewer .s7printdialog .s7closebutton[state='disabled'] { 
 background-image:url(images/sdk/close_disabled.png); 
}
```

Il piè di pagina della finestra di dialogo è costituito dai pulsanti Annulla e Invia a Stampa. Il contenitore piè di pagina è controllato con la seguente classe CSS selettore:

```
.s7ecatalogsearchviewer .s7printdialog .s7dialogfooter
```

**Proprietà CSS del piè di pagina della finestra di dialogo &#x200B;**

<table id="table_0AF7AAAB846A46D690896AFD68575669"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> confine </span> </p> </td> 
   <td colname="col2"> <p> Bordo che è possibile utilizzare per separare visivamente il piè di pagina dal resto della finestra di dialogo. </p> </td> 
  </tr> 
 </tbody> 
</table>

Il piè di pagina ha un contenitore interno che contiene entrambi i pulsanti. È controllato con la seguente classe CSS selettore:

```
.s7ecatalogsearchviewer .s7printdialog .s7dialogbuttoncontainer
```

**Proprietà CSS della finestra di dialogo pulsante del contenitore**

<table id="table_C34906888A8145C7A61E503DFC6B08A9"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> imbottitura </span> </p> </td> 
   <td colname="col2"> <p> Spaziatura interna tra il piè di pagina e i pulsanti. </p> </td> 
  </tr> 
 </tbody> 
</table>

Annulla pulsante è controllato con il seguente selettore di classe CSS:

```
.s7ecatalogsearchviewer .s7printdialog .s7dialogcancelbutton
```

**Proprietà CSS della finestra di dialogo Annulla pulsante**

<table id="table_3DFA90B012F345A3A2A123D6856BE08A"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Larghezza </span> </p> </td> 
   <td colname="col2"> <p>Larghezza pulsante. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> altezza </span> </p> </td> 
   <td colname="col2"> <p>Altezza pulsante. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> colore </span> </p> </td> 
   <td colname="col2"> <p> Colore del testo del pulsante per ogni stato. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> colore di sfondo </span> </p> </td> 
   <td colname="col2"> <p> Colore di sfondo del pulsante per ogni stato. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Questo pulsante supporta l&#39;attributo `state` selettore, che può essere utilizzato per applicare interfacce diverse a diversi stati pulsante.

Invia a Stampa pulsante è controllata con il seguente selettore della classe CSS:

```
.s7ecatalogsearchviewer .s7printdialog .s7dialogactionbutton
```

**Proprietà CSS del pulsante di azione della finestra di dialogo**

<table id="table_91C75B2470A24DC2AD3973A91FA8B325"> 
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
>Questo pulsante supporta il selettore di attributi `state`, che può essere utilizzato per applicare interfacce diverse a diversi stati di pulsante.

Inoltre, entrambi i pulsanti condividono la stessa classe CSS che può contenere impostazioni CSS identiche a quelle degli altri pulsanti della finestra di dialogo:

```
.s7ecatalogsearchviewer .s7printdialog .s7dialogfooter .s7button
```

**Proprietà CSS del pulsante**

<table id="table_E735E5EDFC1E4F8A962CEA533A88DD4E"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Peso font </span> </p> </td> 
   <td colname="col2"> <p>Pulsante font peso. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Dimensioni font </span> </p> </td> 
   <td colname="col2"> <p>Pulsante font dimensione. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-famiglia </span> </p> </td> 
   <td colname="col2"> <p>Button font famiglia. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> altezza linea </span> </p> </td> 
   <td colname="col2"> <p> Altezza del testo all'interno del pulsante. Influisce sull'allineamento verticale. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> box-shadow </span> </p> </td> 
   <td colname="col2"> <p>Ombra. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margine destro </span> </p> </td> 
   <td colname="col2"> <p>Margine pulsante destro. </p> </td> 
  </tr> 
 </tbody> 
</table>

Le descrizioni dei pulsanti possono essere localizzate. Per ulteriori informazioni, vedere [Localizzazione degli elementi dell&#39;interfaccia utente](../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74).

Esempio: per impostare un piè di pagina della finestra di dialogo con un pulsante di 64 x 34 Annulla e un pulsante Invia a Stampa 96 x 34, con il colore del testo e il colore di sfondo diversi per ogni stato pulsante:

```
.s7ecatalogsearchviewer .s7printdialog .s7dialogfooter { 
    border-top: 1px solid #909090; 
} 
.s7ecatalogsearchviewer .s7printdialog .s7dialogbuttoncontainer { 
    padding-bottom: 6px; 
    padding-top: 10px; 
} 
.s7ecatalogsearchviewer .s7printdialog .s7dialogfooter .s7button { 
    box-shadow: 1px 1px 1px #999999; 
    color: #FFFFFF; 
    font-size: 9pt; 
    font-weight: bold; 
    line-height: 34px; 
    margin-right: 10px; 
} 
.s7ecatalogsearchviewer .s7printdialog .s7dialogcancelbutton { 
 width:64px; 
 height:34px; 
} 
.s7ecatalogsearchviewer .s7printdialog .s7dialogcancelbutton[state='up'] { 
 background-color:#666666; 
 color:#dddddd; 
} 
.s7ecatalogsearchviewer .s7printdialog .s7dialogcancelbutton[state='down'] { 
 background-color:#555555; 
 color:#ffffff; 
} 
.s7ecatalogsearchviewer .s7printdialog .s7dialogcancelbutton[state='over'] { 
 background-color:#555555; 
 color:#ffffff; 
} 
.s7ecatalogsearchviewer .s7printdialog .s7dialogcancelbutton[state='disabled'] { 
 background-color:#b2b2b2; 
 color:#dddddd; 
} 
.s7ecatalogsearchviewer .s7printdialog .s7dialogactionbutton { 
 width:96px; 
 height:34px; 
} 
.s7ecatalogsearchviewer .s7printdialog .s7dialogactionbutton[state='up'] { 
 background-color:#333333; 
 color:#dddddd; 
} 
.s7ecatalogsearchviewer .s7printdialog .s7dialogactionbutton[state='down'] { 
 background-color:#222222; 
 color:#cccccc; 
} 
.s7ecatalogsearchviewer .s7printdialog .s7dialogactionbutton[state='over'] { 
 background-color:#222222; 
 color:#cccccc; 
} 
.s7ecatalogsearchviewer .s7printdialog .s7dialogactionbutton[state='disabled'] { 
 background-color:#b2b2b2; 
 color:#dddddd; 
}
```

L&#39;area di dialogo principale, tra l&#39;intestazione e il piè di pagina, contiene contenuto della finestra di dialogo. In tutti i casi, il componente gestisce la larghezza di quest&#39;area, non è possibile impostarlo in CSS. L&#39;area di dialogo principale è controllata dalla seguente classe CSS selettore:

```
.s7ecatalogsearchviewer .s7printdialog .s7dialogviewarea
```

**Proprietà CSS dell&#39;area di visualizzazione della finestra di dialogo &#x200B;**

<table id="table_3FF4691D848A4C4D8EF060B7E79DEEDE"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> altezza </span> </p> </td> 
   <td colname="col2"> <p> Altezza della finestra di dialogo principale. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> colore di sfondo </span> </p> </td> 
   <td colname="col2"> <p>Colore di sfondo dell'area principale della finestra di dialogo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margine </span> </p> </td> 
   <td colname="col2"> <p>Margine esterno. </p> </td> 
  </tr> 
 </tbody> 
</table>

Esempio: per impostare un&#39;area di dialogo principale in modo che abbia un&#39;altezza calcolata automaticamente, abbia un margine di dieci pixel e utilizzi uno sfondo bianco:

```
.s7ecatalogsearchviewer .s7printdialog .s7dialogviewarea { 
 background-color:#ffffff; 
 margin:10px; 
 height:auto; 
}
```

Tutti i contenuto modulo (like etichette e campi di input) risiedono all&#39;interno di un contenitore controllato con la seguente classe CSS selettore:

```
.s7ecatalogsearchviewer .s7printdialog .s7dialogbody
```

**Proprietà CSS del corpo della finestra di dialogo &#x200B;**

<table id="table_5D77F3D5B8CD4B798AA85F722B277F56"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> imbottitura </span> </p> </td> 
   <td colname="col2"> <p>Imbottitura interna. </p> </td> 
  </tr> 
 </tbody> 
</table>

Esempio: per impostare la contenuto del modulo in modo che la spaziatura di dieci pixel sia impostata su dieci pixel:

```
.s7ecatalogsearchviewer .s7printdialog .s7dialogbody { 
    padding: 10px; 
}
```

Il modulo della finestra di dialogo viene compilato riga per riga, dove ogni riga contiene una parte del modulo contenuto (like un&#39;etichetta e un campo di immissione del testo). La linea a forma singola è controllata con la seguente classe CSS selettore:

```
.s7ecatalogsearchviewer .s7emaildialog .s7dialogbody .s7dialogline
```

**Proprietà CSS della riga della finestra di dialogo**

<table id="table_2CCCC71B45B444A8B9CE2894129C9C02"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> imbottitura </span> </p> </td> 
   <td colname="col2"> <p>Imbottitura linea interna. </p> </td> 
  </tr> 
 </tbody> 
</table>

Esempio - per impostare un modulo della finestra di dialogo in modo che abbia dieci pixel di spaziatura per ogni riga:

```
.s7ecatalogsearchviewer .s7emaildialog .s7dialogbody .s7dialogline { 
    padding: 10px; 
}
```

La dimensione del blocco di contenuto finestra di dialogo è controllata con i seguenti selettore di classe CSS:

```
 .s7ecatalogsearchviewer .s7printdialog .s7dialoginputwide
```

**Proprietà CSS della larghezza di input della finestra di dialogo**

<table id="table_FFF0B02B564C443CA8713103D723C733"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Larghezza </span> </p> </td> 
   <td colname="col2"> <p>Larghezza blocco. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> imbottitura </span> </p> </td> 
   <td colname="col2"> <p>Spaziatura interna riga. </p> </td> 
  </tr> 
 </tbody> 
</table>

Esempio: per impostare una larghezza di un blocco di contenuto pari a 430 pixel con una spaziatura inferiore di 10 pixel:

```
.s7ecatalogsearchviewer .s7printdialog .s7dialoginputwide { 
    padding-bottom: 10px; 
    width: 430px; 
}
```

Tutte le etichette statiche nel modulo della finestra di dialogo sono controllate con il seguente selettore di classe CSS:

```
.s7ecatalogsearchviewer .s7printdialog .s7dialoglabel
```

Questa classe non è adatta per controllare le dimensioni o la posizione dell&#39;etichetta perché è possibile applicarla ai testi in varie posizioni nel modulo utente interfaccia.

**Proprietà CSS dell&#39;etichetta della finestra di dialogo. &#x200B;**

<table id="table_13C7874807314ADD83A23075ABB4C340"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Peso font </span> </p> </td> 
   <td colname="col2"> <p>Etichetta font peso. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Dimensioni font </span> </p> </td> 
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

Le etichette delle finestre di dialogo possono essere localizzate. Per ulteriori informazioni, vedere [Localizzazione degli elementi dell&#39;interfaccia utente](../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74).

Esempio: per impostare tutte le etichette in grigio, grassetto, con un carattere di nove pixel:

```
.s7ecatalogsearchviewer .s7printdialog .s7dialoglabel { 
    color: #666666; 
    font-size: 9pt; 
    font-weight: bold; 
}
```

I controlli di input vengono racchiusi nel contenitore e controllati con il seguente selettore di classe CSS:

```
.s7ecatalogsearchviewer .s7printdialog .s7dialoginputcontainer
```

**Proprietà CSS del contenitore di input della finestra di dialogo**

<table id="table_7BC1C5919A54483F8121D928DC63233A"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margine sinistro </span> </p> </td> 
   <td colname="col2"> <p>Imbottitura interna. </p> </td> 
  </tr> 
 </tbody> 
</table>

Esempio: per impostare una spaziatura di 30 pixel dal bordo sinistro della finestra di dialogo.

```
.s7ecatalogsearchviewer .s7printdialog .s7dialoginputcontainer { 
    padding-left: 30px; 
}
```

I pulsanti di scelta e il testo delle didascalie sono controllati con le seguenti selettore di classe CSS:

```
.s7ecatalogsearchviewer .s7printdialog .s7dialogoption
```

**Proprietà CSS dell&#39;opzione della finestra di dialogo**

<table id="table_3B4D85C5A0254A17A34D57F84F8200F7"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Larghezza </span> </p> </td> 
   <td colname="col2"> <p> Larghezza totale della radio pulsante con una didascalia. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Colore </span> </p> </td> 
   <td colname="col2"> <p>Didascalia colore del testo. </p> </td> 
  </tr> 
 </tbody> 
</table>

La spaziatura tra il pulsante radio e la relativa didascalia è controllata con il seguente selettore di classe CSS:

```
.s7ecatalogsearchviewer .s7printdialog .s7dialogoptioninput
```

**Proprietà CSS della finestra di dialogo Input opzione**

<table id="table_BDD03247E594416D93CDF8604DCE937B"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Margine destro </span> </p> </td> 
   <td colname="col2"> <p> Spaziatura tra il pulsante di opzione e la relativa didascalia. </p> </td> 
  </tr> 
 </tbody> 
</table>

I selettori numerici per la selezione dell&#39;intervallo di stampa sono controllati con il seguente selettore di classe CSS

```
.s7ecatalogsearchviewer .s7printdialog .s7dialogrange
```

**Proprietà CSS della finestra di dialogo intervallo di stampa**

<table id="table_35413C16F6B840EBBEEA17890F2A0490"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Larghezza </span> </p> </td> 
   <td colname="col2"> <p> Larghezza del selettore numerico. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margine </span> </p> </td> 
   <td colname="col2"> <p> Spaziatura attorno al selettore numerico. </p> </td> 
  </tr> 
 </tbody> 
</table>

Esempio: per impostare tutti i pulsanti di scelta in modo che abbiano una larghezza di 150 pixel con testo nero, spaziatura di dieci pixel e selettori numerici larghi 42 pixel:

```
.s7ecatalogsearchviewer .s7printdialog .s7dialogoption { 
    color: #000000; 
    width: 150px; 
} 
.s7ecatalogsearchviewer .s7printdialog .s7dialogoption input { 
    margin-right: 10px; 
} 
.s7ecatalogsearchviewer .s7printdialog .s7dialogrange { 
    margin-left: 10px; 
    margin-right: 10px; 
    width: 42px; 
}
```

Il divisore orizzontale tra la selezione dell’intervallo di pagine e le sezioni di layout di stampa è controllato con il seguente selettore di classe CSS:

```
 .s7ecatalogsearchviewer 
.s7printdialog .s7horizontaldivider
```

**Proprietà CSS del divisore orizzontale**

<table id="table_AB42F1DC92BB4946868F0A9FE86ABAA6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> bordo </span> </p> </td> 
   <td colname="col2"> <p> Bordo attorno al divisore. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> riempimento </span> </p> </td> 
   <td colname="col2"> <p>Spaziatura interna. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> larghezza </span> </p> </td> 
   <td colname="col2"> <p>Larghezza divisore. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margine </span> </p> </td> 
   <td colname="col2"> <p>Margine esterno </p> </td> 
  </tr> 
 </tbody> 
</table>

Esempio: per impostare un divisore grigio di 430 pixel di larghezza con un margine verticale di 10 pixel su entrambi i lati e un margine di dieci pixel nella parte superiore:

```
.s7ecatalogsearchviewer .s7printdialog .s7horizontaldivider { 
    border-top: 1px solid #aaaaaa; 
    margin-top: 10px; 
    padding-bottom: 10px; 
    padding-top: 10px; 
    width: 430px; 
}
```
