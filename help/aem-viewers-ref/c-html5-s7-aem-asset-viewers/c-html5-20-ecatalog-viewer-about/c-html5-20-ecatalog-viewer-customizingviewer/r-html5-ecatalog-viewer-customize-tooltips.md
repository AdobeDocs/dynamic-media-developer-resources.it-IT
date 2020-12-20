---
description: Sui sistemi desktop, alcuni elementi dell'interfaccia utente come i pulsanti dispongono di descrizioni comandi che vengono visualizzate al passaggio del mouse.
seo-description: Sui sistemi desktop, alcuni elementi dell'interfaccia utente come i pulsanti dispongono di descrizioni comandi che vengono visualizzate al passaggio del mouse.
seo-title: Descrizioni comandi
solution: Experience Manager
title: Descrizioni comandi
topic: Dynamic media
uuid: 9f188b61-10a2-4283-b8fe-efb4593f0faf
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef
workflow-type: tm+mt
source-wordcount: '153'
ht-degree: 5%

---


# Descrizioni comandi{#tooltips}

Sui sistemi desktop, alcuni elementi dell&#39;interfaccia utente come i pulsanti dispongono di descrizioni comandi che vengono visualizzate al passaggio del mouse.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**Proprietà CSS dell&#39;area visualizzatore principale**

L&#39;aspetto delle descrizioni comandi è controllato dal seguente selettore di classe CSS:

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
   <td colname="col1"> <p> <span class="codeph"> border-radius  </span> </p> </td> 
   <td colname="col2"> <p> Raggio del bordo dello sfondo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> border-color  </span> </p> </td> 
   <td colname="col2"> <p> Colore del bordo dello sfondo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color  </span> </p> </td> 
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
>Se gli stili delle descrizioni comandi sono personalizzati dall&#39;interno della pagina Web in cui sono incorporati, tutte le proprietà devono contenere la regola `!IMPORTANT`. Questo non è necessario se le descrizioni comandi sono personalizzate nel file CSS del visualizzatore.

Esempio: per impostare le descrizioni comandi con bordo grigio con raggio d’angolo di 3 pixel, sfondo nero e testo bianco scritto con Arial, le dimensioni sono di 11 pixel:

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

