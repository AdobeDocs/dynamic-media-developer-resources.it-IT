---
title: Effetto mappa immagine
description: A seconda del valore del parametro mode, il visualizzatore visualizza le icone della mappa immagine sopra la vista principale nei punti in cui le mappe sono state originariamente create in Dynamic Media Classic. In alternativa, esegue il rendering delle aree esatte che corrispondono alla forma delle mappe immagine originali.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: 3816118f-4eb7-4436-9f54-155dde077734
source-git-commit: 6087b48b898e93e605c3873cbd5132b74d04225f
workflow-type: tm+mt
source-wordcount: '303'
ht-degree: 0%

---

# Effetto mappa immagine{#image-map-effect}

A seconda del valore del parametro mode, il visualizzatore visualizza le icone della mappa immagine sopra la vista principale nei punti in cui le mappe sono state originariamente create in Dynamic Media Classic. In alternativa, esegue il rendering delle aree esatte che corrispondono alla forma delle mappe immagine originali.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**Proprietà CSS dell&#39;area visualizzatore principale**

L’aspetto dell’icona mappa immagine è controllato dal seguente selettore di classe CSS:

```
.s7ecatalogviewer .s7imagemapeffect .s7icon
```

>[!NOTE]
>
>La classe CSS `s7mapoverlay` utilizzata in passato per assegnare uno stile alle icone della mappa immagine è ora obsoleta. Utilizzare `s7icon`.

<table id="table_94EE3F5BBE4547C0B4943471CEE7EDE4"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> Proprietà CSS </p> </th> 
   <th colname="col2" class="entry"> <p>Descrizione </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> immagine di sfondo </span> </p> </td> 
   <td colname="col2"> <p>Illustrazione dell'icona della mappa immagine. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> Posizionate all'interno dello sprite del disegno, se vengono utilizzati gli sprite CSS. </p> <p>Vedere anche <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-customizingviewer/c-html5-20-ecatalog-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> sprite CSS </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> larghezza </span> </p> </td> 
   <td colname="col2"> <p>Larghezza icona mappa immagine in pixel. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> altezza </span> </p> </td> 
   <td colname="col2"> <p>Altezza icona mappa immagine in pixel. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>L&#39;icona Mappa immagine supporta il selettore di attributi `state`, che è possibile utilizzare per applicare interfacce diverse agli stati di icona di `default` e `active`.

Esempio: imposta un’icona di mappa immagine di 28 x 28 pixel che visualizza un’immagine diversa per ciascuno dei due diversi stati delle icone.

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

Consulta anche [Supporto mappa immagine](../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-image-map-support.md#concept-28759efae5014a1fa8b0fb14dc26812a).

L’aspetto dell’area della mappa immagine è controllato dal seguente selettore di classe CSS:

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
   <td colname="col1"> <p> <span class="codeph"> sfondo </span> </p> </td> 
   <td colname="col2"> <p> Colore riempimento area mappa immagine. </p> <p>Specificato in formato #RRGGBB, RGB(R,G,B) o RGBA(R,G,B,A). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> colore di sfondo </span> </p> </td> 
   <td colname="col2"> <p> Colore riempimento area mappa immagine. </p> <p>Specificato in formato #RRGGBB, RGB(R,G,B) o RGBA(R,G,B,A). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> bordo </span> </p> </td> 
   <td colname="col2"> <p> Stile bordo area mappa immagine. </p> <p>Specificato come <span class="codeph"> <span class="varname"> larghezza </span> solido <span class="varname"> colore </span> </span>, dove <span class="codeph"> larghezza <span class="varname"> larghezza </span> </span> è espresso in pixel e <span class="codeph"> colore <span class="varname"> colore </span> </span> è impostato come #RRGGBB, RGB(R,G,B) o RGBA(R,G,B,A). </p> </td> 
  </tr> 
 </tbody> 
</table>

Esempio: impostare un&#39;area di mappa immagine trasparente con `1` pixel di bordo nero:

```
.s7ecatalogviewer .s7imagemapeffect .s7region { 
 border: 1px solid #000000; 
 background: RGBA(0,0,0,0);  
}
```
