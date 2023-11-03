---
title: Descrizione
description: Nei sistemi desktop alcuni elementi dell'interfaccia utente, ad esempio i pulsanti, dispongono di descrizioni comandi visualizzate al passaggio del mouse.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,360 VR Video
role: Developer,User
exl-id: 051bfbed-103e-4fcf-9f01-93f03730397a
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '138'
ht-degree: 2%

---

# Descrizione{#tooltips}

Nei sistemi desktop alcuni elementi dell&#39;interfaccia utente, ad esempio i pulsanti, dispongono di descrizioni comandi visualizzate al passaggio del mouse.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**Proprietà CSS dell&#39;area visualizzatore principale**

L’aspetto delle descrizioni comandi è controllato dal seguente selettore di classe CSS:

```
.s7tooltip
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
   <td colname="col1"> <p> <span class="codeph"> border-radius </span> </p> </td> 
   <td colname="col2"> <p> Raggio bordo sfondo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> border-color </span> </p> </td> 
   <td colname="col2"> <p> Colore bordo di sfondo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p> Colore di sfondo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color </span> </p> </td> 
   <td colname="col2"> <p>Colore testo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family </span> </p> </td> 
   <td colname="col2"> <p>Nome font testo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size </span> </p> </td> 
   <td colname="col2"> <p>Dimensione font testo. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Se gli stili delle descrizioni comandi vengono personalizzati dalla pagina Web in cui è incorporato, tutte le proprietà devono contenere `!IMPORTANT` regola. Questa regola non è necessaria se le descrizioni comandi vengono personalizzate all’interno del file CSS del visualizzatore.

Esempio: per impostare descrizioni comandi con un bordo grigio con un raggio d&#39;angolo di tre pixel, sfondo nero e testo bianco in Arial®, 11 pixel:

```
.s7tooltip { 
 border-radius: 3px 3px 3px 3px; 
 border-color: #999999; 
 background-color: #000000; 
 color: #FFFFFF; 
 font-family: Arial, Helvetica, sans-serif; 
 font-size: 11px; 
}
```
