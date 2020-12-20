---
description: L'evidenziazione dello stato attivo visualizzata attorno all'elemento dell'interfaccia utente del visualizzatore mirato è controllata dal selettore di classe CSS.
seo-description: L'evidenziazione dello stato attivo visualizzata attorno all'elemento dell'interfaccia utente del visualizzatore mirato è controllata dal selettore di classe CSS.
seo-title: Evidenziazione dello stato
solution: Experience Manager
title: Evidenziazione dello stato
topic: Dynamic media
uuid: ab7d3a24-46a9-4c74-a7ba-6e53ebf4cf1c
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef
workflow-type: tm+mt
source-wordcount: '96'
ht-degree: 1%

---


# Evidenziazione della messa a fuoco{#focus-highlight}

L&#39;evidenziazione dello stato attivo visualizzata attorno all&#39;elemento dell&#39;interfaccia utente del visualizzatore mirato è controllata dal selettore di classe CSS.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**Proprietà CSS**

L&#39;aspetto è controllato dal seguente selettore di classe CSS:

```
.s7flyoutviewer *:focus
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
   <td colname="col1"> <p> <span class="codeph"> contorno  </span> </p> </td> 
   <td colname="col2"> <p>Stile evidenziazione dello stato attivo. </p> </td> 
  </tr> 
 </tbody> 
</table>

Esempio: per disattivare l&#39;evidenziazione dello stato attivo predefinito del browser per tutti gli elementi dell&#39;interfaccia utente del visualizzatore, aggiungete il seguente selettore CSS al foglio di stile del visualizzatore:

```
.s7flyoutviewer *:focus { 
 outline: none; 
}
```

