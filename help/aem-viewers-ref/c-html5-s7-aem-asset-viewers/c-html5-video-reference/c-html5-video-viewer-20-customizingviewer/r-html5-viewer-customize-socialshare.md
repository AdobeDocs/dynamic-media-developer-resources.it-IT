---
title: Quota sociale
description: Per impostazione predefinita, lo strumento di condivisione social network viene visualizzato nell’angolo in alto a destra. È costituito da un pulsante e da un pannello che si espande quando l’utente fa clic o tocca un pulsante e contiene singoli strumenti di condivisione.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Video
role: Developer,User
exl-id: 82b482f9-b117-4529-a422-cdb0eead0031
source-git-commit: ceb9483f67a19d969ecbbd01cede11f3dae86467
workflow-type: tm+mt
source-wordcount: '314'
ht-degree: 0%

---

# Quota sociale{#social-share}

Per impostazione predefinita, lo strumento di condivisione social network viene visualizzato nell’angolo in alto a destra. È costituito da un pulsante e da un pannello che si espande quando l’utente fa clic o tocca un pulsante e contiene singoli strumenti di condivisione.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

La posizione e le dimensioni dello strumento di social sharing nell&#39;interfaccia utente del visualizzatore sono controllate con i seguenti elementi:

```
.s7videoviewer .s7socialshare
```

**Proprietà CSS dello strumento di social sharing**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> top </span> </p> </td> 
   <td colname="col2"> <p> Posizione verticale dello strumento di condivisione social rispetto al contenitore del visualizzatore. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> sinistra </span> </p> </td> 
   <td colname="col2"> <p> Posizione orizzontale dello strumento di condivisione social rispetto al contenitore del visualizzatore. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p> Larghezza dello strumento di condivisione social network. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Altezza dello strumento di condivisione social network. </p> </td> 
  </tr> 
 </tbody> 
</table>

Esempio : configura uno strumento di condivisione social network che si posiziona a quattro pixel dalla parte superiore e a cinque pixel dalla parte destra del contenitore del visualizzatore e viene ridimensionato a 28 x 28 pixel.

```
.s7videoviewer .s7socialshare { 
 top:4px; 
 right:5px; 
 width:28px; 
 height:28px; 
}
```

L&#39;aspetto del pulsante dello strumento di social sharing è controllato con il seguente selettore di classe CSS:

```
.s7videoviewer .s7socialshare .s7socialbutton
```

**Proprietà CSS del pulsante social**

<table id="table_A18B6978EC304C378F5FE92DD44D138D"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> immagine di sfondo </span> </p> </td> 
   <td colname="col2"> <p> Immagine visualizzata per un determinato stato del pulsante. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> posizione di sfondo </span> </p> </td> 
   <td colname="col2"> <p> Posizione all’interno dello sprite di un’immagine, se vengono utilizzati gli spriti CSS. </p> <p>Vedi <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-customizingviewer/c-html5-video-viewer-20-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> Sprite CSS </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Questo pulsante supporta `state` selettore di attributi, che può essere utilizzato per applicare interfacce diverse a diversi stati del pulsante.

La descrizione comando del pulsante può essere localizzata. Vedi [Localizzazione degli elementi dell’interfaccia utente](../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/r-html5-video-viewer-20-localization.md#concept-1d5ca2d8480f4064a51eddba13940aad) per ulteriori informazioni.

Esempio : imposta un pulsante dello strumento di condivisione social network che mostra un’immagine diversa per ciascuno dei quattro stati del pulsante.

```
.s7videoviewer .s7socialshare .s7socialbutton[state='up'] { 
background-image:url(images/v2/SocialShare_video_dark_up.png); 
} 
.s7videoviewer .s7socialshare .s7socialbutton[state='over'] { 
background-image:url(images/v2/SocialShare_dark_over.png); 
} 
.s7videoviewer .s7socialshare .s7socialbutton[state='down'] { 
background-image:url(images/v2/SocialShare_dark_down.png); 
} 
.s7videoviewer .s7socialshare .s7socialbutton[state='disabled'] { 
background-image:url(images/v2/SocialShare_dark_disabled.png); 
}
```

L&#39;aspetto del pannello che contiene le singole icone di condivisione social è controllato con il seguente selettore di classe CSS:

```
.s7videoviewer .s7socialshare .s7socialsharepanel
```

**Proprietà CSS del pannello di condivisione social**

<table id="table_86E777A5851F47D6A49D966E24A9A6CD"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> colore di sfondo </span> </p> </td> 
   <td colname="col2"> <p>Colore di sfondo del pannello. </p> </td> 
  </tr> 
 </tbody> 
</table>

Esempio: imposta un pannello con colore trasparente:

```
.s7videoviewer .s7socialshare .s7socialsharepanel { 
 background-color: transparent; 
}
```
