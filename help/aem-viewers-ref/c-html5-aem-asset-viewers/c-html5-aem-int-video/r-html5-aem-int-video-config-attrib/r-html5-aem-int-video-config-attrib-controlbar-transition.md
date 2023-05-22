---
title: ControlBar.transition
description: Attributo di configurazione per Visualizzatore video interattivo.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: a8bb32b4-0fd9-4887-98ef-31c3426092b6
source-git-commit: 17556c64af32c957ac25312e2a3288a8d86b5679
workflow-type: tm+mt
source-wordcount: '114'
ht-degree: 2%

---

# ControlBar.transition{#controlbar-transition}

Attributo di configurazione per Visualizzatore video interattivo.

` [ControlBar.|<containerId>_controls.]transition=none|fade[, *`delaytohide`*[, *`durata`*]`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|dissolvenza</span> </p> </td> 
   <td colname="col2"> <p> Specifica il tipo di effetto utilizzato per mostrare o nascondere la barra di controllo e il relativo contenuto. </p> <p>Imposta su <span class="codeph"> nessuno</span> per mostrare/nascondere subito. </p> <p>Imposta su <span class="codeph"> dissolvenza</span> per ottenere un effetto di dissolvenza graduale. Non supportato in Internet Explorer 8. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> delaytohide</span></span> </p> </td> 
   <td colname="col2"> <p> Specifica il tempo in secondi tra l'ultimo evento mouse/touch registrato dalla barra di controllo e quando la barra di controllo viene nascosta. Se impostato su <span class="codeph"> -1</span> il componente non attiva mai il suo effetto di Nascondi automatico e rimane quindi sempre visibile sullo schermo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> durata</span></span> </p> </td> 
   <td colname="col2"> <p> Imposta la durata dell'animazione di dissolvenza in entrata/in uscita, in secondi. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Proprietà {#section-1e637b22e8a44d759d588e47576891e6}

Facoltativo.

## Predefinito {#section-71fb773f814649b2885aefee68073641}

`fade,2,0.5`

## Esempio {#section-bce98c31f08a4a0ab262fab7f95ba020}

```
transition=none
```
