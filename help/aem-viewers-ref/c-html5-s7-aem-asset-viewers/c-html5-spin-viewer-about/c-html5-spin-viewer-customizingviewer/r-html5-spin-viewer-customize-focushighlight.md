---
description: L’evidenziazione dello stato attivo visualizzata intorno all’elemento dell’interfaccia utente del visualizzatore mirato è controllata con il selettore delle classi CSS.
seo-description: L’evidenziazione dello stato attivo visualizzata intorno all’elemento dell’interfaccia utente del visualizzatore mirato è controllata con il selettore delle classi CSS.
seo-title: Evidenziazione
solution: Experience Manager
title: Evidenziazione
uuid: 81bf9937-6a26-4f69-838e-5ba41608ac09
feature: Dynamic Media Classic,Visualizzatori,SDK/API,Set 360 gradi
role: Sviluppatore, Business Practices
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '107'
ht-degree: 0%

---


# Evidenziazione messa a fuoco{#focus-highlight}

L’evidenziazione dello stato attivo visualizzata intorno all’elemento dell’interfaccia utente del visualizzatore mirato è controllata con il selettore delle classi CSS.

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
   <td colname="col1"> <p> <span class="codeph"> contorno  </span> </p> </td> 
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

