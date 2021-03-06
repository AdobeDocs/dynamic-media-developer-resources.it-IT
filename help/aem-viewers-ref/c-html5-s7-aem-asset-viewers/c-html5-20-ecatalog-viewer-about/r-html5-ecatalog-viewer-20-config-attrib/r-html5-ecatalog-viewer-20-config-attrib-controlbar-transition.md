---
title: ControlBar.transition
description: Specifica il tipo di effetto utilizzato per visualizzare o nascondere la barra di controllo e il relativo contenuto.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: abe8affb-cbcd-4072-b2ed-91a398b1d678
source-git-commit: edc127dc6e2ae2d9bd5feed08c8bc896c8c39747
workflow-type: tm+mt
source-wordcount: '136'
ht-degree: 2%

---

# ControlBar.transition{#controlbar-transition}

` [ControlBar.|<containerId>_controls.]transition=none|fade[, *`ritardare`*[, *`durata`*]`

<table id="table_F71AA834FE494949A2D4B569EA5E721F"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|dissolvenza </span> </p> </td> 
   <td colname="col2"> <p> Specifica il tipo di effetto utilizzato per visualizzare o nascondere la barra di controllo e il relativo contenuto. Utilizzo <span class="codeph"> nessuno </span> per mostrare e nascondere istantaneamente; <span class="codeph"> dissolvenza </span> fornisce un effetto di dissolvenza in entrata e in uscita graduale (non supportato in Internet Explorer 8). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> ritardare </span> </span> </p> </td> 
   <td colname="col2"> <p> Specifica il tempo in secondi tra l'ultimo evento mouse/touch registrato dalla barra di controllo e l'eliminazione della barra di controllo del tempo. </p> <p> Se impostato su <span class="codeph"> -1 </span>, il componente non attiva mai il suo effetto di visualizzazione automatica e rimane sempre visibile sullo schermo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> durata </span> </span> </p> </td> 
   <td colname="col2"> <p> Imposta la durata in secondi dell'animazione di dissolvenza in entrata e in uscita. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Proprietà {#section-f42369774e2740dcb399626a0e4e930e}

Facoltativo. Questo comando viene ignorato sui dispositivi touch, in cui la barra di controllo di nascondere automaticamente è disabilitata.

## Predefinito {#section-d016470e92a74f98a18c4ab3489410a5}

`fade,2,0.5`

## Esempio {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

`transition=none`
