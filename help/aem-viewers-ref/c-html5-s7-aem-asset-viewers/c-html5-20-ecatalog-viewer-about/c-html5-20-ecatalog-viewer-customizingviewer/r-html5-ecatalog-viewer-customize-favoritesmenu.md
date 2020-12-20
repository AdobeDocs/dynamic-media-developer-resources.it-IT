---
description: L'elenco a discesa del menu Preferiti viene visualizzato nella barra di controllo. È costituito da un pulsante e da un pannello che si espande quando un utente fa clic o tocca un pulsante. Il pannello contiene i singoli strumenti Preferiti.
seo-description: L'elenco a discesa del menu Preferiti viene visualizzato nella barra di controllo. È costituito da un pulsante e da un pannello che si espande quando un utente fa clic o tocca un pulsante. Il pannello contiene i singoli strumenti Preferiti.
seo-title: Menu Preferiti
solution: Experience Manager
title: Menu Preferiti
topic: Dynamic media
uuid: 816e614d-8253-49a8-b57e-0b57b44db535
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef
workflow-type: tm+mt
source-wordcount: '360'
ht-degree: 0%

---


# Menu Preferiti{#favorites-menu}

L&#39;elenco a discesa del menu Preferiti viene visualizzato nella barra di controllo. È costituito da un pulsante e da un pannello che si espande quando un utente fa clic o tocca un pulsante. Il pannello contiene i singoli strumenti Preferiti.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

La posizione e le dimensioni del menu Preferiti nell&#39;interfaccia utente del visualizzatore sono controllate dal seguente selettore di classe CSS:

```
.s7ecatalogviewer .s7favoritesmenu
```

**Proprietà CSS del pulsante del menu Preferiti**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin-top  </span> </p> </td> 
   <td colname="col2"> <p> L'offset dalla parte superiore della barra di controllo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin-left  </span> </p> </td> 
   <td colname="col2"> <p> La distanza dal pulsante successivo a sinistra o dal lato sinistro della barra di controllo, se si tratta del primo pulsante di una riga. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Larghezza del pulsante. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Altezza del pulsante. </p> </td> 
  </tr> 
 </tbody> 
</table>

Esempio: impostare un menu Preferiti posizionato quattro pixel dalla parte superiore della barra di controllo e dieci pixel dal pulsante più vicino a sinistra e ridimensionato 28 x 28 pixel.

```
.s7ecatalogviewer .s7favoritesmenu { 
margin-top: 4px; 
margin-left: 10px; 
 width:28px; 
 height:28px; 
}
```

L&#39;aspetto del pulsante del menu Preferiti è controllato dal seguente selettore di classe CSS:

```
.s7ecatalogviewer .s7favoritesmenu .s7favoritesbutton
```

**Proprietà CSS del pulsante Preferiti**

<table id="table_970D62A1413145E0A964FA9D9F108579"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image  </span> </p> </td> 
   <td colname="col2"> <p> Immagine visualizzata per un determinato stato del pulsante. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position  </span> </p> </td> 
   <td colname="col2"> <p> Posizionare all'interno dello sprite della grafica, se vengono utilizzati gli spriti CSS. </p> <p>Vedere anche <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-customizingviewer/c-html5-20-ecatalog-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> Sprite CSS </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Questo pulsante supporta il selettore di attributi `state`, che può essere utilizzato per applicare interfacce diverse a diversi stati del pulsante.

La descrizione del pulsante può essere localizzata. Per ulteriori informazioni, vedere [Localizzazione degli elementi dell&#39;interfaccia utente](../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74).

Esempio: impostare un pulsante di menu Preferiti che visualizzi un&#39;immagine diversa per ciascuno dei quattro stati del pulsante.

```
.s7ecatalogviewer .s7favoritesmenu .s7favoritesbutton[state='up'] { 
background-image:url(images/v2/FavoritesMenu dark_up.png); 
} 
.s7ecatalogviewer .s7favoritesmenu .s7favoritesbutton[state='over'] { 
background-image:url(images/v2/FavoritesMenu_dark_over.png); 
} 
.s7ecatalogviewer .s7favoritesmenu .s7favoritesbutton[state='down'] { 
background-image:url(images/v2/FavoritesMenu_dark_down.png); 
} 
.s7ecatalogviewer .s7favoritesmenu .s7favoritesbutton[state='disabled'] { 
background-image:url(images/v2/FavoritesMenu_dark_disabled.png); 
}
```

L&#39;aspetto del pannello che contiene singole icone Preferiti è controllato dal seguente selettore di classe CSS:

```
.s7ecatalogviewer .s7favoritesmenu .s7favoritesmenupanel
```

**Proprietà CSS del pannello del menu Preferiti**

<table id="table_B57B44C561E94F86BB1B0EC1671F26DB"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color  </span> </p> </td> 
   <td colname="col2"> <p>Colore di sfondo del pannello. </p> </td> 
  </tr> 
 </tbody> 
</table>

Esempio: impostare un pannello con un colore trasparente.

```
.s7ecatalogviewer .s7favoritesmenu .s7favoritesmenupanel { 
 background-color: transparent; 
}
```

