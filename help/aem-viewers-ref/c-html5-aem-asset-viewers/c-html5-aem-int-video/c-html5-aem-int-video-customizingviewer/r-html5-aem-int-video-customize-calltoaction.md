---
title: Invito all’azione
description: Il pannello Invito all'azione viene visualizzato al termine del video e mostra tutti i campioni interattivi associati a quel particolare video.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: 43e0ffb3-d650-4b79-ab48-2f32b313b832
source-git-commit: 6aaf4eccf51a05d200c6cc780e342be646d104d8
workflow-type: tm+mt
source-wordcount: '1299'
ht-degree: 0%

---

# Invito all’azione{#call-to-action}

Il pannello Invito all&#39;azione viene visualizzato al termine del video e mostra tutti i campioni interattivi associati a quel particolare video.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

Il pannello è costituito da un’area di intestazione che mostra il titolo del video, un pulsante di riproduzione nell’angolo in alto a destra e campioni interattivi effettivi visualizzati come griglia scorrevole. È possibile disattivare il pannello utilizzando l&#39;attributo di configurazione [callToActionRecap](../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/r-html5-aem-int-video-config-attrib/r-html5-aem-int-video-config-attrib-calltoactionrecap.md#reference-3720b68800684ddabf523e9d81644ce6).

Il pannello di invito all’azione occupa sempre l’intera area di visualizzazione disponibile.

<!--<a id="section_3A619BE925C04AFA87A6B7846C5C7E2B"></a>-->

Il seguente selettore di classe CSS controlla l’aspetto del colore di sfondo nel pannello di invito all’azione:

```
.s7interactivevideoviewer .s7calltoaction
```

