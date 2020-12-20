---
description: Attributo di configurazione per il visualizzatore video interattivo.
seo-description: Attributo di configurazione per il visualizzatore video interattivo.
seo-title: ControlBar.transition
solution: Experience Manager
title: ControlBar.transition
topic: Dynamic media
uuid: cde4a5b9-4512-41a6-84ce-9f4fc2cc0399
translation-type: tm+mt
source-git-commit: 16838d04b005224fad6df215ab5bf8c25ef86fc7
workflow-type: tm+mt
source-wordcount: '122'
ht-degree: 3%

---


# ControlBar.transition{#controlbar-transition}

Attributo di configurazione per il visualizzatore video interattivo.

` [ControlBar.|<containerId>_controls.]transition=none|fade[, *``*[, *`delaytohidedurata`*]`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|dissolvenza</span> </p> </td> 
   <td colname="col2"> <p> Specifica il tipo di effetto da utilizzare per mostrare o nascondere la barra di controllo e il relativo contenuto. </p> <p>Impostate su <span class="codeph"> none</span> per la visualizzazione istantanea/nascondere. </p> <p>Impostare su <span class="codeph"> dissolvenza</span> per ottenere un effetto di dissolvenza graduale in entrata/uscita. Non supportato in Internet Explorer 8. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> delaytohide</span></span> </p> </td> 
   <td colname="col2"> <p> Specifica il tempo in secondi tra l’ultimo evento mouse/tocco registrato dalla barra di controllo e la barra di controllo del tempo nascosto. Se è impostato su <span class="codeph"> -1</span>, il componente non attiva mai il suo effetto di disattivazione automatica e, pertanto, rimane sempre visibile sullo schermo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> length</span></span> </p> </td> 
   <td colname="col2"> <p> Imposta la durata dell'animazione di dissolvenza in entrata/uscita, in secondi. </p> </td> 
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

