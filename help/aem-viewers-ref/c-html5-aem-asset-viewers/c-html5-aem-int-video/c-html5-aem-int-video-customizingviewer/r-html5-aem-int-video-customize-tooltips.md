---
title: Descrizioni comandi
description: Sui sistemi desktop, alcuni elementi dell’interfaccia utente, ad esempio i pulsanti, dispongono di descrizioni comandi visualizzate al passaggio del mouse.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: 430809d8-3d51-49b7-b6bf-c3c3c77501ff
source-git-commit: 6aaf4eccf51a05d200c6cc780e342be646d104d8
workflow-type: tm+mt
source-wordcount: '138'
ht-degree: 7%

---

# Descrizioni comandi{#tooltips}

Sui sistemi desktop, alcuni elementi dell’interfaccia utente, ad esempio i pulsanti, dispongono di descrizioni comandi visualizzate al passaggio del mouse.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**Proprietà CSS dell’area visualizzatore principale**

L’aspetto delle descrizioni dei comandi è controllato dal seguente selettore di classi CSS:

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
   <td colname="col1"> <p> <span class="codeph"> raggio bordo  </span> </p> </td> 
   <td colname="col2"> <p> Raggio del bordo di sfondo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> colore bordo  </span> </p> </td> 
   <td colname="col2"> <p> Colore bordo sfondo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> colore di sfondo  </span> </p> </td> 
   <td colname="col2"> <p> Colore di sfondo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color </span> </p> </td> 
   <td colname="col2"> <p>Colore testo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family  </span> </p> </td> 
   <td colname="col2"> <p>Nome font testo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size  </span> </p> </td> 
   <td colname="col2"> <p>Dimensione del font del testo. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Nel caso in cui gli stili della descrizione comandi siano personalizzati dall’interno della pagina web di incorporamento, tutte le proprietà devono contenere la regola `!IMPORTANT` . Questa nota non è necessaria se le descrizioni comandi sono personalizzate all’interno del file CSS del visualizzatore.

## Esempio {#section-59e009fd05b14019936aba04d7ca779d}

Per impostare descrizioni comandi con bordo grigio con raggio d’angolo di tre pixel, sfondo nero e testo bianco in Arial®, 11 pixel:

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
