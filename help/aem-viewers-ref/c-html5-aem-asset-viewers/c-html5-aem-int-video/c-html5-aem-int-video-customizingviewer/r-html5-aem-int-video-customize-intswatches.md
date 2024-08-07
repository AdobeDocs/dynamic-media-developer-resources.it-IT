---
title: Campioni interattivi
description: Il pannello campioni interattivi viene visualizzato accanto al contenuto video se i dati interattivi sono stati passati al visualizzatore nella configurazione. È costituito da un banner nella parte superiore che esegue il rendering del testo, ad esempio "Fai clic per visualizzare", una colonna di uno o più campioni interattivi e due pulsanti di scorrimento (disponibili solo sui sistemi desktop).
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: c9ef02eb-f5db-474b-b234-c49508e2af35
source-git-commit: 6aaf4eccf51a05d200c6cc780e342be646d104d8
workflow-type: tm+mt
source-wordcount: '888'
ht-degree: 0%

---

# Campioni interattivi{#interactive-swatches}

Il pannello campioni interattivi viene visualizzato accanto al contenuto video se i dati interattivi sono stati passati al visualizzatore nella configurazione. È costituito da un banner nella parte superiore che esegue il rendering del testo, ad esempio &quot;Fai clic per visualizzare&quot;, una colonna di uno o più campioni interattivi e due pulsanti di scorrimento (disponibili solo sui sistemi desktop).

<!--<a id="section_235621A1533A49AAADB64A7C3191F735"></a>-->

Sui sistemi desktop e sui dispositivi touch, in orientamento orizzontale, i campioni interattivi vengono riprodotti verticalmente a destra del contenuto video. Sui dispositivi touch con orientamento verticale, vengono visualizzati nella parte inferiore del visualizzatore, come una riga orizzontale di campioni.

Il seguente selettore di classe CSS controlla la posizione e l’orientamento del pannello dei campioni interattivi:

```
.s7interactivevideoviewer .s7interactiveswatches
```

## Proprietà CSS dei campioni interattivi {#css-properties-of-the-interactive-swatches}

<table id="table_352DAD495AE742E39B4F12629C43F712"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> larghezza </span> </p> </td> 
   <td colname="col2"> <p>Larghezza del pannello dei campioni interattivi </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> altezza </span> </p> </td> 
   <td colname="col2"> <p>Altezza del pannello dei campioni interattivi. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> primi </span> </p> </td> 
   <td colname="col2"> <p>Posizione superiore del pannello dei campioni interattivi. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> in basso </span> </p> </td> 
   <td colname="col2"> <p>Posizione inferiore del pannello dei campioni interattivi. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ha lasciato </span> </p> </td> 
   <td colname="col2"> <p>Posizione sinistra del pannello dei campioni interattivi. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> a destra </span> </p> </td> 
   <td colname="col2"> <p>Posizione destra nel pannello dei campioni interattivi. </p> </td> 
  </tr> 
 </tbody> 
</table>

La posizione in fase di esecuzione e l’orientamento del pannello dei campioni interattivi sono definiti da una combinazione delle proprietà CSS sopra riportate, come segue:

* Per eseguire il rendering orizzontale dei campioni interattivi nella parte inferiore del visualizzatore, impostate l&#39;altezza su un valore in pixel assoluto; sinistra e inferiore su 0 px; larghezza, destra e superiore su auto.
* Per eseguire il rendering dei campioni interattivi in verticale a destra del contenuto video, imposta la larghezza su un pixel assoluto; da destra e dall&#39;alto a 0 px; da altezza, da sinistra e dal basso a automatico.

Con questo stile è possibile utilizzare marcatori CSS per ottenere il posizionamento adattivo del pannello dei campioni interattivo.

## Esempio {#example}

Impostare un pannello di campioni interattivo per il rendering orizzontale nella parte inferiore del visualizzatore sui dispositivi touch con orientamento orizzontale. E, per mostrarlo verticalmente a destra del contenuto video in tutti gli altri casi:

```
.s7interactivevideoviewer.s7touchinput.s7device_landscape .s7interactiveswatches, 
.s7interactivevideoviewer.s7mouseinput .s7interactiveswatches { 
 width:120px; 
 height:auto; 
 right:0px; 
 top:0px; 
 left:auto; 
 bottom:auto; 
} 
.s7interactivevideoviewer.s7touchinput.s7device_portrait .s7interactiveswatches { 
 width:auto; 
 height:136px; 
 right:auto; 
 top:auto; 
 left:0px; 
 bottom:0px; 
}
```

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

