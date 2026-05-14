---
description: ControlBar.transition
solution: Experience Manager
title: ControlBar.transition
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: 2e08a62b-9499-41f8-927b-89bed972b4eb
TQID: 'https://experienceleague.adobe.com/bcpeaqLRZ8ClN2OulOfO9ujXzz44Yb2HTmy-GyPQ8mU'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 121
ht-degree: 2%

---

# ControlBar.transition{#controlbar-transition}

[!DNL ` [ControlBar.|<containerId>_controls.]transition=none|fade[, *`delaytohide`*[, *`durata`*]`]

<table id="table_F71AA834FE494949A2D4B569EA5E721F"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> nessuno|dissolvenza </span> </p> </td> 
   <td colname="col2"> <p> Specifica il tipo di effetto utilizzato per mostrare o nascondere la barra di controllo e il relativo contenuto. Utilizzare <span class="codeph"> none </span> per mostrare e nascondere subito; <span class="codeph"> fade </span> fornisce un effetto di dissolvenza graduale (non supportato in Internet Explorer 8). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> ritardatonascondere </span> </span> </p> </td> 
   <td colname="col2"> <p> Specifica il tempo in secondi che intercorre tra l'ultimo evento mouse/touch registrato dalla barra di controllo e il momento in cui la barra di controllo viene nascosta. </p> <p> Se è impostato su <span class="codeph"> -1 </span>, il componente non attiva mai l'effetto Nascondi automatico e resta sempre visibile sullo schermo. </p> </td> 
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
