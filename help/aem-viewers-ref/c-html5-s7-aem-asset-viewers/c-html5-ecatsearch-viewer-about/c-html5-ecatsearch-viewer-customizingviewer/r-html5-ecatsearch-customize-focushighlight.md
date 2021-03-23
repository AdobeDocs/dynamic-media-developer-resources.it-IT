---
description: Evidenziazione dello stato attivo visualizzata intorno all'elemento dell'interfaccia utente del visualizzatore mirato.
seo-description: Evidenziazione dello stato attivo visualizzata intorno all'elemento dell'interfaccia utente del visualizzatore mirato.
seo-title: Evidenziazione
solution: Experience Manager
title: Evidenziazione
uuid: 0bd36795-e663-4f0e-8310-a57c2ffae4a2
feature: Dynamic Media Classic,Visualizzatori,SDK/API,Ricerca eCatalog
role: Sviluppatore, Business Practices
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '98'
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

