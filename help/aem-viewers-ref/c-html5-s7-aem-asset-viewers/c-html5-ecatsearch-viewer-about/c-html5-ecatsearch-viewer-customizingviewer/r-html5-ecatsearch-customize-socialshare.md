---
description: Per impostazione predefinita, lo strumento di condivisione social network viene visualizzato nell'angolo superiore sinistro. È costituito da un pulsante e da un pannello che si espande quando l’utente fa clic su un pulsante o tocca un pulsante e contiene singoli strumenti di condivisione.
seo-description: Per impostazione predefinita, lo strumento di condivisione social network viene visualizzato nell'angolo superiore sinistro. È costituito da un pulsante e da un pannello che si espande quando l’utente fa clic su un pulsante o tocca un pulsante e contiene singoli strumenti di condivisione.
seo-title: Condivisione social network
solution: Experience Manager
title: Condivisione social network
topic: Dynamic media
uuid: 6d463eb1-c6bf-4f1c-90e4-b5ef1e5a1538
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef

---


# Condivisione social network{#social-share}

Per impostazione predefinita, lo strumento di condivisione social network viene visualizzato nell&#39;angolo superiore sinistro. È costituito da un pulsante e da un pannello che si espande quando l’utente fa clic su un pulsante o tocca un pulsante e contiene singoli strumenti di condivisione.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

La posizione e le dimensioni dello strumento di condivisione mediante social network nell&#39;interfaccia utente del visualizzatore sono controllate dai seguenti elementi:

```
.s7ecatalogsearchviewer .s7socialshare
```

**Proprietà CSS dello strumento di condivisione mediante social network**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin-top </span> </p> </td> 
   <td colname="col2"> <p> L'offset dalla parte superiore della barra di controllo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin=left </span> </p> </td> 
   <td colname="col2"> <p> La distanza dal pulsante successivo a sinistra o dal lato sinistro della barra di controllo, se si tratta del primo pulsante di una riga. </p> </td> 
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

Esempio: configurate uno strumento di condivisione social network che si posiziona a quattro pixel dalla parte superiore e cinque pixel dalla parte destra del contenitore del visualizzatore e viene ridimensionato a 28 x 28 pixel.

```
.s7ecatalogsearchviewer .s7socialshare { 
margin-top: 4px; 
margin-left: 10px; width:28px; 
 height:28px; 
}
```

L&#39;aspetto del pulsante dello strumento di condivisione mediante social network è controllato dal seguente selettore di classe CSS:

```
.s7ecatalogsearchviewer .s7socialshare .s7socialbutton
```

**Proprietà CSS del pulsante social**

<table id="table_A18B6978EC304C378F5FE92DD44D138D"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image </span> </p> </td> 
   <td colname="col2"> <p> Immagine visualizzata per un determinato stato del pulsante. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> Posizionare all'interno dello sprite della grafica, se vengono utilizzati gli spriti CSS. </p> <p>Consultate anche <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-customizingviewer/c-html5-ecatsearch-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> CSS Sprite </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Questo pulsante supporta il selettore `state` di attributi, che può essere utilizzato per applicare interfacce diverse a stati di pulsante diversi.

La descrizione del pulsante può essere localizzata. Per ulteriori informazioni, consultate [Localizzazione degli elementi](../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) dell&#39;interfaccia utente.

Esempio: impostare un pulsante dello strumento di condivisione mediante social network che visualizzi un&#39;immagine diversa per ciascuno dei quattro stati del pulsante.

```
.s7ecatalogsearchviewer .s7socialshare .s7socialbutton[state='up'] { 
background-image:url(images/v2/SocialShare_video_dark_up.png); 
} 
.s7ecatalogsearchviewer .s7socialshare .s7socialbutton[state='over'] { 
background-image:url(images/v2/SocialShare_dark_over.png); 
} 
.s7ecatalogsearchviewer .s7socialshare .s7socialbutton[state='down'] { 
background-image:url(images/v2/SocialShare_dark_down.png); 
} 
.s7ecatalogsearchviewer .s7socialshare .s7socialbutton[state='disabled'] { 
background-image:url(images/v2/SocialShare_dark_disabled.png); 
}
```

L&#39;aspetto del pannello che contiene le singole icone di condivisione mediante social network è controllato dal seguente selettore di classe CSS:

```
.s7ecatalogsearchviewer .s7socialshare .s7socialsharepanel
```

**Proprietà CSS del pannello Condivisione social network**

<table id="table_86E777A5851F47D6A49D966E24A9A6CD"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p>Colore di sfondo del pannello. </p> </td> 
  </tr> 
 </tbody> 
</table>

Esempio: impostare un pannello con colore trasparente:

```
.s7ecatalogsearchviewer .s7socialshare .s7socialsharepanel { 
 background-color: transparent; 
}
```

