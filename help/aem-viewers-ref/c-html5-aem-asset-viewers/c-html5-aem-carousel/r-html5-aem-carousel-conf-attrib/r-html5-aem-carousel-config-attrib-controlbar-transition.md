---
description: Attributo di configurazione per il visualizzatore Carosello.
solution: Experience Manager
title: ControlBar.transition
feature: Dynamic Media Classic,Viewers,SDK/API,Carousel Banners
role: Developer,Business Practitioner
exl-id: 260a1767-e49a-46e3-9c3d-23efa5c3228e
translation-type: tm+mt
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '133'
ht-degree: 3%

---

# ControlBar.transition{#controlbar-transition}

Attributo di configurazione per il visualizzatore Carosello.

` [ControlBar.|<containerId>_controlBar.]transition=none|fade[, *``*[, *`delaytohideduration`*]`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|dissolvenza</span> </p> </td> 
   <td colname="col2"> <p> Specifica il tipo di effetto utilizzato per visualizzare o nascondere la barra di controllo e il relativo contenuto. </p> <p>Impostare su <span class="codeph"> none</span> per mostrare/nascondere istantaneamente. </p> <p>Impostare su <span class="codeph"> dissolvenza</span> per fornire un effetto graduale di dissolvenza in entrata/uscita. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> ritardare</span></span> </p> </td> 
   <td colname="col2"> <p> Specifica il tempo in secondi tra l’ultimo evento mouse/touch registrato dalla barra di controllo e la barra di controllo del tempo nascosto. </p> <p>Se è impostato su <span class="codeph"> -1</span>, il componente non attiva mai il suo effetto di visualizzazione automatica e quindi rimane sempre visibile sullo schermo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> durata</span></span> </p> </td> 
   <td colname="col2"> <p> Imposta la durata in secondi dell’animazione di dissolvenza in entrata/in uscita. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Proprietà {#section-1e637b22e8a44d759d588e47576891e6}

Facoltativo. Questo comando viene ignorato sui dispositivi touch in cui la barra di controllo mostra automaticamente è disabilitata.

## Predefinito {#section-71fb773f814649b2885aefee68073641}

`fade,2,0.3`

## Esempio {#section-bce98c31f08a4a0ab262fab7f95ba020}

```
transition=none
```
