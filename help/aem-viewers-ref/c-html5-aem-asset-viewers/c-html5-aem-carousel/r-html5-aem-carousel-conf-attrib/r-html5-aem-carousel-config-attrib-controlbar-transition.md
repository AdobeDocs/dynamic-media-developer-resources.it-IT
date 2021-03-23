---
description: Attributo di configurazione per il visualizzatore Carosello.
seo-description: Attributo di configurazione per il visualizzatore Carosello.
seo-title: ControlBar.transition
solution: Experience Manager
title: ControlBar.transition
uuid: 80053511-f0e2-49f6-a1db-cd96c7788703
feature: Dynamic Media Classic,Visualizzatori,SDK/API,Banner carosello
role: Sviluppatore, Business Practices
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '139'
ht-degree: 2%

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

