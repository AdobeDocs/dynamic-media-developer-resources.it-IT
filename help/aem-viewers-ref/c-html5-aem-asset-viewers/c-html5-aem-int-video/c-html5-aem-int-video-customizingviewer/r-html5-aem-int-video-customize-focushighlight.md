---
description: L’evidenziazione dello stato attivo visualizzata intorno all’elemento dell’interfaccia utente del visualizzatore mirato è controllata con il selettore delle classi CSS.
solution: Experience Manager
title: Evidenziazione
feature: Dynamic Media Classic,Visualizzatori,SDK/API,Video interattivi
role: Developer,User
exl-id: cb5231ed-106a-444f-aac7-06dd1a84a665
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '88'
ht-degree: 1%

---

# Evidenziazione{#focus-highlight}

L’evidenziazione dello stato attivo visualizzata intorno all’elemento dell’interfaccia utente del visualizzatore mirato è controllata con il selettore delle classi CSS.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**Proprietà CSS**

L’aspetto viene controllato con il seguente selettore di classe CSS:

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
   <td colname="col1"> <p> <span class="codeph"> contorno  </span> </p> </td> 
   <td colname="col2"> <p>Stile evidenziazione focus. </p> </td> 
  </tr> 
 </tbody> 
</table>

Esempio: per disattivare l’evidenziazione dello stato attivo predefinito del browser per tutti gli elementi dell’interfaccia utente del visualizzatore, aggiungi il seguente selettore CSS al foglio di stile del visualizzatore:

```
.s7interactivevideoviewer *:focus { 
 outline: none; 
}
```
