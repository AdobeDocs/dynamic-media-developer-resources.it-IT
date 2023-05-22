---
title: Evidenziazione focus
description: L’evidenziazione dello stato attivo dell’input visualizzata intorno all’elemento dell’interfaccia utente del visualizzatore attivo è controllata con il selettore di classe CSS.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Flyout
role: Developer,User
exl-id: 2cb2e719-ee56-45e5-a509-7e13bb3c2165
source-git-commit: 50dddf148345d2ca5243d5d7108fefa56d23dad6
workflow-type: tm+mt
source-wordcount: '78'
ht-degree: 1%

---

# Evidenziazione focus{#focus-highlight}

L’evidenziazione dello stato attivo dell’input visualizzata intorno all’elemento dell’interfaccia utente del visualizzatore attivo è controllata con il selettore di classe CSS.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**Proprietà CSS**

L’aspetto viene controllato con il seguente selettore di classe CSS:

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
   <td colname="col1"> <p> <span class="codeph"> contorno </span> </p> </td> 
   <td colname="col2"> <p>Attiva lo stile di evidenziazione. </p> </td> 
  </tr> 
 </tbody> 
</table>

Esempio: per disattivare l’evidenziazione predefinita dello stato attivo del browser per tutti gli elementi dell’interfaccia utente del visualizzatore, aggiungi il seguente selettore CSS al foglio di stile del visualizzatore:

```
.s7flyoutviewer *:focus { 
 outline: none; 
}
```
