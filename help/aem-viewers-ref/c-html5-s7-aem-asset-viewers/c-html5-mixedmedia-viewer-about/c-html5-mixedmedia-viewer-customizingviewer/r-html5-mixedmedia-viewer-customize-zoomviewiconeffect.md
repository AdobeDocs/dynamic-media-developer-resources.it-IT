---
description: L'indicatore dello zoom viene sovrapposto all'area di visualizzazione dello zoom. Viene visualizzato quando l’immagine è in uno stato di reset e dipende anche dal parametro iconeffect.
solution: Experience Manager
title: Effetto icona visualizzazione zoom
feature: Dynamic Media Classic,Visualizzatori,SDK/API,Set di file multimediali diversi
role: Developer,User
exl-id: f2db0259-f1cf-41bc-86fd-97a40d01db16
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '177'
ht-degree: 1%

---

# Effetto icona visualizzazione zoom{#zoom-view-icon-effect}

L&#39;indicatore dello zoom viene sovrapposto all&#39;area di visualizzazione dello zoom. Viene visualizzato quando l’immagine è in uno stato di reset e dipende anche dal parametro iconeffect.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**Proprietà CSS dell’area visualizzatore principale**

L’aspetto dell’area di visualizzazione è controllato con il seguente selettore di classe CSS:

```
.s7mixedmediaviewer .s7zoomview .s7iconeffect
```

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
   <td colname="col2"> <p> Grafico indicatore dello zoom. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> posizione di sfondo  </span> </p> </td> 
   <td colname="col2"> <p> Posizione all’interno dello sprite di un’immagine, se vengono utilizzati gli spriti CSS. </p> <p>Consulta <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/c-html5-mixedmedia-viewer-customizingviewer/c-html5-mixedmedia-viewer-customizingviewer.md#section-209a43dfbddf4fc589e79cddaf233f50" format="dita" scope="local"> Sprite CSS </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Spessore indicatore dello zoom. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Altezza indicatore dello zoom. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>L’effetto icona supporta il selettore di attributi `media-type` , che è possibile utilizzare per applicare diversi effetti icona su diversi dispositivi. In particolare, `media-type='standard'` corrisponde ai sistemi desktop in cui l&#39;input del mouse viene normalmente utilizzato e `media-type='multitouch'` corrisponde ai dispositivi con input touch.

Esempio: per impostare un indicatore di zoom da 100 x 100 pixel con grafica diversa per i sistemi desktop e i dispositivi touch.

```
.s7mixedmediaviewer .s7zoomview .s7iconeffect { 
 width: 100px; 
 height: 100px; 
} 
.s7mixedmediaviewer .s7zoomview .s7iconeffect[media-type='standard'] { 
 background-image:url(images/v2/IconEffect_zoom.png); 
} 
.s7mixedmediaviewer .s7zoomview .s7iconeffect[media-type='multitouch'] { 
 background-image:url(images/v2/IconEffect_pinch.png); 
}
```
