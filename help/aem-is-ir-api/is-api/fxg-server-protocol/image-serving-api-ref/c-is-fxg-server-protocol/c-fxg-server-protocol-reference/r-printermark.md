---
description: Visualizzare gli indicatori di stampa. Specifica come visualizzare gli indicatori di stampa.
seo-description: Visualizzare gli indicatori di stampa. Specifica come visualizzare gli indicatori di stampa.
seo-title: printerMark
solution: Experience Manager
title: printerMark
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 3e5699ce-3ccd-4f85-91dd-c40c252a758d
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '126'
ht-degree: 29%

---


# printerMark{#printermark}

Visualizzare gli indicatori di stampa. Specifica come visualizzare gli indicatori di stampa.

` printerMark= *`trim `*, *`marksbleed `*, *`marksregistration `*, *`markscolor `*, *`barspage `*, *``*, *`informationstyleline `*, *`Weight Layer incorporato`*`

I diversi indicatori possono essere disattivati o attivati. È inoltre possibile controllare lo stile degli indicatori di stampa.

Di seguito sono riportati i valori validi:

<table id="simpletable_C84560940CAC46D8BE9D0EFEE5EBF323"> 
 <tr class="strow"> 
  <td class="stentry"> <p>indicatori di rifilo= </p></td> 
  <td class="stentry"> <p>0|1 </p></td> 
  <td class="stentry"> <p>Il valore predefinito è 0. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>indicatori di pagina al vivo= </p></td> 
  <td class="stentry"> <p>0|1 </p></td> 
  <td class="stentry"> <p>Il valore predefinito è 0. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>crocini di registro= </p></td> 
  <td class="stentry"> <p>0|1 </p></td> 
  <td class="stentry"> <p>Il valore predefinito è 0. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>barre colori= </p></td> 
  <td class="stentry"> <p>0|1 </p></td> 
  <td class="stentry"> <p>Il valore predefinito è 0. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>informazioni pagina= </p></td> 
  <td class="stentry"> <p>0|1 </p></td> 
  <td class="stentry"> <p>Il valore predefinito è 0. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>style= </p></td> 
  <td class="stentry"> <p>Predefinito </p> <p>InDesignJ1 </p> <p>InDesignJ2 </p> <p>Illustrator </p> <p>IllustratorJ </p> <p>QuarkXPress </p> </td> 
  <td class="stentry"> <p>Predefinito </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>spessore linea= </p></td> 
  <td class="stentry"> <p>Qualsiasi valore compreso tra 0,125 e 2,0, entrambi i valori inclusi. </p></td> 
  <td class="stentry"> <p>Il valore predefinito è 0.25. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>incorpora in livello= </p></td> 
  <td class="stentry"> <p>0|1 </p></td> 
  <td class="stentry"> <p>Il valore predefinito è 1. </p></td> 
 </tr> 
</table>

## Esempio {#section-d2e394ddabe14f4ea63af6dab233a163}

`&printerMark=1,1,1,1,1,Illustrator,.25,1`
