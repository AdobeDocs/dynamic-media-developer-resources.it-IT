---
title: Video scrubber
description: Lo scorrimento video è il controllo cursore orizzontale che consente a un utente di cercare dinamicamente qualsiasi posizione temporale all'interno del video attualmente in riproduzione.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: 9d11f2e9-315c-44d8-beb1-530d2b316604
source-git-commit: 14ca8cd5e1ce60d59806765e573e50417d0ccc50
workflow-type: tm+mt
source-wordcount: '1034'
ht-degree: 0%

---

# Video scrubber{#video-scrubber}

Lo scorrimento video è il controllo cursore orizzontale che consente a un utente di cercare dinamicamente qualsiasi posizione temporale all&#39;interno del video attualmente in riproduzione.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

Anche la &quot;manopola&quot; dello scorrimento si muove durante la riproduzione del video per indicare la posizione temporale corrente del video durante la riproduzione. Lo scorrimento video occupa sempre l&#39;intera larghezza della barra di controllo. È possibile applicare lo skin al video scrubber e modificarne l’altezza e la posizione verticale, mediante CSS.

L’aspetto generale dello scorrimento dei video è controllato dal seguente selettore di classe CSS:

```
.s7interactivevideoviewer .s7videoscrubber 
.s7interactivevideoviewer .s7videoscrubber .s7videotime 
.s7interactivevideoviewer .s7videoscrubber .s7knob
```

**Proprietà CSS dello scorrimento video**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> primi </span> </p> </td> 
   <td colname="col2"> <p>Posizione dal bordo superiore, inclusa la spaziatura. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Fondoschiena </span> </p> </td> 
   <td colname="col2"> <p> Posizione dal basso bordo, compresa l'imbottitura. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> altezza </span> </p> </td> 
   <td colname="col2"> <p>Altezza dello scrubber video. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> colore di sfondo </span> </p> </td> 
   <td colname="col2"> <p>Colore dello scrubber video. </p> </td> 
  </tr> 
 </tbody> 
</table>

I seguenti selettori di classi CSS tengono traccia degli indicatori di background, riproduzione e caricamento:

```
.s7interactivevideoviewer .s7videoscrubber .s7track 
.s7interactivevideoviewer .s7videoscrubber .s7trackloaded 
.s7interactivevideoviewer .s7videoscrubber .s7trackplayed
```

**Proprietà CSS della traccia**

<table id="table_46903DCACF314426B67783167ADF7715"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> altezza </span> </p> </td> 
   <td colname="col2"> <p>Altezza della traccia corrispondente. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> colore di sfondo </span> </p> </td> 
   <td colname="col2"> <p>Colore del brano corrispondente. </p> </td> 
  </tr> 
 </tbody> 
</table>

Il seguente selettore di classe CSS controlla la manopola:

```
.s7interactivevideoviewer .s7videoscrubber .s7knob
```

**Proprietà CSS della manopola**

<table id="table_966826FB81114362A8D81D1EED38D512"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> primi </span> </p> </td> 
   <td colname="col2"> <p>Offset manopola verticale. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> larghezza </span> </p> </td> 
   <td colname="col2"> <p>Larghezza manopola. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> altezza </span> </p> </td> 
   <td colname="col2"> <p>Altezza manopola. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> immagine di sfondo </span> </p> </td> 
   <td colname="col2"> <p>Grafica a manopola. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> posizione sfondo </span> </p> </td> 
   <td colname="col2"> <p> Posizione all'interno dello sprite dell'illustrazione, se vengono utilizzati sprite CSS. </p> <p>Vedere <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-customizingviewer/c-html5-aem-int-video-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> CSS Sprite </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

La seguente classe CSS selettore controlla l&#39;indicatore del tempo riprodotto:

```
.s7interactivevideoviewer .s7videoscrubber .s7videotime
```

**Proprietà CSS della bolla di tempo riprodotta**

