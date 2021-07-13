---
description: Attributo di configurazione per il visualizzatore Video360.
solution: Experience Manager
title: ControlBar.transition
feature: Dynamic Media Classic,Visualizzatori,SDK/API,Video VR 360
role: Developer,User
exl-id: 950b1230-5c4b-4222-87e2-d069287fc3ff
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '125'
ht-degree: 3%

---

# ControlBar.transition{#controlbar-transition}

Attributo di configurazione per il visualizzatore Video360.

` [ControlBar.|<containerId>_controls.]transition=none|fade[, *``*[, *`delaytohideduration`*]`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|dissolvenza</span> </p> </td> 
   <td colname="col2"> <p> Specifica il tipo di effetto utilizzato per visualizzare o nascondere la barra di controllo e il relativo contenuto. </p> <p>Utilizza <span class="codeph"> none</span> per visualizzare e nascondere istantaneamente. Utilizza <span class="codeph"> dissolvenza</span> per fornire un effetto graduale di dissolvenza in entrata e in uscita. </p> <p>La dissolvenza non è supportata in Internet Explorer 8. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> ritardare</span> </span> </p> </td> 
   <td colname="col2"> <p>Specifica il tempo in secondi tra l'ultimo evento mouse/touch registrato dalla barra di controllo e la barra di controllo del tempo nascosta. </p> <p> Se è impostato su <span class="codeph"> -1</span> il componente non attiva mai il suo effetto di visualizzazione automatica e rimane sempre visibile sullo schermo. </p> </td> 
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
