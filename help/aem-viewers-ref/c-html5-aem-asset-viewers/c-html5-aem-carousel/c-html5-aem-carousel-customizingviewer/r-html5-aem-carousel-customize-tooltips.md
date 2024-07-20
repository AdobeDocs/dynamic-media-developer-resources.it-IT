---
title: Descrizione
description: Sui sistemi desktop, alcuni elementi dell'interfaccia utente come i pulsanti hanno descrizioni comandi che vengono visualizzate al passaggio del mouse.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Carousel Banners
role: Developer,User
exl-id: b4604528-93f6-440c-b676-7b4c89fff6c8
source-git-commit: c99aac44711852d8ac661878e11ce0b19d3dbf60
workflow-type: tm+mt
source-wordcount: '142'
ht-degree: 0%

---

# Descrizione{#tooltips}

Sui sistemi desktop, alcuni elementi dell&#39;interfaccia utente come i pulsanti hanno descrizioni comandi che vengono visualizzate al passaggio del mouse.

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
   <td colname="col1"> <p> <span class="codeph"> raggio bordo </span> </p> </td> 
   <td colname="col2"> <p> Raggio bordo sfondo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> colore bordo </span> </p> </td> 
   <td colname="col2"> <p> Colore bordo di sfondo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> colore di sfondo </span> </p> </td> 
   <td colname="col2"> <p> Colore di sfondo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> colore </span> </p> </td> 
   <td colname="col2"> <p>Colore testo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> famiglia di caratteri </span> </p> </td> 
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
>Nel caso in cui gli stili delle descrizioni comandi siano personalizzati dalla pagina Web in cui è incorporato, tutte le proprietà devono contenere la regola `!IMPORTANT`. Questo passaggio non è necessario se le descrizioni comandi sono personalizzate nel file CSS del visualizzatore.

Esempio: per impostare descrizioni comandi con un bordo grigio con un raggio d&#39;angolo di 3 pixel, sfondo nero e testo bianco in Arial®, dimensioni di 11 pixel:

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