<table id="table_21E9AD3FBC8C4437BA02E5CD1BF7E831"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> famiglia di caratteri </span> </p> </td> 
   <td colname="col2"> <p> Famiglia di font da utilizzare per il testo visualizzato nel tempo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Dimensioni font </span> </p> </td> 
   <td colname="col2"> <p> Dimensioni font da utilizzare per il testo visualizzato per l'ora. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Colore </span> </p> </td> 
   <td colname="col2"> <p> Colore font da utilizzare per il testo visualizzato per l'ora. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> larghezza </span> </p> </td> 
   <td colname="col2"> <p>Larghezza dell'area della bolla. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> altezza </span> </p> </td> 
   <td colname="col2"> <p>Altezza dell'area della bolla. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> imbottitura </span> </p> </td> 
   <td colname="col2"> <p>Imbottitura dell'area delle bolle. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> immagine di sfondo </span> </p> </td> 
   <td colname="col2"> <p>Grafica a bolle. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> posizione sfondo </span> </p> </td> 
   <td colname="col2"> <p> Posizione all'interno dello sprite dell'illustrazione, se vengono utilizzati sprite CSS. </p> <p>Vedere <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-customizingviewer/c-html5-aem-int-video-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> CSS Sprite </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> allinea testo </span> </p> </td> 
   <td colname="col2"> <p>Allineamento del testo con l'area a bolle. </p> </td> 
  </tr> 
 </tbody> 
</table>

