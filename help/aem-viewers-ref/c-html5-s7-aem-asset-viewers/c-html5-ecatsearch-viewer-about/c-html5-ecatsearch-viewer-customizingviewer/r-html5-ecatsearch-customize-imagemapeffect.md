---
description: A seconda del valore del parametro della modalità, il visualizzatore visualizza le icone della mappa immagine sulla vista principale in luoghi in cui le mappe sono originariamente create in Dynamic Media Classic o esegue il rendering delle aree esatte che corrispondono alla forma delle mappe immagine originali.
solution: Experience Manager
title: Effetto mappa immagine
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '325'
ht-degree: 1%

---


# Effetto mappa immagine{#image-map-effect}

A seconda del valore del parametro della modalità, il visualizzatore visualizza le icone della mappa immagine sulla vista principale in luoghi in cui le mappe sono originariamente create in Dynamic Media Classic o esegue il rendering delle aree esatte che corrispondono alla forma delle mappe immagine originali.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**Proprietà CSS dell’area visualizzatore principale**

L’aspetto dell’icona mappa immagine è controllato dal seguente selettore di classe CSS:

```
.s7ecatalogsearchviewer .s7imagemapeffect .s7icon
```

>[!NOTE]
>
>La classe CSS `s7mapoverlay` utilizzata in passato per assegnare uno stile alle icone delle mappe immagine è ora obsoleta. utilizza invece `s7icon` .

<table id="table_94EE3F5BBE4547C0B4943471CEE7EDE4"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> Proprietà CSS </p> </th> 
   <th colname="col2" class="entry"> <p>Descrizione </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> immagine di sfondo  </span> </p> </td> 
   <td colname="col2"> <p>Immagine icona mappa immagine. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> posizione di sfondo  </span> </p> </td> 
   <td colname="col2"> <p> Posizione all’interno dello sprite di un’immagine, se vengono utilizzati gli spriti CSS. </p> <p>Vedi anche <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-customizingviewer/c-html5-ecatsearch-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> Sprite CSS </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Larghezza icona mappa immagine in pixel. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Altezza dell'icona della mappa immagine in pixel. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>L’icona della mappa immagine supporta il selettore di attributi `state` , che è possibile utilizzare per applicare interfacce diverse agli stati delle icone `default` e `active`.

Esempio : imposta un’icona di mappa immagine da 28 x 28 pixel che mostra un’immagine diversa per ciascuno dei due stati dell’icona diversi.

```
.s7ecatalogsearchviewer .s7imagemapeffect .s7icon { 
 height: 28px; 
 width: 28px;  
 background-image: url(images/v2/ImageMapEffect_dark_up.png); 
} 
.s7ecatalogsearchviewer .s7imagemapeffect .s7icon[state="default"] { 
 opacity: 0.5; 
} 
.s7ecatalogsearchviewer .s7imagemapeffect .s7icon[state="active"] { 
opacity: 1; 
}
```

Vedere anche [Supporto mappa immagine](../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-image-map-support.md#concept-28759efae5014a1fa8b0fb14dc26812a).

L’aspetto dell’area della mappa immagine è controllato con il seguente selettore di classe CSS:

```
.s7ecatalogsearchviewer .s7imagemapeffect .s7region
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
   <td colname="col1"> <p> <span class="codeph"> sfondo  </span> </p> </td> 
   <td colname="col2"> <p> Colore di riempimento area mappa immagine. </p> <p>Specificato in formato #RRGGBB, RGB(R,G,B) o RGBA(R,G,B,A). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> colore di sfondo  </span> </p> </td> 
   <td colname="col2"> <p> Colore di riempimento area mappa immagine. </p> <p>Specificato in formato #RRGGBB, RGB(R,G,B) o RGBA(R,G,B,A). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> border  </span> </p> </td> 
   <td colname="col2"> <p> Stile del bordo della regione mappa immagine. </p> <p>Specificato come <span class="codeph"> <span class="varname"> larghezza </span> tinta unita <span class="varname"> colore </span> </span>, dove <span class="codeph"> <span class="varname"> larghezza </span> </span> è espresso in pixel e <span class="codeph"> <span class="varname"> colore </span> </span> è impostato come #RRGGBB, RGB(R,G,B) o RGBA(R,G,B,A). </p> </td> 
  </tr> 
 </tbody> 
</table>

Esempio : imposta un&#39;area mappa immagine trasparente con `1` bordo nero pixel :

```
.s7ecatalogsearchviewer .s7imagemapeffect .s7region { 
 border: 1px solid #000000; 
 background: RGBA(0,0,0,0);  
}
```

