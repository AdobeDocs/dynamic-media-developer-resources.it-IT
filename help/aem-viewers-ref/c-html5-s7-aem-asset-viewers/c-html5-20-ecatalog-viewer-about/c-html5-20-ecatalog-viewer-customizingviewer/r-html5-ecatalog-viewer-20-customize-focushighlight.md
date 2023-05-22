---
title: Evidenziazione focus
description: L’elemento attivo dell’input viene evidenziato attorno all’elemento dell’interfaccia utente del visualizzatore attivo.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: 3d5737d7-1295-46a9-9b84-c43269e5a914
source-git-commit: edc127dc6e2ae2d9bd5feed08c8bc896c8c39747
workflow-type: tm+mt
source-wordcount: '74'
ht-degree: 0%

---

# Evidenziazione focus{#focus-highlight}

L’elemento attivo dell’input viene evidenziato attorno all’elemento dell’interfaccia utente del visualizzatore attivo.

<!--<a id="section_E8B3D0BF9FF548F188F717D6EA65EC32"></a>-->

L’aspetto dell’evidenziazione dello stato attivo viene controllato con il seguente selettore di classe CSS:

```
.s7ecatalogviewer *:focus
```

**Proprietà CSS dell’evidenziazione focus**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> contorno </span> </p> </td> 
   <td colname="col2"> <p> Attiva lo stile di evidenziazione. </p> </td> 
  </tr> 
 </tbody> 
</table>

Esempio: per disattivare l’evidenziazione predefinita dello stato attivo del browser per tutti gli elementi dell’interfaccia utente del visualizzatore, aggiungi il seguente selettore CSS al foglio di stile del visualizzatore:

```
.s7ecatalogviewer *:focus { 
 outline: none; 
}
```
