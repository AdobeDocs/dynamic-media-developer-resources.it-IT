---
title: Scorrimento video
description: Lo scorrimento video è il dispositivo di scorrimento orizzontale che consente all'utente di cercare dinamicamente una posizione temporale all'interno del video in fase di riproduzione
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Video
role: Developer,User
exl-id: 404e39d4-565e-4dde-b2bd-fa83a895d001
source-git-commit: ceb9483f67a19d969ecbbd01cede11f3dae86467
workflow-type: tm+mt
source-wordcount: '1025'
ht-degree: 1%

---

# Scorrimento video{#video-scrubber}

Lo scorrimento video è il dispositivo di scorrimento orizzontale che consente all’utente di cercare dinamicamente una posizione temporale all’interno del video attualmente in riproduzione.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

La &quot;manopola&quot; di scorrimento si sposta anche durante la riproduzione del video per indicare la posizione temporale corrente del video durante la riproduzione. Lo scorrimento video occupa sempre l&#39;intera larghezza della barra di controllo. È possibile applicare lo skin al video scrubber e modificarne l’altezza e la posizione verticale, mediante CSS.

L’aspetto generale dello scorrimento dei video è controllato dal seguente selettore di classe CSS:

```
.s7videoviewer .s7videoscrubber 
.s7videoviewer .s7videoscrubber .s7videotime 
.s7videoviewer .s7videoscrubber .s7knob
```

**Proprietà CSS dello scorrimento video**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> top </span> </p> </td> 
   <td colname="col2"> <p>Posizione dal bordo superiore, inclusa la spaziatura. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> bottom </span> </p> </td> 
   <td colname="col2"> <p> Posizione dal bordo inferiore, inclusa la spaziatura. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Altezza dello scorrimento video. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p>Colore dello scorrimento video. </p> </td> 
  </tr> 
 </tbody> 
</table>

I seguenti selettori di classi CSS tengono traccia degli indicatori di sfondo, riproduzione e caricamento:

```
.s7videoviewer .s7videoscrubber .s7track 
.s7videoviewer .s7videoscrubber .s7trackloaded 
.s7videoviewer .s7videoscrubber .s7trackplayed
```

**Proprietà CSS del brano**

<table id="table_46903DCACF314426B67783167ADF7715"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Altezza del brano corrispondente. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p>Colore del brano corrispondente. </p> </td> 
  </tr> 
 </tbody> 
</table>

Il seguente selettore di classe CSS controlla la manopola:

```
.s7videoviewer .s7videoscrubber .s7knob
```

**Proprietà CSS della manopola**

<table id="table_966826FB81114362A8D81D1EED38D512"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> top </span> </p> </td> 
   <td colname="col2"> <p>Offset manopola verticale. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Larghezza manopola. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Altezza manopola. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image </span> </p> </td> 
   <td colname="col2"> <p>Grafica a manopola. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> Posizionate all'interno dello sprite del disegno, se vengono utilizzati gli sprite CSS. </p> <p>Consulta <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-customizingviewer/c-html5-video-viewer-20-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> Spunti CSS </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

Il seguente selettore di classe CSS controlla la bolla del tempo riprodotto:

```
.s7videoviewer .s7videoscrubber .s7videotime
```

**Proprietà CSS dell’indicatore di riproduzione**

<table id="table_21E9AD3FBC8C4437BA02E5CD1BF7E831"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family </span> </p> </td> 
   <td colname="col2"> <p> Famiglia di font da utilizzare per il testo visualizzato nel tempo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size </span> </p> </td> 
   <td colname="col2"> <p> Dimensione font da utilizzare per il testo visualizzato nel tempo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color </span> </p> </td> 
   <td colname="col2"> <p> Colore del carattere da utilizzare per il testo visualizzato nel tempo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Larghezza area bolle. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Altezza area bolle. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> riempimento </span> </p> </td> 
   <td colname="col2"> <p>Spaziatura interna area bolle. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image </span> </p> </td> 
   <td colname="col2"> <p>Illustrazione di bolle. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> Posizionate all'interno dello sprite del disegno, se vengono utilizzati gli sprite CSS. </p> <p>Consulta <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-customizingviewer/c-html5-video-viewer-20-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> Spunti CSS </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> text-align </span> </p> </td> 
   <td colname="col2"> <p>Allineamento del testo con l'area a bolle. </p> </td> 
  </tr> 
 </tbody> 
</table>