Le dimensioni e la posizione del banner vengono gestite dal componente campioni interattivi in base ad altri stili applicati con gli stili CSS e non possono essere impostate in modo esplicito.

Il seguente selettore di classe CSS controlla l&#39;aspetto del pannello del banner:

```
.s7interactivevideoviewer .s7interactiveswatches .s7banner
```

## Proprietà CSS del pannello banner {#css-properties-of-the-banner-panel}

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> colore di sfondo </span> </p> </td> 
   <td colname="col2"> <p>Colore di sfondo del pannello del banner. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> colore </span> </p> </td> 
   <td colname="col2"> <p>Colore del testo nel pannello del banner. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> bordo </span> </p> </td> 
   <td colname="col2"> <p>Bordo intorno al pannello del banner. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-weight </span> </p> </td> 
   <td colname="col2"> <p>Spessore del font da utilizzare per il testo all'interno del pannello del banner. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size </span> </p> </td> 
   <td colname="col2"> <p>Dimensione font da utilizzare per il testo all'interno del pannello del banner. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> famiglia di caratteri </span> </p> </td> 
   <td colname="col2"> <p>Famiglia di font da utilizzare per il testo all'interno del pannello del banner. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> allineamento font </span> </p> </td> 
   <td colname="col2"> <p>Allineamento del font da utilizzare per il testo all'interno del pannello del banner. </p> </td> 
  </tr> 
 </tbody> 
</table>

