---
description: Visualizza gli indicatori della stampante. Specifica come visualizzare i segni della stampante.
solution: Experience Manager
title: stampanteMark
feature: Dynamic Media Classic, SDK/API
role: Developer,User
exl-id: f61c7311-a2e9-4eb7-ae05-276a4eec980b
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '120'
ht-degree: 30%

---

# stampanteMark{#printermark}

Visualizza gli indicatori della stampante. Specifica come visualizzare i segni della stampante.

` printerMark= *`trim `*, *`marksbleed `*, *`markscolor registrazione `*, *`markscolor `*, *`barspage `*, *``*, *`informazioni `*, *`stilelinepesatura livello incorporato`*`

I diversi contrassegni possono essere disattivati o attivati. È inoltre possibile controllare lo stile dei segni della stampante.

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
  <td class="stentry"> <p>line weight= </p></td> 
  <td class="stentry"> <p>Qualsiasi valore compreso tra 0,125 e 2,0, entrambi compresi. </p></td> 
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
