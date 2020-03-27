---
description: L'evidenziazione dello stato attivo visualizzata attorno all'elemento dell'interfaccia utente del visualizzatore mirato è controllata dal selettore di classe CSS.
seo-description: L'evidenziazione dello stato attivo visualizzata attorno all'elemento dell'interfaccia utente del visualizzatore mirato è controllata dal selettore di classe CSS.
seo-title: Evidenziazione dello stato
solution: Experience Manager
title: Evidenziazione dello stato
topic: Dynamic media
uuid: 44057e10-98b6-4316-bf6c-9bf569be6a50
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef

---


# Evidenziazione dello stato{#focus-highlight}

L&#39;evidenziazione dello stato attivo visualizzata attorno all&#39;elemento dell&#39;interfaccia utente del visualizzatore mirato è controllata dal selettore di classe CSS.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**Proprietà CSS**

L&#39;aspetto è controllato dal seguente selettore di classe CSS:

```
.s7interactivevideoviewer *:focus
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
   <td colname="col1"> <p> <span class="codeph"> contorno </span> </p> </td> 
   <td colname="col2"> <p>Stile evidenziazione dello stato attivo. </p> </td> 
  </tr> 
 </tbody> 
</table>

Esempio: per disattivare l&#39;evidenziazione dello stato attivo predefinito del browser per tutti gli elementi dell&#39;interfaccia utente del visualizzatore, aggiungete il seguente selettore CSS al foglio di stile del visualizzatore:

```
.s7interactivevideoviewer *:focus { 
 outline: none; 
}
```

