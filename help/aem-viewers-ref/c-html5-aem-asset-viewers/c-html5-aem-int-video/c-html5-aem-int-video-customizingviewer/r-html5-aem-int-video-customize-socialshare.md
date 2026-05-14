---
title: Condivisione social
description: Per impostazione predefinita, lo strumento condivisione social viene visualizzato nell'angolo in alto a destra. È costituito da un pulsante e da un pannello che si espande quando l’utente fa clic o tocca un pulsante e contiene singoli strumenti di condivisione.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: ad544a12-d2a4-45c9-9e76-e0bf96901725
TQID: 'https://experienceleague.adobe.com/YIV6y11nCjz4iC2ODpnUOiHeDlMcQY5Sq06res4DgPM'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 324
ht-degree: 0%

---

# Condivisione social{#social-share}

Per impostazione predefinita, lo strumento condivisione social viene visualizzato nell&#39;angolo in alto a destra. È costituito da un pulsante e da un pannello che si espande quando l’utente fa clic o tocca un pulsante e contiene singoli strumenti di condivisione.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

La posizione e le dimensioni dello strumento di condivisione social network nell’interfaccia utente del visualizzatore sono controllate da quanto segue:

```
.s7interactivevideoviewer .s7socialshare
```

**Proprietà CSS dello strumento condivisione social**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> primi </span> </p> </td> 
   <td colname="col2"> <p> Posizione verticale dello strumento di condivisione social network rispetto al contenitore del visualizzatore. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ha lasciato </span> </p> </td> 
   <td colname="col2"> <p> Posizione orizzontale dello strumento di condivisione social network rispetto al contenitore del visualizzatore. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> larghezza </span> </p> </td> 
   <td colname="col2"> <p> Larghezza dello strumento di condivisione social. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> altezza </span> </p> </td> 
   <td colname="col2"> <p>Altezza dello strumento di condivisione social. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Esempio {#example}

Per impostare uno strumento di condivisione social che sia posizionato a quattro pixel dall’alto e a cinque pixel dalla destra del contenitore visualizzatore e sia ridimensionato a 28 x 28 pixel.

```
.s7interactivevideoviewer .s7socialshare { 
 top:4px; 
 right:5px; 
 width:28px; 
 height:28px; 
}
```

L’aspetto del pulsante dello strumento Condivisione social è controllato dal seguente selettore di classe CSS:

```
.s7interactivevideoviewer .s7socialshare .s7socialbutton
```

**Proprietà CSS del pulsante dello strumento condivisione social**

<table id="table_A18B6978EC304C378F5FE92DD44D138D"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> immagine di sfondo </span> </p> </td> 
   <td colname="col2"> <p> Immagine visualizzata per un determinato stato del pulsante. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> Posizionate all'interno dello sprite del disegno, se vengono utilizzati gli sprite CSS. </p> <p>Vedere <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-customizingviewer/c-html5-aem-int-video-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> sprite CSS </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Questo pulsante supporta il selettore di attributi `state`, che può essere utilizzato per applicare interfacce diverse a diversi stati di pulsante.

La descrizione comando del pulsante può essere localizzata. Vedi [Localizzazione degli elementi dell&#39;interfaccia utente](../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74).

## Esempio {#example-1}

Per impostare un pulsante dello strumento di condivisione social network che mostri un&#39;immagine diversa per ciascuno dei quattro diversi stati dei pulsanti.

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

L’aspetto del pannello che contiene le singole icone di condivisione social è controllato dal seguente selettore di classe CSS:

```
.s7interactivevideoviewer .s7socialshare .s7socialsharepanel
```

**Proprietà CSS del pannello condivisione social**

<table id="table_86E777A5851F47D6A49D966E24A9A6CD"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> colore di sfondo </span> </p> </td> 
   <td colname="col2"> <p>Colore di sfondo del pannello. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Esempio {#example-2}

Per impostare un pannello in modo che presenti un colore trasparente:

```
.s7interactivevideoviewer .s7socialshare .s7socialsharepanel { 
 background-color: transparent; 
}
```
