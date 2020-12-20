---
description: Per impostazione predefinita, lo strumento di condivisione social network viene visualizzato nell'angolo superiore destro. È costituito da un pulsante e un pannello che si espande quando l'utente fa clic o tocca un pulsante e contiene singoli strumenti di condivisione.
seo-description: Per impostazione predefinita, lo strumento di condivisione social network viene visualizzato nell'angolo superiore destro. È costituito da un pulsante e un pannello che si espande quando l'utente fa clic o tocca un pulsante e contiene singoli strumenti di condivisione.
seo-title: Condivisione social network
solution: Experience Manager
title: Condivisione social network
topic: Dynamic media
uuid: 1123e96a-581f-4c1c-ad95-9804e3235002
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef
workflow-type: tm+mt
source-wordcount: '357'
ht-degree: 1%

---


# Condivisione social network{#social-share}

Per impostazione predefinita, lo strumento di condivisione social network viene visualizzato nell&#39;angolo superiore destro. È costituito da un pulsante e un pannello che si espande quando l&#39;utente fa clic o tocca un pulsante e contiene singoli strumenti di condivisione.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

La posizione e le dimensioni dello strumento di condivisione mediante social network nell&#39;interfaccia utente del visualizzatore sono controllate dai seguenti elementi:

```
.s7interactivevideoviewer .s7socialshare
```

**Proprietà CSS dello strumento di condivisione mediante social network**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> top  </span> </p> </td> 
   <td colname="col2"> <p> Posizione verticale dello strumento di condivisione social network rispetto al contenitore del visualizzatore. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> left  </span> </p> </td> 
   <td colname="col2"> <p> Posizione orizzontale dello strumento di condivisione social network rispetto al contenitore del visualizzatore. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p> Larghezza dello strumento di condivisione mediante social network. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Altezza dello strumento di condivisione mediante social network. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Esempio {#example}

Per impostare uno strumento di condivisione mediante social network che si posiziona a quattro pixel dalla parte superiore e cinque pixel dalla parte destra del contenitore del visualizzatore e abbia dimensioni pari a 28x28 pixel.

```
.s7interactivevideoviewer .s7socialshare { 
 top:4px; 
 right:5px; 
 width:28px; 
 height:28px; 
}
```

L&#39;aspetto del pulsante dello strumento di condivisione mediante social network è controllato dal seguente selettore di classe CSS:

```
.s7interactivevideoviewer .s7socialshare .s7socialbutton
```

**Proprietà CSS del pulsante dello strumento di condivisione mediante social network**

<table id="table_A18B6978EC304C378F5FE92DD44D138D"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image  </span> </p> </td> 
   <td colname="col2"> <p> Immagine visualizzata per un determinato stato del pulsante. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position  </span> </p> </td> 
   <td colname="col2"> <p> Posizionare all'interno dello sprite della grafica, se vengono utilizzati gli spriti CSS. </p> <p>Consultate <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-customizingviewer/c-html5-aem-int-video-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> Sprite CSS </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Questo pulsante supporta il selettore di attributi `state`, che può essere utilizzato per applicare interfacce diverse a diversi stati del pulsante.

La descrizione del pulsante può essere localizzata. Vedere [Localizzazione degli elementi dell&#39;interfaccia utente](../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74).

## Esempio {#example-1}

Per impostare un pulsante dello strumento di condivisione mediante social network che visualizzi un&#39;immagine diversa per ciascuno dei quattro stati del pulsante.

```
.s7interactivevideoviewer .s7socialshare .s7socialbutton[state='up'] { 
background-image:url(images/v2/SocialShare_video_dark_up.png); 
} 
.s7interactivevideoviewer .s7socialshare .s7socialbutton[state='over'] { 
background-image:url(images/v2/SocialShare_dark_over.png); 
} 
.s7interactivevideoviewer .s7socialshare .s7socialbutton[state='down'] { 
background-image:url(images/v2/SocialShare_dark_down.png); 
} 
.s7interactivevideoviewer .s7socialshare .s7socialbutton[state='disabled'] { 
background-image:url(images/v2/SocialShare_dark_disabled.png); 
}
```

L&#39;aspetto del pannello che contiene le singole icone di condivisione mediante social network è controllato dal seguente selettore di classe CSS:

```
.s7interactivevideoviewer .s7socialshare .s7socialsharepanel
```

**Proprietà CSS del pannello Condivisione social network**

<table id="table_86E777A5851F47D6A49D966E24A9A6CD"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color  </span> </p> </td> 
   <td colname="col2"> <p>Colore di sfondo del pannello. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Esempio {#example-2}

Per impostare un pannello con colore trasparente:

```
.s7interactivevideoviewer .s7socialshare .s7socialsharepanel { 
 background-color: transparent; 
}
```

