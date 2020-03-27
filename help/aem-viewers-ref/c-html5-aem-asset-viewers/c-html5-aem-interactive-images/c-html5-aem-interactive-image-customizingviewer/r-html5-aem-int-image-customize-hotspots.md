---
description: Il visualizzatore visualizza le icone dei punti attivi sopra la vista principale, nei punti in cui i punti attivi erano originariamente creati in Contenuti multimediali dinamici di Risorse AEM - su richiesta.
seo-description: Il visualizzatore visualizza le icone dei punti attivi sopra la vista principale, nei punti in cui i punti attivi erano originariamente creati in Contenuti multimediali dinamici di Risorse AEM - su richiesta.
seo-title: Punti attivi
solution: Experience Manager
title: Punti attivi
topic: Dynamic media
uuid: 79c4d128-e24a-43b0-8e18-13b588eb396e
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef

---


# Punti attivi{#hotspots}

Il visualizzatore visualizza le icone dei punti attivi sopra la vista principale, nei punti in cui i punti attivi erano originariamente creati in Contenuti multimediali dinamici di Risorse AEM - su richiesta.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**Proprietà CSS dell&#39;area visualizzatore principale**

L&#39;aspetto dell&#39;icona del punto di attivazione è controllato dal seguente selettore di classe CSS:

```
.s7interactiveimage .s7imagemapeffect .s7icon
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
   <td colname="col1"> <p> <span class="codeph"> background-image </span> </p> </td> 
   <td colname="col2"> <p>Grafica dell'icona del punto di attivazione. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p>Posizionarsi all'interno dello sprite della grafica, se vengono utilizzati gli spriti CSS. </p> <p>Consultate <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-interactive-images/c-html5-aem-interactive-image-customizingviewer/c-html5-aem-interactive-image-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> Spessi CSS </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Larghezza icona punto di attivazione. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Altezza icona punto di attivazione. </p> </td> 
  </tr> 
 </tbody> 
</table>

Esempio: impostate un’icona di un punto attivo da 56x56 pixel che mostra un’immagine diversa per ciascuno dei due stati di icona:

```
.s7interactiveimage .s7imagemapeffect .s7icon { 
 background-image: url(images/v2/imagemap/ImageMapEffect_icon1_light_up_touch.png); 
 width: 56px; 
 height: 56px; 
} 
.s7interactiveimage .s7imagemapeffect .s7icon:hover { 
 background-image: url(images/v2/imagemap/ImageMapEffect_icon1_light_over_touch.png); 
}
```

