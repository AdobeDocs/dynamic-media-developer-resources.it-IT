---
description: 'null'
seo-description: 'null'
seo-title: ControlBar.Transition
solution: Experience Manager
title: ControlBar.Transition
topic: Dynamic media
uuid: 30f133bd-09c7-4d70-bcc4-d961bb028e55
translation-type: tm+mt
source-git-commit: 2bd5b17e473ec53844b4bbcb4f13580b2d6bfaf4

---


# ControlBar.Transition{#controlbar-transition}

[!DNL ` [ControlBar.|<containerId>_controls.]transition=none|fade[, *``*[, *`delaytohidedurata`*]`]

<table id="table_F71AA834FE494949A2D4B569EA5E721F"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|dissolvenza </span> </p> </td> 
   <td colname="col2"> <p> Specifica il tipo di effetto utilizzato per mostrare o nascondere la barra di controllo e il relativo contenuto. Utilizzate <span class="codeph"> none </span> per la visualizzazione istantanea e il nascondimento; La <span class="codeph"> dissolvenza </span> fornisce un effetto di dissolvenza graduale in entrata e in uscita (non supportato in Internet Explorer 8). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> ritardo </span></span> </p> </td> 
   <td colname="col2"> <p> Specifica il tempo in secondi tra l'ultimo evento mouse/tocco registrato dalla barra di controllo e quello nascosto dalla barra di controllo tempo. </p> <p> Se è impostato su <span class="codeph"> -1, </span> il componente non attiva mai il suo effetto di disattivazione automatica e resta sempre visibile sullo schermo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> durata </span></span> </p> </td> 
   <td colname="col2"> <p> Imposta la durata dell'animazione di dissolvenza in entrata e in uscita, in secondi. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Proprietà {#section-f42369774e2740dcb399626a0e4e930e}

Facoltativo. Questo comando viene ignorato sui dispositivi touch, dove la barra di controllo si nasconde automaticamente.

## Predefinito {#section-d016470e92a74f98a18c4ab3489410a5}

[!DNL `fade,2,0.5`]

## Esempio {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

[!DNL `transition=none`]
