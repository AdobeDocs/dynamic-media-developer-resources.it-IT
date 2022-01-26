---
title: Descrizioni comandi
description: Sui sistemi desktop, alcuni elementi dell'interfaccia utente come i pulsanti dispongono di descrizioni comandi visualizzate al passaggio del mouse.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: bbf8e8f0-eb1c-49fa-a501-4c7ed7827595
source-git-commit: cdc85af782ebc492ae2303469a7f4f54b5bc09c8
workflow-type: tm+mt
source-wordcount: '136'
ht-degree: 6%

---

# Descrizioni comandi{#tooltips}

Sui sistemi desktop, alcuni elementi dell&#39;interfaccia utente come i pulsanti dispongono di descrizioni comandi visualizzate al passaggio del mouse.

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
   <td colname="col1"> <p> <span class="codeph"> raggio bordo </span> </p> </td> 
   <td colname="col2"> <p> Raggio del bordo di sfondo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> colore bordo </span> </p> </td> 
   <td colname="col2"> <p> Colore bordo sfondo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> colore di sfondo </span> </p> </td> 
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
   <td colname="col2"> <p>Dimensione del font del testo. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Nel caso in cui gli stili della descrizione comandi siano personalizzati dall’interno della pagina web di incorporamento, tutte le proprietà devono contenere `!IMPORTANT` regola. Questa regola non è necessaria se le descrizioni comandi sono personalizzate nel file CSS del visualizzatore.

Esempio: per impostare descrizioni comandi con bordo grigio con raggio d&#39;angolo di 3 pixel, sfondo nero e testo bianco scritto con Arial®, dimensioni di 11 pixel:

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
