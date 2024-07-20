---
title: PageView.frametransition
description: PageView.frametransition
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: 026c2fc5-0460-481c-aca9-ddd25371779c
source-git-commit: a919130f0940d81a221b79563b6b3e41533ba788
workflow-type: tm+mt
source-wordcount: '125'
ht-degree: 2%

---

# PageView.frametransition{#pageview-frametransition}

` [PageView.|<containerId>_pageView.]frametransition=slide|turn|auto[, *`durata`*]`

<table id="table_625D0EEDA21B46FEA3F5CF7DDF769B50"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> diapositiva|turn|auto</span> </p> </td> 
   <td colname="col2"> <p> Specifica il tipo di effetto applicato al cambio di fotogramma. </p> <p> 
     <ul id="ul_4224B7C2722A4185A8BD48703D019AA1"> 
      <li id="li_8482037F8E1C4F11A84DF51790A073FE"> <p>La diapositiva <span class="codeph"></span> attiva una transizione in cui il vecchio frame scorre fuori visualizzazione e il nuovo frame scorre in visualizzazione. </p> </li> 
      <li id="li_CE9A99564DF348D0A76AB2A5945155A5"> <p><span class="codeph"> turno</span> abilita un effetto di capovolgimento pagina, quando un utente può trascinare uno dei quattro angoli di pagine affiancate ed eseguire un capovolgimento pagina interattivo. </p> <p>Quando si utilizza il <span class="codeph"> turno</span>, l'aspetto del componente è controllato dal modificatore <span class="codeph"> pageturnstyle</span> e la classe CSS <span class="codeph"> .s7pagedivider</span> viene ignorata. </p> <p>Nota:  <p>Animazione <span class="codeph"> turn</span> non supportata in Motorola Xoom. </p> </p> </li> 
      <li id="li_79F85B0429CD4B389399FB3823FE767F"> <p> <span class="codeph"> auto</span> imposta la transizione del fotogramma di svolta sui sistemi desktop e la transizione di scorrimento sui dispositivi touch. </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Durata <span class="codeph"><span class="varname"></span></span> </p> </td> 
   <td colname="col2"> <p>Specifica la durata in secondi di un effetto di transizione <span class="codeph"> diapositiva</span> o <span class="codeph"> turno</span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Proprietà {#section-4d25a3f483834d2b9586fa70270ce6bd}

Facoltativo.

## Predefinito {#section-d677f04f1c894966884ce9d77a5ea1c1}

`slide,0.3`

## Esempio {#section-b877011e5f6240718e9451be8f622c02}

`frametransition=auto,1`
