---
description: Evidenziazione dello stato attivo visualizzata intorno all'elemento dell'interfaccia utente del visualizzatore mirato.
solution: Experience Manager
title: Evidenziazione
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '84'
ht-degree: 0%

---


# Evidenziazione messa a fuoco{#focus-highlight}

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

