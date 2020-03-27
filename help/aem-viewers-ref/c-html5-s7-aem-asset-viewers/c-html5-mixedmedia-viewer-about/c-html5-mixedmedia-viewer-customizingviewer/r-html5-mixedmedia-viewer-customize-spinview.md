---
description: La vista principale consiste nell’immagine a 360 gradi quando la risorsa corrente è un set 360 gradi.
seo-description: La vista principale consiste nell’immagine a 360 gradi quando la risorsa corrente è un set 360 gradi.
seo-title: Visualizzazione 360 gradi
solution: Experience Manager
title: Visualizzazione 360 gradi
topic: Dynamic media
uuid: f1edbcc4-966a-4ec6-8ba9-a76f3ae51733
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef

---


# Spin view{#spin-view}

La vista principale consiste nell’immagine a 360 gradi quando la risorsa corrente è un set 360 gradi.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**Proprietà CSS dell&#39;area visualizzatore principale**

L&#39;aspetto dell&#39;area di visualizzazione è controllato dal seguente selettore di classe CSS:

```
.s7mixedmediaviewer .s7spinview
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
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p> Colore di sfondo nel formato esadecimale della visualizzazione a 360 gradi. </p> </td> 
  </tr> 
 </tbody> 
</table>

Esempio: per rendere trasparente la visualizzazione a 360 gradi.

```
.s7mixedmediaviewer .s7spinview { 
 background-color: transparent; 
}
```

