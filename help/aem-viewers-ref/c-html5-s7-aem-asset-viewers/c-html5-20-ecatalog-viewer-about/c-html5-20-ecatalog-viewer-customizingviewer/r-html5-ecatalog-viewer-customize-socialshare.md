---
title: Condivisione social
description: Per impostazione predefinita, lo strumento condivisione social viene visualizzato nell'angolo superiore sinistro. È costituito da un pulsante e da un pannello che si espande quando l’utente fa clic o tocca un pulsante e contiene singoli strumenti di condivisione.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: b65b8846-3287-47ae-bdb6-6cac768cece0
source-git-commit: edc127dc6e2ae2d9bd5feed08c8bc896c8c39747
workflow-type: tm+mt
source-wordcount: '330'
ht-degree: 0%

---

# Condivisione social{#social-share}

Per impostazione predefinita, lo strumento condivisione social viene visualizzato nell&#39;angolo superiore sinistro. È costituito da un pulsante e da un pannello che si espande quando l’utente fa clic o tocca un pulsante e contiene singoli strumenti di condivisione.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

La posizione e le dimensioni dello strumento di condivisione social network nell’interfaccia utente del visualizzatore sono controllate da quanto segue:

```
.s7ecatalogviewer .s7socialshare
```

**Proprietà CSS dello strumento condivisione social**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin-top </span> </p> </td> 
   <td colname="col2"> <p> Offset dalla parte superiore della barra di controllo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin=left </span> </p> </td> 
   <td colname="col2"> <p> Distanza dal pulsante successivo a sinistra o dal lato sinistro della barra di controllo se si tratta del primo pulsante di una riga. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p> Larghezza dello strumento di condivisione social. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Altezza dello strumento di condivisione social. </p> </td> 
  </tr> 
 </tbody> 
</table>

Esempio: per impostare uno strumento di condivisione social, posizionato quattro pixel dall’alto e cinque pixel dalla destra del contenitore visualizzatore e ridimensionato a 28 x 28 pixel:

```
.s7ecatalogviewer .s7socialshare { 
margin-top: 4px; 
margin-left: 10px; width:28px; 
 height:28px; 
}
```

L’aspetto del pulsante dello strumento Condivisione social è controllato dal seguente selettore di classe CSS:

```
.s7ecatalogviewer .s7socialshare .s7socialbutton
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
   <td colname="col2"> <p> Posizionate all'interno dello sprite del disegno, se vengono utilizzati gli sprite CSS. </p> <p>Vedi anche <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-customizingviewer/c-html5-20-ecatalog-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> Spunti CSS </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Questo pulsante supporta `state` selettore di attributi, che può essere utilizzato per applicare interfacce diverse a stati di pulsante diversi.

La descrizione comando del pulsante può essere localizzata. Consulta [Localizzazione degli elementi dell’interfaccia utente](../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) per ulteriori informazioni.

Esempio: per impostare un pulsante dello strumento di condivisione social network che mostri un’immagine diversa per ciascuno dei quattro stati dei pulsanti:

```
.s7ecatalogviewer .s7socialshare .s7socialbutton[state='up'] { 
background-image:url(images/v2/SocialShare_video_dark_up.png); 
} 
.s7ecatalogviewer .s7socialshare .s7socialbutton[state='over'] { 
background-image:url(images/v2/SocialShare_dark_over.png); 
} 
.s7ecatalogviewer .s7socialshare .s7socialbutton[state='down'] { 
background-image:url(images/v2/SocialShare_dark_down.png); 
} 
.s7ecatalogviewer .s7socialshare .s7socialbutton[state='disabled'] { 
background-image:url(images/v2/SocialShare_dark_disabled.png); 
}
```

L’aspetto del pannello che contiene le singole icone di condivisione social è controllato dal seguente selettore di classe CSS:

```
.s7ecatalogviewer .s7socialshare .s7socialsharepanel
```

**Proprietà CSS del pannello Condivisione social**

<table id="table_86E777A5851F47D6A49D966E24A9A6CD"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p>Colore di sfondo del pannello. </p> </td> 
  </tr> 
 </tbody> 
</table>

Esempio: per impostare un pannello con un colore trasparente:

```
.s7ecatalogviewer .s7socialshare .s7socialsharepanel { 
 background-color: transparent; 
}
```
