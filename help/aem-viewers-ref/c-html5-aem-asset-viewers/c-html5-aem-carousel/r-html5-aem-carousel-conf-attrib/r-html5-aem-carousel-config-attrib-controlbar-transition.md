---
title: ControlBar.transition
description: Attributo di configurazione per visualizzatore carosello.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Carousel Banners
role: Developer,User
exl-id: 260a1767-e49a-46e3-9c3d-23efa5c3228e
source-git-commit: 5a7af31d6788ded908a5e1630a3b1b0723e6fb4b
workflow-type: tm+mt
source-wordcount: '122'
ht-degree: 2%

---

# ControlBar.transition{#controlbar-transition}

Attributo di configurazione per visualizzatore carosello.

` [ControlBar.|<containerId>_controlBar.]transition=none|fade[, *`delaytohide`*[, *`durata`*]`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|dissolvenza</span> </p> </td> 
   <td colname="col2"> <p> Specifica il tipo di effetto utilizzato per mostrare o nascondere la barra di controllo e il relativo contenuto. </p> <p>Imposta su <span class="codeph"> nessuno</span> per mostrare/nascondere subito. </p> <p>Imposta su <span class="codeph"> dissolvenza</span> per ottenere un effetto di dissolvenza graduale. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> delaytohide</span></span> </p> </td> 
   <td colname="col2"> <p> Specifica il tempo in secondi tra l'ultimo evento mouse/touch registrato dalla barra di controllo e quando la barra di controllo viene nascosta. </p> <p>Se impostato su <span class="codeph"> -1</span> il componente non attiva mai il suo effetto di Nascondi automatico e rimane quindi sempre visibile sullo schermo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> durata</span></span> </p> </td> 
   <td colname="col2"> <p> Imposta la durata dell'animazione di dissolvenza in entrata/in uscita in secondi. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Proprietà {#section-1e637b22e8a44d759d588e47576891e6}

Facoltativo. Questo comando viene ignorato nei dispositivi touch in cui l&#39;opzione Nascondi automaticamente barra di controllo è disabilitata.

## Predefinito {#section-71fb773f814649b2885aefee68073641}

`fade,2,0.3`

## Esempio {#section-bce98c31f08a4a0ab262fab7f95ba020}

```
transition=none
```