La descrizione del banner può essere localizzata. Per ulteriori informazioni, vedere [Localizzazione degli elementi dell&#39;interfaccia utente](../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74).

## Esempio {#section-e8caea0a303c425a8a637c2a47c06355}

Per impostare un banner con sfondo grigio scuro, bordo grigio più chiaro di due pixel e testo bianco centrato orizzontalmente:

```
.s7interactivevideoviewer .s7interactiveswatches .s7banner { 
    background-color: #222222; 
    border-bottom: 2px solid #444444; 
    color: #ffffff; 
    text-align: center; 
}
```

Il seguente selettore di classe CSS controlla l’aspetto dei campioni:

```
.s7interactivevideoviewer .s7interactiveswatches .s7swatches
```

## Proprietà CSS dell&#39;area campioni {#css-properties-of-the-swatches-area}

<table id="table_45E98E96B07246CAA5D3076FAF62A0B3"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> colore di sfondo </span> </p> </td> 
   <td colname="col2"> <p>Colore di sfondo dell'area dei campioni. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Esempio {#section-9cadd62a09fd44a280f55ff42437e416}

Per impostare l&#39;area dei campioni con sfondo grigio scuro:

```
.s7interactivevideoviewer .s7interactiveswatches .s7swatches { 
    background-color: #222222; 
}
```

Il seguente selettore di classe CSS controlla la spaziatura tra le miniature dei campioni:

`.s7interactivevideoviewer .s7interactiveswatches .s7swatches .s7thumbcell`

## Proprietà CSS per la spaziatura delle miniature dei campioni {#css-properties-of-the-swatches-thumbnail-spacing}

<table id="table_FE6A749EA3894956998D50EA4AB6497B"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margine </span> </p> </td> 
   <td colname="col2"> <p> Dimensione del margine orizzontale e verticale intorno a ciascuna miniatura. La spaziatura effettiva delle miniature è uguale alla somma dei margini sinistro e destro impostati per <span class="codeph"> .s7thumbcell </span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Esempio {#section-39fb270b7e494a9d99e6e8f6890ec53c}

Per impostare la spaziatura verticale su dieci pixel:

```
.s7interactivevideoviewer .s7interactiveswatches .s7swatches .s7thumbcell { 
 margin: 5px; 
}
```

Il seguente selettore di classe CSS controlla l’aspetto delle singole miniature:

`.s7interactivevideoviewer .s7interactiveswatches .s7swatches .s7thumb`

## Proprietà CSS dell&#39;aspetto delle singole miniature {#css-properties-of-the-appearance-of-individual-thumbnails}

<table id="table_FB760FE6BEA44E129C07DD912C86DE57"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> larghezza </span> </p> </td> 
   <td colname="col2"> <p>Larghezza della miniatura. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> altezza </span> </p> </td> 
   <td colname="col2"> <p>Altezza della miniatura. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> bordo </span> </p> </td> 
   <td colname="col2"> <p>Bordo della miniatura. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>La miniatura supporta il selettore di attributi `state`, che è possibile utilizzare per applicare interfacce diverse a stati di miniatura diversi. In particolare, `state="selected"` corrisponde alla miniatura per l&#39;immagine attualmente selezionata; `state="default"` corrisponde al resto delle miniature; `state="over"` viene utilizzato al passaggio del mouse.

## Esempio {#section-69fec189ffaa440b97b6b846c320b75b}

Per impostare miniature di 100 x 75 pixel:

```
.s7interactivevideoviewer .s7interactiveswatches .s7swatches .s7thumb { 
 width:100px; 
 height:75px; 
}
```

Il seguente selettore di classe CSS controlla l’aspetto dell’etichetta della miniatura:

`.s7interactivevideoviewer .s7interactiveswatches .s7swatches .s7label`

## Proprietà CSS dell’aspetto dell’etichetta della miniatura {#css-properties-of-the-appearance-of-the-thumbnail-label}

<table id="table_81B3209FB8124FFA9DB81FD35717900D"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> colore </span> </p> </td> 
   <td colname="col2"> <p>Colore testo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> bordo </span> </p> </td> 
   <td colname="col2"> <p>Bordo etichetta. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> allinea testo </span> </p> </td> 
   <td colname="col2"> <p>Allineamento orizzontale del testo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> famiglia di caratteri </span> </p> </td> 
   <td colname="col2"> <p>Nome font. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Esempio {#section-eb141eb6c1154183baa69796edb90536}

Per impostare le etichette in modo da utilizzare caratteri Helvetica® bianchi, allineati a sinistra e con 12 pixel e un bordo inferiore:

```
.s7interactivevideoviewer .s7interactiveswatches .s7swatches .s7label { 
 border-bottom: 1px solid #e9e9e9; 
 text-align: left; 
color: #ffffff; 
font-family: Helvetica,sans-serif; 
font-size: 12px; 
}
```

Il seguente selettore di classe CSS controlla l&#39;aspetto dei pulsanti di scorrimento verso l&#39;alto e verso il basso:

`.s7interactivevideoviewer .s7interactiveswatches .s7scrollupbutton`

`.s7interactivevideoviewer .s7interactiveswatches .s7scrolldownbutton`

Non è possibile posizionare i pulsanti di scorrimento utilizzando le proprietà CSS `top`, `left`, `bottom` e `right`, ma la logica del visualizzatore li posiziona automaticamente.

## Proprietà CSS dell&#39;aspetto dei pulsanti di scorrimento verso l&#39;alto e verso il basso {#css-properties-of-the-appearance-of-the-up-and-down-scroll-buttons}

<table id="table_48AF27AFBB1543288D45449D6900675C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> larghezza </span> </p> </td> 
   <td colname="col2"> <p>Larghezza del pulsante di scorrimento. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> altezza </span> </p> </td> 
   <td colname="col2"> <p>Altezza del pulsante di scorrimento. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> immagine di sfondo </span> </p> </td> 
   <td colname="col2"> <p>Immagine visualizzata per un determinato stato del pulsante. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p>La posizione all'interno dello sprite del disegno, se vengono utilizzati sprite CSS. </p> <p>Vedere anche <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-customizingviewer/c-html5-aem-int-video-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> sprite CSS </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Questo pulsante supporta il selettore di attributi `state`, che è possibile utilizzare per applicare interfacce diverse agli stati dei pulsanti: &quot; `up`&quot;, &quot; `down`&quot;, &quot; `over`&quot; e &quot; `disabled`&quot;.

Le descrizioni dei pulsanti possono essere localizzate. Per ulteriori informazioni, vedere [Localizzazione degli elementi dell&#39;interfaccia utente](../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74).

## Esempio {#section-e6ce4fa084b84288bc7583342b2c510c}

Per impostare un pulsante di scorrimento verso l&#39;alto di 60 x 36 pixel, avere un disegno diverso per ciascuno stato e prendere tale disegno dall&#39;immagine di sprite del componente:

```
.s7interactivevideoviewer .s7interactiveswatches .s7scrollupbutton { 
 background-size: 120px; 
 width: 60px; 
 height: 36px;  
} 
.s7interactivevideoviewer .s7interactiveswatches .s7scrollupbutton[state] { 
 background-image: url(images/v2/InteractiveSwatches_light_sprite.png); 
} 
.s7interactivevideoviewer .s7interactiveswatches .s7scrollupbutton[state='up'] { background-position: -60px -684px; } 
.s7interactivevideoviewer .s7interactiveswatches .s7scrollupbutton[state='over'] { background-position: -0px -684px; } 
.s7interactivevideoviewer .s7interactiveswatches .s7scrollupbutton[state='down'] { background-position: -60px -648px; } 
.s7interactivevideoviewer .s7interactiveswatches .s7scrollupbutton[state='disabled'] { background-position: -0px -648px; }
```
