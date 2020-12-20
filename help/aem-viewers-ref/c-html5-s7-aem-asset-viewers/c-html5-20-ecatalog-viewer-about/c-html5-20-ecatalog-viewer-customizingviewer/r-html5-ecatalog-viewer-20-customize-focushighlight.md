---
description: Evidenziazione dello stato attivo visualizzata attorno all'elemento dell'interfaccia utente del visualizzatore attivo.
seo-description: Evidenziazione dello stato attivo visualizzata attorno all'elemento dell'interfaccia utente del visualizzatore attivo.
seo-title: Evidenziazione dello stato
solution: Experience Manager
title: Evidenziazione dello stato
topic: Dynamic media
uuid: 50411b68-8d01-4240-b548-a6c51374a8c6
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef
workflow-type: tm+mt
source-wordcount: '87'
ht-degree: 0%

---


# Evidenziazione della messa a fuoco{#focus-highlight}

Evidenziazione dello stato attivo visualizzata attorno all&#39;elemento dell&#39;interfaccia utente del visualizzatore attivo.

<!--<a id="section_E8B3D0BF9FF548F188F717D6EA65EC32"></a>-->

L&#39;aspetto dell&#39;evidenziazione dello stato attivo è controllato dal seguente selettore di classe CSS:

```
.s7ecatalogviewer *:focus
```

**Proprietà CSS dell&#39;evidenziazione dello stato attivo**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> contorno  </span> </p> </td> 
   <td colname="col2"> <p> Stile evidenziazione dello stato attivo. </p> </td> 
  </tr> 
 </tbody> 
</table>

Esempio: per disattivare l&#39;evidenziazione dello stato attivo predefinito del browser per tutti gli elementi dell&#39;interfaccia utente del visualizzatore, aggiungete il seguente selettore CSS al foglio di stile del visualizzatore:

```
.s7ecatalogviewer *:focus { 
 outline: none; 
}
```