## Proprietà CSS del colore di sfondo del pannello di invito all’azione {#css-properties-of-the-background-color-of-the-call-to-action-panel}

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> colore di sfondo </span> </p> </td> 
   <td colname="col2"> <p> Colore di sfondo del pannello di invito all’azione. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Esempio {#example}

Per impostare un pannello di invito all’azione con sfondo grigio scuro:

```
.s7interactivevideoviewer .s7calltoaction { 
    background-color: #222222; 
}
```

<!--<a id="section_AD18C770788B49989BEDAA608ECA804C"></a>-->

Il seguente selettore di classe CSS controlla l’aspetto dell’intestazione nel pannello di invito all’azione:

```
.s7interactivevideoviewer .s7calltoaction .s7header
```

## Proprietà CSS dell’intestazione del pannello di invito all’azione {#css-properties-of-the-call-to-action-panel-header}

<table id="table_DAA1770AB3074845B5E1B700CD6FC18A"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> colore di sfondo </span> </p> </td> 
   <td colname="col2"> <p>Colore di sfondo dell’intestazione. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> altezza </span> </p> </td> 
   <td colname="col2"> <p>Altezza dell'intestazione. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> border-bottom </span> </p> </td> 
   <td colname="col2"> <p>Bordo inferiore dell’intestazione. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Esempio {#example-1}

Per impostare un&#39;intestazione alta 70 pixel, con uno sfondo grigio scuro e un bordo grigio leggermente più chiaro di due pixel lungo il fondo:

```
.s7interactivevideoviewer .s7calltoaction .s7header { 
    height: 70px; 
    border-bottom: 2px solid #444444; 
    background-color: #222222; 
}
```

<!--<a id="section_B0333FC1A2CC4E089C68D34B839E5156"></a>-->

Il seguente selettore di classe CSS controlla l’aspetto del titolo dell’intestazione nel pannello di invito all’azione:

```
.s7interactivevideoviewer .s7calltoaction .s7header .s7title
```

## Proprietà CSS del titolo dell’intestazione nel pannello di invito all’azione:  {#css-properties-of-the-header-title-in-the-call-to-action-panel}

<table id="table_A5E36A5C4C664346B6DAE9A02B36C3D2"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> colore </span> </p> </td> 
   <td colname="col2"> <p> Colore del testo all'interno del banner. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size </span> </p> </td> 
   <td colname="col2"> <p>Dimensione font. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> altezza riga </span> </p> </td> 
   <td colname="col2"> <p>Altezza riga. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> famiglia di caratteri </span> </p> </td> 
   <td colname="col2"> <p> Famiglia di caratteri. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> allinea testo </span> </p> </td> 
   <td colname="col2"> <p>Allineamento del testo nel banner. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margine sinistro </span> </p> </td> 
   <td colname="col2"> <p>Margine sinistro. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> riempimento a destra </span> </p> </td> 
   <td colname="col2"> <p> Spaziatura interna a destra per consentire lo spazio per il pulsante Ripeti. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Esempio {#example-2}

Per impostare un titolo video con un&#39;altezza della linea di 70 pixel, una dimensione del carattere di 25 pixel, un colore bianco e un allineamento a sinistra:

```
.s7interactivevideoviewer .s7calltoaction .s7header .s7title { 
    line-height: 70px; 
    font-size: 25px; 
    color: #ffffff; 
    text-align: left; 
}
```

<!--<a id="section_D23A6D4BA0614286A060982B359E3C08"></a>-->

Il seguente selettore di classe CSS controlla l’aspetto del pulsante Chiudi nel pannello di invito all’azione:

```
.s7interactivevideoviewer .s7calltoaction .s7closebutton
```

## Proprietà CSS del pulsante Chiudi nel pannello di invito all’azione: {#css-properties-of-the-close-button-in-the-call-to-action-panel}

<table id="table_CB0BCBE70DB447BC8D31034A96308924"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> primi </span> </p> </td> 
   <td colname="col2"> <p>Posizione dalla parte superiore dell’intestazione, inclusa la spaziatura. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> a destra </span> </p> </td> 
   <td colname="col2"> <p>Posizione a destra dell'intestazione, inclusa la spaziatura. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> larghezza </span> </p> </td> 
   <td colname="col2"> <p>Larghezza pulsante. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> altezza </span> </p> </td> 
   <td colname="col2"> <p> Altezza pulsante. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> immagine di sfondo </span> </p> </td> 
   <td colname="col2"> <p>Immagine visualizzata per un determinato stato del pulsante. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p>Posizione all'interno dello sprite del disegno, se vengono utilizzati sprite CSS. </p> <p>Vedere <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-customizingviewer/c-html5-aem-int-video-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> sprite CSS </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Questo pulsante supporta il selettore di attributi `state`, che può essere utilizzato per applicare interfacce diverse a diversi stati di pulsante.

## Esempio {#example-3}

Per impostare un pulsante di riproduzione di 28 x 28 pixel. Il pulsante deve essere posizionato a 20 pixel dal bordo superiore e da quello destro dell’intestazione. Inoltre, deve visualizzare un’immagine diversa per ciascuno dei quattro diversi stati dei pulsanti; prende il disegno dall’immagine di sprite del componente:

```
.s7interactivevideoviewer .s7calltoaction .s7closebutton { 
 top: 20px; 
 right: 20px; 
 background-size: 336px; 
 width: 28px; 
 height: 28px;  
} 
.s7interactivevideoviewer .s7calltoaction .s7closebutton[state] { 
 background-image: url(images/v2/PlayPauseButton_sprite.png); 
} 
.s7interactivevideoviewer .s7calltoaction .s7closebutton[state='up'] { 
 background-position: -28px -1260px; 
} 
.s7interactivevideoviewer .s7calltoaction .s7closebutton[state='over'] { 
 background-position: -0px -1260px; 
} 
.s7interactivevideoviewer .s7calltoaction .s7closebutton[state='down'] { 
 background-position: -28px -1232px; 
} 
.s7interactivevideoviewer .s7calltoaction .s7closebutton[state='disabled'] { 
 background-position: -0px -1232px; 
}
```

<!--<a id="section_3975B58E78DE4E81B469372FB8A3A348"></a>-->

Il seguente selettore di classe CSS controlla l’aspetto della visualizzazione della griglia delle miniature nel pannello di invito all’azione:

```
.s7interactivevideoviewer .s7calltoaction .s7thumbnailgridview
```

## Proprietà CSS della visualizzazione griglia miniature nel pannello invito all’azione:  {#css-properties-of-the-thumbnail-grid-view-in-the-call-to-action-panel}

<table id="table_A0DDD21C84944D48A639F51FCC8DF065"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> colore di sfondo </span> </p> </td> 
   <td colname="col2"> <p>Colore di sfondo dell'area delle miniature. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Esempio {#example-4}

Per impostare un&#39;area delle miniature con uno sfondo grigio scuro:

```
.s7interactivevideoviewer .s7calltoaction .s7thumbnailgridview { 
    background-color: #222222; 
}
```

<!--<a id="section_D2E5AADFCE0345468DC0D2977E2765D2"></a>-->

Il seguente selettore di classe CSS controlla l’aspetto della cella miniatura nel pannello di invito all’azione:

```
.s7interactivevideoviewer .s7calltoaction .s7thumbcell
```

## Proprietà CSS della cella miniatura nel pannello di invito all’azione: {#css-properties-of-the-thumbcell-in-the-call-to-action-panel}

<table id="table_9CEBEF6FC7024F02840A581AEEF612B4"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margine </span> </p> </td> 
   <td colname="col2"> <p> Dimensioni del margine orizzontale e verticale intorno a ciascuna miniatura. </p> <p>La spaziatura effettiva delle miniature orizzontale è uguale alla somma del margine sinistro e destro impostato per <span class="codeph"> .s7thumbcell </span>. La stessa regola si applica anche alla spaziatura verticale. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Esempio {#example-5}

Per impostare la spaziatura orizzontale di 24 pixel e la spaziatura verticale di 18 pixel:

```
.s7interactivevideoviewer .s7calltoaction .s7thumbcell { 
 margin-top: 9px; 
 margin-bottom: 9px; 
 margin-left: 12px; 
 margin-right: 12px; 
}
```

<!--<a id="section_D06CF9F709A3447F83DC6E1CE7CA58B5"></a>-->

Il seguente selettore di classe CSS controlla l’aspetto della miniatura nel pannello di invito all’azione:

```
.s7interactivevideoviewer .s7calltoaction .s7thumb
```

## Proprietà CSS della miniatura nel pannello di invito all’azione: {#css-properties-of-the-thumbnail-in-the-call-to-action-panel}

<table id="table_ECD7477F4BE94BA8943210FA8B6B8D01"> 
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
>La miniatura supporta il selettore di attributi `state`, che può essere utilizzato per applicare skin diversi a stati di miniature diversi. In particolare, `state="selected"` corrisponde alla miniatura per l&#39;immagine attualmente selezionata; `state="default"` corrisponde al resto delle miniature; `state="over"` viene utilizzato al passaggio del mouse.

## Esempio {#example-6}

Per impostare miniature di 94 x 100 pixel:

```
.s7interactivevideoviewer .s7calltoaction .s7thumb { 
 width:94px; 
 height:100px; 
}
```

<!--<a id="section_F1B7E3FA3ABD4D71848586A3B308F9E2"></a>-->

Il seguente selettore di classe CSS controlla l’aspetto dell’etichetta di miniatura nel pannello di invito all’azione:

```
.s7interactivevideoviewer .s7calltoaction .s7label
```

## Proprietà CSS dell’etichetta di miniatura nel pannello di invito all’azione: {#css-properties-of-the-thumbnail-label-in-the-call-to-action-panel}

<table id="table_E2C9F21EBD9140FD9D20A4BBAD117E2F"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> colore </span> </p> </td> 
   <td colname="col2"> <p> Colore del testo dell’etichetta. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> allinea testo </span> </p> </td> 
   <td colname="col2"> <p>Allineamento orizzontale dell’etichetta. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> famiglia di caratteri </span> </p> </td> 
   <td colname="col2"> <p>Nome font. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size </span> </p> </td> 
   <td colname="col2"> <p>Famiglia di caratteri. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Esempio {#example-7}

Per impostare le etichette che utilizzano un colore bianco, allineate al centro di 15 pixel e utilizzate un carattere Arial®:

```
.s7interactivevideoviewer .s7calltoaction .s7label { 
 text-align: center; 
 color: #ffffff; 
  font-family: Arial,Helvetica,sans-serif; 
  font-size: 15px; 
}
```

<!--<a id="section_2C011101EB804513B942EFB4CBD38E62"></a>-->

Se sono presenti più miniature di quelle che possono essere visualizzate verticalmente, le miniature eseguono il rendering di una barra di scorrimento verticale a destra. Per impostazione predefinita, il pannello di invito all’azione esegue il rendering di una piccola barra verticale senza pulsanti di scorrimento e miniatura. Tuttavia, è possibile personalizzare la barra modificando il CSS del visualizzatore.

Il seguente selettore di classe CSS controlla l’aspetto dell’area della barra di scorrimento nel pannello di invito all’azione:

```
.s7interactivevideoviewer .s7calltoaction .s7thumbnailgridview .s7scrollbar
```

## Proprietà CSS dell’area della barra di scorrimento nel pannello di invito all’azione: {#css-properties-of-the-scroll-bar-area-in-the-call-to-action-panel}

<table id="table_6D3A4A68BFDB44259A6E2E632B9195F3"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> larghezza </span> </p> </td> 
   <td colname="col2"> <p> Larghezza della barra di scorrimento. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> primi </span> </p> </td> 
   <td colname="col2"> <p>Scostamento della barra di scorrimento verticale dalla parte superiore dell'area delle miniature. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> in basso </span> </p> </td> 
   <td colname="col2"> <p>Scostamento della barra di scorrimento verticale dalla parte inferiore dell'area delle miniature. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> a destra </span> </p> </td> 
   <td colname="col2"> <p> Scostamento della barra di scorrimento orizzontale dal bordo destro dell'area delle miniature. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Esempio {#example-8}

Per impostare una barra di scorrimento larga 22 pixel e priva di margini nella parte superiore, destra o inferiore dell&#39;area delle miniature:

```
.s7interactivevideoviewer .s7calltoaction .s7thumbnailgridview .s7scrollbar { 
 top:0px; 
 bottom:0px; 
 right:0px; 
 width:22px; 
}
```

<!--<a id="section_E27B7253441543278E1081D70BA46122"></a>-->

La traccia della barra di scorrimento è l&#39;area compresa tra i pulsanti della barra di scorrimento superiore e inferiore. Il componente imposta automaticamente la posizione e l&#39;altezza della traccia.

Il seguente selettore di classe CSS controlla l’aspetto della traccia della barra di scorrimento nel pannello di invito all’azione:

```
.s7interactivevideoviewer .s7calltoaction .s7thumbnailgridview .s7scrollbar .s7scrolltrack
```

## Proprietà CSS della barra del brano di scorrimento {#css-properties-of-the-scroll-track-bar}

<table id="table_7A7D40C332F4461FAAC623196C00D5A8"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> larghezza </span> </p> </td> 
   <td colname="col2"> <p>Larghezza della barra del brano di scorrimento. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> colore di sfondo </span> </p> </td> 
   <td colname="col2"> <p>Colore di sfondo della barra dei brani. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Esempio {#example-9}

Per impostare una traccia della barra di scorrimento larga 22 pixel e di colore grigio:

```
.s7interactivevideoviewer .s7calltoaction .s7thumbnailgridview .s7scrollbar .s7scrolltrack { 
 width:22px; 
 background-color:#222222; 
}
```

<!--<a id="section_4A5D8C1A9C9D4E7B8AC0CD5BC6F3772D"></a>-->

Il pollice della barra di scorrimento si sposta verticalmente all&#39;interno dell&#39;area della traccia di scorrimento. La sua posizione verticale è completamente controllata dalla logica del componente; tuttavia, l’altezza del pollice non cambia in modo dinamico a seconda della quantità di contenuto.

Il seguente selettore di classe CSS controlla l’aspetto dell’altezza del pollice e di altro tipo:

```
.s7interactivevideoviewer .s7calltoaction .s7thumbnailgridview .s7scrollbar .s7scrollthumb
```

## Proprietà CSS dell’altezza del pollice nel pannello di invito all’azione: {#css-properties-of-the-thumb-height-in-the-call-to-action-panel}

<table id="table_1F39948FC3924FA4B7F851B65B2D860B"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> larghezza </span> </p> </td> 
   <td colname="col2"> <p>Larghezza del pollice. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> altezza </span> </p> </td> 
   <td colname="col2"> <p>Altezza del pollice. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> riempimento superiore </span> </p> </td> 
   <td colname="col2"> <p>Spaziatura verticale tra la parte superiore del brano. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> riempimento inferiore </span> </p> </td> 
   <td colname="col2"> <p>Spaziatura verticale tra la parte inferiore del brano. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> raggio bordo </span> </p> </td> 
   <td colname="col2"> <p>Raggio del bordo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> colore di sfondo </span> </p> </td> 
   <td colname="col2"> <p>Colore del pollice. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> immagine di sfondo </span> </p> </td> 
   <td colname="col2"> <p> Immagine visualizzata per un determinato stato del pollice. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> Posizionate all'interno dello sprite del disegno, se vengono utilizzati gli sprite CSS. </p> <p>Vedere <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-customizingviewer/c-html5-aem-int-video-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> sprite CSS </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>La miniatura supporta il selettore di attributi `state`, che può essere utilizzato per applicare skin diversi ai seguenti stati miniatura: `"up"`, `"down"`, `"over"` e `"disabled"`.

## Esempio {#example-10}

Per impostare una barra di scorrimento di 6 x 167 pixel con tre angoli arrotondati di pixel e un colore grigio:

```
.s7interactivevideoviewer .s7calltoaction .s7thumbnailgridview .s7scrollbar .s7scrollthumb[state] { 
 width:6px; 
 height:167px; 
 background-color:#666666; 
 background-image:none; 
 border-radius:3px 3px 3px 3px; 
}
```

<!--<a id="section_C393B59763344E70A3BBD0601110F8DD"></a>-->

Il seguente selettore di classe CSS controlla l&#39;aspetto dei pulsanti di scorrimento superiore e inferiore:

```
.s7interactivevideoviewer .s7calltoaction .s7thumbnailgridview .s7scrollbar .s7scrollupbutton 
 
.s7interactivevideoviewer .s7calltoaction .s7thumbnailgridview .s7scrollbar .s7scrolldownbutton
```

Non è possibile posizionare i pulsanti di scorrimento utilizzando le proprietà CSS superiore, sinistra, inferiore o destra; la logica di visualizzazione li posiziona automaticamente. Il pannello di invito all’azione nel visualizzatore video interattivo non utilizza questi pulsanti nella barra di scorrimento, pertanto le loro dimensioni sono impostate su 0 pixel nel CSS predefinito.

## Proprietà CSS dei pulsanti di scorrimento superiore e inferiore nel pannello di invito all’azione:  {#css-properties-of-the-top-and-bottom-scroll-buttons-in-the-call-to-action-panel}

<table id="table_FE17D19E0545424EADB0256524361359"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> larghezza </span> </p> </td> 
   <td colname="col2"> <p> Larghezza del pulsante. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> altezza </span> </p> </td> 
   <td colname="col2"> <p>Altezza pulsante. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> immagine di sfondo </span> </p> </td> 
   <td colname="col2"> <p>Immagine visualizzata per un determinato stato del pulsante. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> Posizionate all'interno dello sprite del disegno, se vengono utilizzati gli sprite CSS. </p> <p>Vedere <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-customizingviewer/c-html5-aem-int-video-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> sprite CSS </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Questi pulsanti supportano il selettore di attributi `state`, che può essere utilizzato per applicare interfacce diverse ai seguenti stati miniatura diversi: `"up"`, `"down"`, `"over"` e `"disabled"`.

Le descrizioni dei pulsanti possono essere localizzate. Vedi [Localizzazione degli elementi dell&#39;interfaccia utente](../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74).

## Esempio {#example-11}

Disattivare i pulsanti di scorrimento impostandone le dimensioni su 0 e nasconderli:

```
.s7interactivevideoviewer .s7calltoaction .s7thumbnailgridview .s7scrollbar .s7scrollupbutton { 
 visibility: hidden; 
 width: 0px; 
 height: 0px; 
} 
.s7interactivevideoviewer .s7calltoaction .s7thumbnailgridview .s7scrollbar .s7scrolldownbutton { 
 visibility: hidden; 
 width: 0px; 
 height: 0px; 
}
```
