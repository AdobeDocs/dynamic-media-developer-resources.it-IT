---
description: ControlBar.transition
solution: Experience Manager
title: ControlBar.transition
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: 2e08a62b-9499-41f8-927b-89bed972b4eb
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '118'
ht-degree: 2%

---

# ControlBar.transition{#controlbar-transition}

[!DNL ` [ControlBar.|<containerId>_controls.]transition=none|fade[, *`delaytohide`*[, *`durata`*]`]

<table id="table_F71AA834FE494949A2D4B569EA5E721F"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|dissolvenza </span> </p> </td> 
   <td colname="col2"> <p> Specifica il tipo di effetto utilizzato per mostrare o nascondere la barra di controllo e il relativo contenuto. Utilizzare <span class="codeph"> nessuno </span> per mostrare e nascondere istantaneamente; <span class="codeph"> dissolvenza </span> fornisce un effetto di dissolvenza graduale in entrata e in uscita (non supportato in Internet Explorer 8). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> delaytohide </span> </span> </p> </td> 
   <td colname="col2"> <p> Specifica il tempo in secondi che intercorre tra l'ultimo evento mouse/touch registrato dalla barra di controllo e il momento in cui la barra di controllo viene nascosta. </p> <p> Se impostato su <span class="codeph"> -1 </span> il componente non attiva mai il suo effetto di Nascondi automatico e resta sempre visibile sullo schermo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> durata </span> </span> </p> </td> 
   <td colname="col2"> <p> Imposta la durata dell'animazione di dissolvenza in entrata e in uscita, in secondi. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Proprietà {#section-f42369774e2740dcb399626a0e4e930e}

Facoltativo. Questo comando viene ignorato nei dispositivi touch, in cui l&#39;opzione Nascondi automaticamente barra di controllo è disattivata.

## Predefinito {#section-d016470e92a74f98a18c4ab3489410a5}

[!DNL `fade,2,0.5`]

## Esempio {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

[!DNL `transition=none`]
