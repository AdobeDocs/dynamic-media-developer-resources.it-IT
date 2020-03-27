---
description: La barra di scorrimento video è il cursore orizzontale che consente all’utente di cercare in modo dinamico una posizione temporale all’interno del video attualmente in riproduzione.
seo-description: La barra di scorrimento video è il cursore orizzontale che consente all’utente di cercare in modo dinamico una posizione temporale all’interno del video attualmente in riproduzione.
seo-title: Scorrimento video
solution: Experience Manager
title: Scorrimento video
topic: Dynamic media
uuid: 5e4abc8a-ee61-4528-a5de-66148aac3389
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef

---


# Video scrubber{#video-scrubber}

La barra di scorrimento video è il cursore orizzontale che consente all’utente di cercare in modo dinamico una posizione temporale all’interno del video attualmente in riproduzione.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

La &#39;manopola&#39; di scorrimento si sposta anche durante la riproduzione del video per indicare la posizione temporale corrente del video durante la riproduzione. La barra di scorrimento video occupa sempre l’intera larghezza della barra di controllo. È possibile applicare lo scorrimento del video. modificate l’altezza e la posizione verticale del file mediante CSS.

L&#39;aspetto generale dello scorrimento video è controllato dal seguente selettore di classe CSS:

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

I seguenti selettori di classe CSS tracciano gli indicatori di sfondo, riproduzione e caricamento:

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
   <td colname="col2"> <p>Altezza della traccia corrispondente. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p>Colore della traccia corrispondente. </p> </td> 
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
   <td colname="col2"> <p>Offset a manopola verticale. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Larghezza della manopola. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Altezza della manopola. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image </span> </p> </td> 
   <td colname="col2"> <p>Manopola la grafica. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> Posizionare all'interno dello sprite della grafica, se vengono utilizzati gli spriti CSS. </p> <p>Consultate <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-customizingviewer/c-html5-video-viewer-20-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> Sprite CSS </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

Il seguente selettore di classe CSS controlla la bolla temporale riprodotta:

```
.s7videoviewer .s7videoscrubber .s7videotime
```

**Proprietà CSS della bolla temporale riprodotta**

<table id="table_21E9AD3FBC8C4437BA02E5CD1BF7E831"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family </span> </p> </td> 
   <td colname="col2"> <p> Famiglia di font da utilizzare per il testo di visualizzazione dell'ora. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size </span> </p> </td> 
   <td colname="col2"> <p> La dimensione del font da utilizzare per il testo di visualizzazione dell'ora. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color </span> </p> </td> 
   <td colname="col2"> <p> Il colore del font da utilizzare per il testo di visualizzazione dell'ora. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Larghezza area bolla. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Altezza dell'area della bolla. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> spaziatura </span> </p> </td> 
   <td colname="col2"> <p>Spaziatura area bolla. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image </span> </p> </td> 
   <td colname="col2"> <p>Grafica a bolle. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> Posizionare all'interno dello sprite della grafica, se vengono utilizzati gli spriti CSS. </p> <p>Consultate <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-customizingviewer/c-html5-video-viewer-20-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> Sprite CSS </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> text-align </span> </p> </td> 
   <td colname="col2"> <p>Allineamento del testo all'area della bolla. </p> </td> 
  </tr> 
 </tbody> 
</table>

