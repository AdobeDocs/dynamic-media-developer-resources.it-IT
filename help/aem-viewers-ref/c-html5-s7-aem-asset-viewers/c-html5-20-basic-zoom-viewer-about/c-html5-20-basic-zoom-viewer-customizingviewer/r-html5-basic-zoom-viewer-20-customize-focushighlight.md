---
description: L’evidenziazione dello stato attivo visualizzata intorno all’elemento dell’interfaccia utente del visualizzatore mirato è controllata con il selettore di classi CSS.
solution: Experience Manager
title: Evidenziazione
feature: Dynamic Media Classic,Visualizzatori,SDK/API,Zoom
role: Developer,User
exl-id: 74ff9669-d56b-4731-9d4a-dda7c831e162
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '85'
ht-degree: 1%

---

# Evidenziazione{#focus-highlight}

L’evidenziazione dello stato attivo visualizzata intorno all’elemento dell’interfaccia utente del visualizzatore mirato è controllata con il selettore di classi CSS.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

L’aspetto viene controllato con il seguente selettore di classe CSS:

```
.s7basiczoomviewer *:focus
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
.s7basiczoomviewer *:focus { 
 outline: none; 
}
```
