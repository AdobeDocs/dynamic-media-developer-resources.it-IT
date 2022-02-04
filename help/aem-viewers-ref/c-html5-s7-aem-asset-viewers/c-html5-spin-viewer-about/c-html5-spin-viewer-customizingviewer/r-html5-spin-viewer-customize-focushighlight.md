---
title: Evidenziazione
description: L’evidenziazione dello stato attivo visualizzata intorno all’elemento dell’interfaccia utente del visualizzatore mirato è controllata dal selettore di classi CSS.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Spin Sets
role: Developer,User
exl-id: dc59e081-97cc-46fe-a8f7-0690833a8290
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '78'
ht-degree: 1%

---

# Evidenziazione{#focus-highlight}

L’evidenziazione dello stato attivo visualizzata intorno all’elemento dell’interfaccia utente del visualizzatore mirato è controllata dal selettore di classi CSS.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**Proprietà CSS**

L’aspetto viene controllato con il seguente selettore di classe CSS:

```
.s7spinviewer *:focus
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
   <td colname="col2"> <p>Stile evidenziazione focus. </p> </td> 
  </tr> 
 </tbody> 
</table>

Esempio: per disattivare l’evidenziazione dello stato attivo predefinito del browser per tutti gli elementi dell’interfaccia utente del visualizzatore, aggiungi il seguente selettore CSS al foglio di stile del visualizzatore:

```
.s7spinviewer *:focus { 
 outline: none; 
}
```