È possibile localizzare la descrizione comandi per lo scorrimento video. Per ulteriori informazioni, consultate [Localizzazione degli elementi](../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/r-html5-video-viewer-20-localization.md#concept-1d5ca2d8480f4064a51eddba13940aad) dell&#39;interfaccia utente.

**Esempio** : per impostare un visualizzatore video con uno scorrimento video con colori di traccia personalizzati alti 10 pixel e posizionati 10 pixel e 35 pixel dai bordi superiore e sinistro della barra di controllo.

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

Quando è attivato il filtro per video con il `navigation` parametro, le posizioni dei capitoli vengono visualizzate come marcatori sulla traccia di scorrimento video.

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
   <td colname="col2"> <p>Grafica marcatore capitolo video. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> Posizionare all'interno dello sprite della grafica, se vengono utilizzati gli spriti CSS. </p> <p>Consultate <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-customizingviewer/c-html5-video-viewer-20-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> Sprite CSS </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Questo pulsante supporta entrambi i selettori di `state` attributi, che è possibile utilizzare per applicare interfacce diverse a diversi stati del pulsante. In particolare, `selected='default'` corrisponde allo stato predefinito del marcatore del capitolo video e `selected='over'` viene utilizzato quando il marcatore del capitolo video viene attivato da un mouse o da un tocco.

**Esempio** : per impostare un marcatore di capitolo video di 5 x 8 pixel e utilizzare un&#39;immagine diversa per lo stato &quot;predefinito&quot; e &quot;sopra&quot;.

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

La bolla dei capitoli video è posizionata sopra l’indicatore del capitolo video e mostra il titolo, l’ora di inizio e la descrizione di un determinato capitolo. È possibile controllare la larghezza massima della bolla e l&#39;offset verticale rispetto alla traccia di scorrimento video. Il resto viene calcolato automaticamente dal componente.

La bolla dei capitoli video è controllata dal seguente selettore di classe CSS:

```
.s7videoviewer .s7videoscrubber .s7chapter
```

**Proprietà CSS della bolla dei capitoli video**

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

**Esempio** - Per impostare una bolla video con capitoli di larghezza pari a 235 pixel e altezza pari a 8 pixel dal basso della traccia di scorrimento video.

```
.s7videoviewer .s7videoscrubber .s7chapter { 
max-width:235px; 
bottom:8px; 
}
```

La bolla dei capitoli video è costituita da un&#39;intestazione e da un contenuto facoltativi. L’intestazione contiene l’ora di inizio e il titolo del capitolo facoltativi.

L&#39;intestazione è controllata dal seguente selettore di classe CSS:

```
.s7videoviewer .s7videoscrubber .s7chapter .s7header
```

**Proprietà CSS dell’intestazione della bolla dei capitoli video**

<table id="table_56FBC3BADDEA4E15924DD750CADC474F"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Altezza dell’intestazione della bolla del capitolo video. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> spaziatura </span> </p> </td> 
   <td colname="col2"> <p>Spaziatura interna per il testo dell’intestazione della bolla dei capitoli video. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p>Colore di sfondo dell’intestazione della bolla video. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> line-height </span> </p> </td> 
   <td colname="col2"> <p>Altezza della riga di testo della bolla del capitolo video. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Esempio** - Per impostare un&#39;intestazione di capitolo video con un&#39;altezza di 22 pixel, un&#39;altezza di riga di 22 pixel, un margine orizzontale di 12 pixel e uno sfondo grigio.

```
.s7videoviewer .s7videoscrubber .s7chapter .s7header { 
height:22px; 
padding:0 12px; 
line-height:22px; 
background-color: rgba(51, 51, 51, 0.8); 
}
```

L&#39;ora di inizio del capitolo video è controllata dal seguente selettore di classe CSS:

```
 .s7videoviewer .s7videoscrubber .s7chapter .s7header .s7starttime
```

**Proprietà CSS del tempo di inizio del capitolo video**

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
   <td colname="col2"> <p>Dimensione del font. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family </span> </p> </td> 
   <td colname="col2"> <p>Famiglia di font. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> spaziatura destra </span> </p> </td> 
   <td colname="col2"> <p> Spaziatura tra l’ora di inizio e il titolo del capitolo. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Esempio** - Per impostare l&#39;ora di inizio del capitolo utilizzando un carattere Verdana grigio con dieci pixel e con una spaziatura di dieci pixel a destra.

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
   <td colname="col2"> <p>Colore del testo del titolo del capitolo video. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-weight </span> </p> </td> 
   <td colname="col2"> <p>Titolo del capitolo video spessore del font. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size </span> </p> </td> 
   <td colname="col2"> <p>Dimensione del font del titolo del capitolo video. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family </span> </p> </td> 
   <td colname="col2"> <p>Famiglia di font del titolo del capitolo video. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Esempio** - Per impostare un titolo del capitolo video che utilizza un font Verdana bianco, grassetto, di dieci pixel.

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
   <td colname="col2"> <p>Colore del testo della descrizione del capitolo video. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p>Colore di sfondo della descrizione del capitolo video. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-weight </span> </p> </td> 
   <td colname="col2"> <p>Descrizione del capitolo video spessore del font. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size </span> </p> </td> 
   <td colname="col2"> <p>Descrizione del capitolo video, dimensioni del font. </p> </td> 
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
   <td colname="col1"> <p> <span class="codeph"> spaziatura </span> </p> </td> 
   <td colname="col2"> <p>Spaziatura interna descrizione capitolo video. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Esempio** - Per impostare la descrizione del capitolo video con un carattere Verdana grigio scuro di 11 pixel, con uno sfondo grigio chiaro; Altezza della riga di 5 pixel, spaziatura orizzontale di 12 pixel, spaziatura superiore di 12 pixel e spaziatura inferiore di 9 pixel.

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

Il connettore cuneo nella parte inferiore della bolla dei capitoli è controllato dal seguente selettore di classe CSS:

```
 .s7videoviewer .s7videoscrubber .s7chapter .s7tail
```

**Proprietà CSS del connettore cuneo**

<table id="table_BC6AFB57D9404A84A3AE657448C0EB06"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> border-color </span> </p> </td> 
   <td colname="col2"> <p>Colore connettore cuneo. </p> <p>Definito come trasparente <span class="codeph"> &lt;color&gt;, in modo </span> che solo il colore del bordo superiore sia definito e i bordi rimanenti siano lasciati trasparenti. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> border-width </span> </p> </td> 
   <td colname="col2"> <p> Larghezza connettore cuneo. </p> <p>È definito come <span class="codeph"> &lt;width&gt; &lt;width&gt; 0 </span> , in modo che la stessa larghezza sia definita solo per i bordi superiore e orizzontale e la larghezza inferiore sia <span class="codeph"> 0 </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin </span> </p> </td> 
   <td colname="col2"> <p> Definisce solo un margine inferiore negativo. Deve avere lo stesso valore di <span class="codeph"> border-width </span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Esempio** : per impostare un connettore cuneo grigio di sei pixel:

```
.s7videoviewer .s7videoscrubber .s7chapter .s7tail { 
border-color: rgba(221, 221, 221, 0.9) transparent transparent; 
border-width: 6px 6px 0; 
margin: 0 0 0 -6px; 
}
```

