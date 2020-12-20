---
description: Attributo di configurazione per il visualizzatore Video360.
seo-description: Attributo di configurazione per il visualizzatore Video360.
seo-title: ControlBar.transition
solution: Experience Manager
title: ControlBar.transition
topic: Dynamic media
uuid: e8c1da96-3533-4d31-9ad3-569a87948ac6
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '123'
ht-degree: 3%

---


# ControlBar.transition{#controlbar-transition}

Attributo di configurazione per il visualizzatore Video360.

` [ControlBar.|<containerId>_controls.]transition=none|fade[, *``*[, *`delaytohidedurata`*]`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|dissolvenza</span> </p> </td> 
   <td colname="col2"> <p> Specifica il tipo di effetto utilizzato per mostrare o nascondere la barra di controllo e il relativo contenuto. </p> <p>Utilizzate <span class="codeph"> none</span> per visualizzare e nascondere all'istante. Utilizzate <span class="codeph"> dissolvenza</span> per ottenere un effetto di dissolvenza graduale in entrata e in uscita. </p> <p>La dissolvenza non è supportata in Internet Explorer 8. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> delaytohide</span> </span> </p> </td> 
   <td colname="col2"> <p>Specifica il tempo in secondi tra l'ultimo evento mouse/tocco registrato dalla barra di controllo e quello nascosto dalla barra di controllo tempo. </p> <p> Se è impostato su <span class="codeph"> -1</span>, il componente non attiva mai il suo effetto di disattivazione automatica e rimane sempre visibile sullo schermo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> length</span> </span> </p> </td> 
   <td colname="col2"> <p>Imposta la durata dell'animazione di dissolvenza in entrata e in uscita, in secondi. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Proprietà {#section-f42369774e2740dcb399626a0e4e930e}

Facoltativo.

## Predefinito {#section-d016470e92a74f98a18c4ab3489410a5}

`fade,2,0.5`

## Esempio {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

```
transition=none
```

