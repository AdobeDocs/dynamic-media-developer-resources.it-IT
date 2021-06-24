---
description: Evidenziazione dello stato attivo visualizzata intorno all'elemento dell'interfaccia utente del visualizzatore mirato.
solution: Experience Manager
title: Evidenziazione
feature: Dynamic Media Classic,Visualizzatori,SDK/API,eCatalog
role: Developer,Business Practitioner
exl-id: 3d5737d7-1295-46a9-9b84-c43269e5a914
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '81'
ht-degree: 0%

---

# Evidenziazione{#focus-highlight}

Evidenziazione dello stato attivo visualizzata intorno all&#39;elemento dell&#39;interfaccia utente del visualizzatore mirato.

<!--<a id="section_E8B3D0BF9FF548F188F717D6EA65EC32"></a>-->

L’aspetto dell’evidenziazione dello stato attivo è controllato con il seguente selettore di classe CSS:

```
.s7ecatalogviewer *:focus
```

**Proprietà CSS dell&#39;evidenziazione**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> contorno  </span> </p> </td> 
   <td colname="col2"> <p> Stile evidenziazione focus. </p> </td> 
  </tr> 
 </tbody> 
</table>

Esempio: per disabilitare l’evidenziazione di attivazione predefinita del browser per tutti gli elementi dell’interfaccia utente del visualizzatore, aggiungi il seguente selettore CSS al foglio di stile del visualizzatore:

```
.s7ecatalogviewer *:focus { 
 outline: none; 
}
```
