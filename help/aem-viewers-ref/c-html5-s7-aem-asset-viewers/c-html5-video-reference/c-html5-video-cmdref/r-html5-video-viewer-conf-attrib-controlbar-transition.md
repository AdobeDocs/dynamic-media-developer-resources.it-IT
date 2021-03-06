---
title: ControlBar.transition
description: Attributo di configurazione per il visualizzatore video.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Video
role: Developer,User
exl-id: 133717c7-38d9-47b6-86bb-e23ebd8f147a
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '119'
ht-degree: 3%

---

# ControlBar.transition{#controlbar-transition}

Attributo di configurazione per il visualizzatore video.

` [ControlBar.|<containerId>_controls.]transition=none|fade[, *`ritardare`*[, *`durata`*]`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|dissolvenza</span> </p> </td> 
   <td colname="col2"> <p> Specifica il tipo di effetto utilizzato per visualizzare o nascondere la barra di controllo e il relativo contenuto. </p> <p>Utilizzo <span class="codeph"> nessuno</span> per mostrare e nascondere istantanei. Utilizzo <span class="codeph"> dissolvenza</span> per fornire un effetto graduale di dissolvenza in entrata e in uscita. </p> <p>La dissolvenza non è supportata in Internet Explorer 8. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> ritardare</span> </span> </p> </td> 
   <td colname="col2"> <p>Specifica il tempo in secondi tra l'ultimo evento mouse/touch registrato dalla barra di controllo e il tempo nascosto dalla barra di controllo. </p> <p> Se impostato su <span class="codeph"> -1</span>, il componente non attiva mai il suo effetto di visualizzazione automatica e rimane sempre visibile sullo schermo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> durata</span> </span> </p> </td> 
   <td colname="col2"> <p>Imposta la durata in secondi dell'animazione di dissolvenza in entrata e in uscita. </p> </td> 
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