La descrizione comando dello scorrimento video può essere localizzata. Consulta [Localizzazione degli elementi dell’interfaccia utente](../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/r-html5-video-viewer-20-localization.md#concept-1d5ca2d8480f4064a51eddba13940aad) per ulteriori informazioni.

**Esempio** : per impostare un visualizzatore video con uno scorrimento video con colori di brano personalizzati. Lo scorrimento deve essere alto dieci pixel e posizionato a dieci pixel e a 35 pixel dai bordi superiore e sinistro della barra di controllo.

```
.s7videoviewer .s7videoscrubber  { 
top:10px; 
left:35px; 
height:10px; 
background-color:#AAAAAA; 
} 
.s7videoviewer .s7videoscrubber .s7track { 
height:10px; 
background-color:#444444; 
} 
.s7videoviewer .s7videoscrubber .s7trackloaded { 
height:10px; 
background-color:#666666; 
} 
.s7videoviewer .s7videoscrubber .s7trackplayed { 
height:10px; 
background-color:#888888; 
}
```

Quando il capitolo video è abilitato con il `navigation` Le posizioni dei capitoli vengono visualizzate come marcatori sopra la traccia di scorrimento video.

Il marcatore del capitolo video è controllato dal seguente selettore di classe CSS:

```
 .s7videoviewer .s7videoscrubber .s7navigation
```

**Proprietà CSS del marcatore capitolo video**

<table id="table_51F16E47BEF3430B919ABEEDBE543973"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Larghezza marcatore capitolo video. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Altezza marcatore capitolo video. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image </span> </p> </td> 
   <td colname="col2"> <p>Illustrazione del marcatore del capitolo video. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> Posizionate all'interno dello sprite del disegno, se vengono utilizzati gli sprite CSS. </p> <p>Consulta <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-customizingviewer/c-html5-video-viewer-20-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> Spunti CSS </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Questo pulsante supporta sia `state` selettore di attributi, che può essere utilizzato per applicare interfacce diverse a stati di pulsante diversi. In particolare: `selected='default'` corrisponde allo stato predefinito del marcatore del capitolo video e `selected='over'` viene utilizzato quando il marcatore del capitolo video viene attivato con il mouse o con un movimento tattile.

**Esempio** : per impostare un marcatore capitolo video di 5 x 8 pixel che utilizza immagini diverse per lo stato &quot;default&quot; e &quot;over&quot;.

```
.s7videoviewer .s7videoscrubber .s7navigation { 
width:5px; 
height:8px; 
} 
.s7videoviewer .s7videoscrubber .s7navigation[state="default"] { 
background-image: url("images/v2/VideoScrubberDiamond.png"); 
} 
.s7videoviewer .s7videoscrubber .s7navigation[state="over"] { 
background-image: url("images/v2/VideoScrubberDiamond_over.png"); 
}
```

La bolla dei capitoli video è posizionata sopra il marcatore dei capitoli video e mostra il titolo, l’ora di inizio e la descrizione di un determinato capitolo. È possibile controllare la larghezza massima della bolla e l&#39;offset verticale rispetto alla traccia di scorrimento video. Il resto viene calcolato automaticamente dal componente.

La bolla dei capitoli video è controllata dal seguente selettore di classe CSS:

```
.s7videoviewer .s7videoscrubber .s7chapter
```

**Proprietà CSS del fumetto del capitolo video**

<table id="table_7F33738422F84978B9132495F67C2156"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> max-width </span> </p> </td> 
   <td colname="col2"> <p>Larghezza massima della bolla del capitolo video. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> bottom </span> </p> </td> 
   <td colname="col2"> <p>Offset verticale dalla traccia di scorrimento video. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Esempio** - Per impostare una bolla di capitolo video larga 235 pixel e alta 8 pixel dalla parte inferiore della traccia di scorrimento video.

```
.s7videoviewer .s7videoscrubber .s7chapter { 
max-width:235px; 
bottom:8px; 
}
```

La bolla dei capitoli video è composta da un’intestazione e da un contenuto opzionali. L’intestazione presenta l’ora di inizio del capitolo e il titolo del capitolo opzionali.

L’intestazione è controllata dal seguente selettore di classe CSS:

```
.s7videoviewer .s7videoscrubber .s7chapter .s7header
```

**Proprietà CSS dell’intestazione a bolla del capitolo video**

<table id="table_56FBC3BADDEA4E15924DD750CADC474F"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Altezza intestazione bolla capitolo video. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> riempimento </span> </p> </td> 
   <td colname="col2"> <p>Spaziatura interna per il testo dell’intestazione della bolla del capitolo video. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p>Colore di sfondo intestazione bolla capitolo video. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> line-height </span> </p> </td> 
   <td colname="col2"> <p>Altezza riga testo intestazione capitolo video. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Esempio** : per impostare un&#39;intestazione a bolla di capitolo video alta 22 pixel, un&#39;altezza della linea di 22 pixel, un margine orizzontale di 12 pixel e uno sfondo grigio.

```
.s7videoviewer .s7videoscrubber .s7chapter .s7header { 
height:22px; 
padding:0 12px; 
line-height:22px; 
background-color: rgba(51, 51, 51, 0.8); 
}
```

L’ora di inizio del capitolo video è controllata dal seguente selettore di classe CSS:

```
 .s7videoviewer .s7videoscrubber .s7chapter .s7header .s7starttime
```

**Proprietà CSS dell’ora di inizio del capitolo video**

<table id="table_D58D6B22BAEE4E26BAAB34783AE5A044"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color </span> </p> </td> 
   <td colname="col2"> <p>Colore testo. </p> </td> 
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
   <td colname="col1"> <p> <span class="codeph"> padding-right </span> </p> </td> 
   <td colname="col2"> <p> Spaziatura tra l'ora di inizio e il titolo del capitolo. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Esempio** - Per impostare l&#39;ora di inizio del capitolo utilizzando il carattere Verdana grigio da dieci pixel e con dieci pixel di spaziatura verso destra.

```
.s7videoviewer .s7videoscrubber .s7chapter .s7header .s7starttime { 
color: #dddddd; 
font-family: Verdana,Arial,Helvetica,sans-serif; 
font-size: 10px; 
padding-right: 10px; 
}
```

Il titolo del capitolo video è controllato dal seguente selettore di classe CSS:

```
.s7videoviewer .s7videoscrubber .s7chapter .s7header .s7title
```

**Proprietà CSS del titolo del capitolo video**

<table id="table_240DD3E119584DCC95FF480B60266603"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color </span> </p> </td> 
   <td colname="col2"> <p>Colore testo titolo capitolo video. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-weight </span> </p> </td> 
   <td colname="col2"> <p>Spessore font titolo capitolo video. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size </span> </p> </td> 
   <td colname="col2"> <p>Dimensione font titolo capitolo video. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family </span> </p> </td> 
   <td colname="col2"> <p>Famiglia di font per il titolo del capitolo video. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Esempio** : per impostare un titolo del capitolo video che utilizza un font Verdana bianco, grassetto e a dieci pixel.

```
.s7videoviewer .s7videoscrubber .s7chapter .s7header .s7title { 
color: #ffffff; 
font-family: Verdana,Arial,Helvetica,sans-serif; 
font-size: 10px; 
font-weight: bold; 
}
```

La descrizione del capitolo video è controllata dal seguente selettore di classe CSS:

```
 .s7videoviewer .s7videoscrubber .s7chapter .s7description
```

**Proprietà CSS della descrizione del capitolo video**

<table id="table_780382ECB3D049118857DCA21D130326"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color </span> </p> </td> 
   <td colname="col2"> <p>Colore testo descrizione capitolo video. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p>Colore di sfondo della descrizione del capitolo video. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-weight </span> </p> </td> 
   <td colname="col2"> <p>Spessore font descrizione capitolo video. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size </span> </p> </td> 
   <td colname="col2"> <p>Dimensione font descrizione capitolo video. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family </span> </p> </td> 
   <td colname="col2"> <p>Famiglia di font per la descrizione del capitolo video. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> line-height </span> </p> </td> 
   <td colname="col2"> <p>Altezza riga descrizione capitolo video. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> riempimento </span> </p> </td> 
   <td colname="col2"> <p>Spaziatura interna descrizione capitolo video. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Esempio** : per impostare la descrizione del capitolo video utilizzando un carattere Verdana grigio scuro da 11 pixel con uno sfondo grigio chiaro. Infine, utilizza l&#39;altezza di cinque pixel della linea, la spaziatura orizzontale di 12 pixel, la spaziatura superiore di 12 pixel e la spaziatura inferiore di nove pixel.

```
.s7videoviewer .s7videoscrubber .s7chapter .s7description { 
color: #333333; 
background-color: rgba(221, 221, 221, 0.9); 
font-family: Verdana,Arial,Helvetica,sans-serif; 
font-size: 11px; 
line-height: 15px; 
padding: 12px 12px 9px; 
}
```

Il connettore a cuneo all’interno della parte inferiore della bolla del capitolo è controllato dal seguente selettore di classe CSS:

```
 .s7videoviewer .s7videoscrubber .s7chapter .s7tail
```

**Proprietà CSS del connettore cuneo**

<table id="table_BC6AFB57D9404A84A3AE657448C0EB06"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> border-color </span> </p> </td> 
   <td colname="col2"> <p>Colore connettore cuneo. </p> <p>Definito come <span class="codeph"> &lt;color&gt; trasparente </span> in modo che venga definito solo il colore del bordo superiore e che i bordi rimanenti vengano lasciati trasparenti. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> border-width </span> </p> </td> 
   <td colname="col2"> <p> Larghezza connettore cuneo. </p> <p>Definito come <span class="codeph"> &lt;width&gt; &lt;width&gt; 0 </span> in modo che venga definita la stessa larghezza solo per i bordi superiore e orizzontale e che la larghezza del bordo inferiore sia <span class="codeph"> 0 </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margine </span> </p> </td> 
   <td colname="col2"> <p> Definisce solo un margine inferiore negativo. Deve avere lo stesso valore di <span class="codeph"> border-width </span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Esempio** - Per impostare un connettore cuneo grigio a sei pixel:

```
.s7videoviewer .s7videoscrubber .s7chapter .s7tail { 
border-color: rgba(221, 221, 221, 0.9) transparent transparent; 
border-width: 6px 6px 0; 
margin: 0 0 0 -6px; 
}
```
