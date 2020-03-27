---
description: A seconda del valore del parametro mode, il visualizzatore visualizza le icone delle mappe immagine sopra la visualizzazione principale, nei punti in cui le mappe sono state originariamente create in Scene7 Publishing System o riproduce le aree esatte che corrispondono alla forma delle mappe immagine originali.
seo-description: A seconda del valore del parametro mode, il visualizzatore visualizza le icone delle mappe immagine sopra la visualizzazione principale, nei punti in cui le mappe sono state originariamente create in Scene7 Publishing System o riproduce le aree esatte che corrispondono alla forma delle mappe immagine originali.
seo-title: Effetto mappa immagine
solution: Experience Manager
title: Effetto mappa immagine
topic: Dynamic media
uuid: 193d2f4e-77a2-4741-bf36-90ca31c600c6
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef

---


# Image map effect{#image-map-effect}

A seconda del valore del parametro mode, il visualizzatore visualizza le icone delle mappe immagine sopra la visualizzazione principale, nei punti in cui le mappe sono state originariamente create in Scene7 Publishing System o riproduce le aree esatte che corrispondono alla forma delle mappe immagine originali.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**Proprietà CSS dell&#39;area visualizzatore principale**

L&#39;aspetto dell&#39;icona della mappa immagine è controllato dal seguente selettore di classe CSS:

```
.s7ecatalogviewer .s7imagemapeffect .s7icon
```

>[!NOTE]
>
>La classe `s7mapoverlay` CSS utilizzata in passato per definire lo stile delle icone delle mappe immagine è ora obsoleta; utilizzate `s7icon` invece.

<table id="table_94EE3F5BBE4547C0B4943471CEE7EDE4"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> Proprietà CSS </p> </th> 
   <th colname="col2" class="entry"> <p>Descrizione </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image </span> </p> </td> 
   <td colname="col2"> <p>Immagine dell’icona della mappa immagine. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> Posizionare all'interno dello sprite della grafica, se vengono utilizzati gli spriti CSS. </p> <p>Consultate anche <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-customizingviewer/c-html5-20-ecatalog-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> CSS Sprite </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Larghezza icona mappa immagine in pixel. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Altezza dell’icona della mappa immagine in pixel. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>L’icona mappa immagine supporta il selettore `state` di attributi, che potete usare per applicare interfacce diverse agli stati delle icone `default` e `active`.

Esempio: impostate un’icona di mappa immagine da 28x28 pixel con un’immagine diversa per ciascuno dei due stati di icona.

```
.s7ecatalogviewer .s7imagemapeffect .s7icon { 
 height: 28px; 
 width: 28px;  
 background-image: url(images/v2/ImageMapEffect_dark_up.png); 
} 
.s7ecatalogviewer .s7imagemapeffect .s7icon[state="default"] { 
 opacity: 0.5; 
} 
.s7ecatalogviewer .s7imagemapeffect .s7icon[state="active"] { 
opacity: 1; 
}
```

Consultate anche Supporto per [mappe](../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-image-map-support.md#concept-28759efae5014a1fa8b0fb14dc26812a)immagine.

L&#39;aspetto dell&#39;area della mappa immagine è controllato dal seguente selettore di classe CSS:

```
.s7ecatalogviewer .s7imagemapeffect .s7region
```

<table id="table_1FF98CE842604AAABD838FF528CDC4EF"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> Proprietà CSS </p> </th> 
   <th colname="col2" class="entry"> <p>Descrizione </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background </span> </p> </td> 
   <td colname="col2"> <p> Colore di riempimento area mappa immagine </p> <p>Specificato in formato #RRGGBB, RGB(R,G,B) o RGBA(R,G,B,A). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p> Colore di riempimento area mappa immagine </p> <p>Specificato in formato #RRGGBB, RGB(R,G,B) o RGBA(R,G,B,A). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> border </span> </p> </td> 
   <td colname="col2"> <p> Stile del bordo della mappa immagine. </p> <p>Specificato come <span class="codeph"> larghezza <span class="varname"> del </span> colore in tinta unita <span class="varname"> , dove </span></span>la larghezza <span class="codeph"> <span class="varname"> </span> </span> <span class="codeph"> <span class="varname"> </span> </span> è espressa in pixel e in un colore , è impostato come #RRGGBB, RGB(R,G,B) o RGBA(R,G,B,A). </p> </td> 
  </tr> 
 </tbody> 
</table>

Esempio: impostare un&#39;area mappa immagine trasparente con bordo nero `1` in pixel:

```
.s7ecatalogviewer .s7imagemapeffect .s7region { 
 border: 1px solid #000000; 
 background: RGBA(0,0,0,0);  
}
```