La descrizione comando dello scorrimento video può essere localizzata. Per ulteriori informazioni, vedere [Localizzazione degli elementi dell&#39;interfaccia utente](../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74).

**Esempio** - Per impostare un visualizzatore video con uno scorrimento video e con colori di traccia personalizzati alti dieci pixel. Posizionalo a dieci pixel e 35 pixel dai bordi superiore e sinistro della barra di controllo.

```
.s7interactivevideoviewer .s7videoscrubber  { 
top:10px; 
left:35px; 
height:10px; 
background-color:#AAAAAA; 
} 
.s7interactivevideoviewer .s7videoscrubber .s7track { 
height:10px; 
background-color:#444444; 
} 
.s7interactivevideoviewer .s7videoscrubber .s7trackloaded { 
height:10px; 
background-color:#666666; 
} 
.s7interactivevideoviewer .s7videoscrubber .s7trackplayed { 
height:10px; 
background-color:#888888; 
}
```

Quando il marcatore capitolo video è attivato con il `navigation` parametro, le posizioni dei capitoli vengono visualizzate come marcatori nella parte superiore della traccia di scorrimento video.

Il marcatore del capitolo video è controllato dal seguente selettore di classe CSS:

```
.s7interactivevideoviewer .s7videoscrubber .s7navigation
```

**Proprietà CSS del marcatore capitolo video**

<table id="table_51F16E47BEF3430B919ABEEDBE543973"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Larghezza </span> </p> </td> 
   <td colname="col2"> <p>Video larghezza dell'indicatore capitolo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> altezza </span> </p> </td> 
   <td colname="col2"> <p>Altezza marcatore capitolo video. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> immagine di sfondo </span> </p> </td> 
   <td colname="col2"> <p>Illustrazione del marcatore del capitolo video. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> Posizionate all'interno dello sprite del disegno, se vengono utilizzati gli sprite CSS. </p> <p>Vedere <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-customizingviewer/c-html5-aem-int-video-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> sprite CSS </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Questo supporta pulsante il `state` selettore attributo, che potete utilizzare per applicare interfacce diverse a diversi stati pulsante. In particolare, `selected='default'` corrisponde allo stato predefinito del marcatore capitolo video e `selected='over'` viene utilizzato quando il marcatore capitolo video viene attivato con un gesto di passaggio del mouse o di tocco.

**Esempio** : per impostare un marcatore capitolo video di 5 x 8 pixel e con grafica diversa per lo stato &quot;Predefinito&quot; e &quot;Sopra&quot;.

```
.s7interactivevideoviewer .s7videoscrubber .s7navigation { 
width:5px; 
height:8px; 
} 
.s7interactivevideoviewer .s7videoscrubber .s7navigation[state="default"] { 
background-image: url("images/v2/VideoScrubberDiamond.png"); 
} 
.s7interactivevideoviewer .s7videoscrubber .s7navigation[state="over"] { 
background-image: url("images/v2/VideoScrubberDiamond_over.png"); 
}
```

Video fumetto del capitolo è posizionato sopra l&#39;indicatore del capitolo video e mostra il titolo, l&#39;ora di inizio e la descrizione di un determinato capitolo. È possibile controllare la larghezza massima della bolla e l&#39;offset verticale rispetto alla traccia di scorrimento video. Il resto viene calcolato automaticamente dal componente.

Il fumetto del capitolo video è controllato dalla seguente classe CSS selettore:

```
.s7interactivevideoviewer .s7videoscrubber .s7chapter
```

**Proprietà CSS del fumetto del capitolo video**

<table id="table_7F33738422F84978B9132495F67C2156"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Larghezza massima </span> </p> </td> 
   <td colname="col2"> <p>Larghezza massima del fumetto del capitolo video. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Fondoschiena </span> </p> </td> 
   <td colname="col2"> <p>Offset verticale dalla traccia di scorrimento video. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Esempio** - Per impostare una bolla di capitoli video larga 235 pixel e alta otto pixel dalla parte inferiore della traccia di scorrimento video.

```
.s7interactivevideoviewer .s7videoscrubber .s7chapter { 
max-width:235px; 
bottom:8px; 
}
```

La bolla dei capitoli video è composta da un’intestazione e da un contenuto opzionali. L’intestazione presenta l’ora di inizio del capitolo e il titolo del capitolo opzionali.

L’intestazione è controllata dal seguente selettore di classe CSS:

```
.s7interactivevideoviewer .s7videoscrubber .s7chapter .s7header
```

**Proprietà CSS dell&#39;intestazione del fumetto del capitolo video**

<table id="table_56FBC3BADDEA4E15924DD750CADC474F"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> altezza </span> </p> </td> 
   <td colname="col2"> <p>Altezza intestazione bolla capitolo video. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> riempimento </span> </p> </td> 
   <td colname="col2"> <p>Spaziatura interna per il testo dell’intestazione della bolla del capitolo video. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> colore di sfondo </span> </p> </td> 
   <td colname="col2"> <p>Colore di sfondo intestazione bolla capitolo video. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> altezza riga </span> </p> </td> 
   <td colname="col2"> <p>Video altezza riga del testo dell'intestazione del fumetto del capitolo. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Esempio** : per impostare un&#39;intestazione a fumetto del capitolo video alta 22 pixel, un&#39;altezza della linea di 22 pixel, un margine orizzontale di 12 pixel e uno sfondo grigio.

```
.s7interactivevideoviewer .s7videoscrubber .s7chapter .s7header { 
height:22px; 
padding:0 12px; 
line-height:22px; 
background-color: rgba(51, 51, 51, 0.8); 
}
```

L&#39;ora di inizio del capitolo video è controllata dalla seguente classe CSS selettore:

```
.s7interactivevideoviewer .s7videoscrubber .s7chapter .s7header .s7starttime
```

**Proprietà CSS dell&#39;ora di inizio del capitolo video**

<table id="table_D58D6B22BAEE4E26BAAB34783AE5A044"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> colore </span> </p> </td> 
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
   <td colname="col1"> <p> <span class="codeph"> famiglia di caratteri </span> </p> </td> 
   <td colname="col2"> <p>Famiglia di caratteri. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> riempimento a destra </span> </p> </td> 
   <td colname="col2"> <p> Spaziatura tra l'ora di inizio e il titolo del capitolo. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Esempio** - Per impostare l&#39;ora di inizio del capitolo utilizzando il tipo di carattere Verdana a dieci pixel di colore grigio e con dieci pixel di spaziatura interna a destra.

```
.s7interactivevideoviewer .s7videoscrubber .s7chapter .s7header .s7starttime { 
color: #dddddd; 
font-family: Verdana,Arial,Helvetica,sans-serif; 
font-size: 10px; 
padding-right: 10px; 
}
```

Il titolo del capitolo video è controllato dal seguente selettore di classe CSS:

```
.s7interactivevideoviewer .s7videoscrubber .s7chapter .s7header .s7title
```

**Proprietà CSS del titolo del capitolo video**

<table id="table_240DD3E119584DCC95FF480B60266603"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Colore </span> </p> </td> 
   <td colname="col2"> <p>Video colore del testo del titolo del capitolo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Peso font </span> </p> </td> 
   <td colname="col2"> <p>Video titolo del capitolo font peso. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size </span> </p> </td> 
   <td colname="col2"> <p>Dimensione font titolo capitolo video. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> famiglia di caratteri </span> </p> </td> 
   <td colname="col2"> <p>Famiglia di font per il titolo del capitolo video. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Esempio** - Per impostare un titolo di capitolo video che utilizza un font Verdana bianco, grassetto e a dieci pixel.

```
.s7interactivevideoviewer .s7videoscrubber .s7chapter .s7header .s7title { 
color: #ffffff; 
font-family: Verdana,Arial,Helvetica,sans-serif; 
font-size: 10px; 
font-weight: bold; 
}
```

La descrizione del capitolo video è controllata dalla seguente classe CSS selettore:

```
.s7interactivevideoviewer .s7videoscrubber .s7chapter .s7description
```

**Proprietà CSS della descrizione del capitolo video**

<table id="table_780382ECB3D049118857DCA21D130326"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Colore </span> </p> </td> 
   <td colname="col2"> <p>Video colore del testo della descrizione del capitolo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> colore di sfondo </span> </p> </td> 
   <td colname="col2"> <p>Video colore di sfondo della descrizione del capitolo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Peso font </span> </p> </td> 
   <td colname="col2"> <p>Spessore font descrizione capitolo video. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size </span> </p> </td> 
   <td colname="col2"> <p>Dimensione font descrizione capitolo video. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> famiglia di caratteri </span> </p> </td> 
   <td colname="col2"> <p>Famiglia di font per la descrizione del capitolo video. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> altezza linea </span> </p> </td> 
   <td colname="col2"> <p>Video altezza riga descrizione capitolo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> imbottitura </span> </p> </td> 
   <td colname="col2"> <p>Video descrizione del capitolo imbottitura interna. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Esempio** : per impostare la descrizione del capitolo video usando un font Verdana grigio scuro da 11 pixel, con sfondo grigio chiaro. Altezza linea di cinque pixel, spaziatura orizzontale di 12 pixel, spaziatura superiore di 12 pixel e spaziatura inferiore di nove pixel.

```
.s7interactivevideoviewer .s7videoscrubber .s7chapter .s7description { 
color: #333333; 
background-color: rgba(221, 221, 221, 0.9); 
font-family: Verdana,Arial,Helvetica,sans-serif; 
font-size: 11px; 
line-height: 15px; 
padding: 12px 12px 9px; 
}
```

Il connettore wedge nella parte inferiore del fumetto del capitolo è controllato dalla seguente classe CSS selettore:

```
.s7interactivevideoviewer .s7videoscrubber .s7chapter .s7tail
```

**Proprietà CSS del connettore wedge**

<table id="table_BC6AFB57D9404A84A3AE657448C0EB06"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> bordo colore </span> </p> </td> 
   <td colname="col2"> <p>Colore connettore cuneo. </p> <p>Definito trasparente <span class="codeph"> &lt;color&gt; </span> in modo che venga definito solo il colore superiore bordo e i bordi rimanenti rimangano trasparenti.&lt;/color&gt; </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Larghezza bordo </span> </p> </td> 
   <td colname="col2"> <p> Larghezza connettore cuneo. </p> <p>Definito come <span class="codeph"> &lt;larghezza&gt; &lt;larghezza&gt; 0 </span> in modo che la stessa larghezza sia definita solo per i bordi superiore e orizzontale e la larghezza del bordo inferiore sia <span class="codeph"> 0 </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margine </span> </p> </td> 
   <td colname="col2"> <p> Definisce solo un margine inferiore negativo. Deve avere lo stesso valore di <span class="codeph"> border-width </span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Esempio** - Per impostare un connettore cuneo grigio da sei pixel:

```
.s7interactivevideoviewer .s7videoscrubber .s7chapter .s7tail { 
border-color: rgba(221, 221, 221, 0.9) transparent transparent; 
border-width: 6px 6px 0; 
margin: 0 0 0 -6px; 
}
```
