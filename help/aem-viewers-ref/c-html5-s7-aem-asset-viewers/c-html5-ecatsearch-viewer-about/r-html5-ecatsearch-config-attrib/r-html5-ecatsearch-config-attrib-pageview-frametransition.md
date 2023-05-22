---
description: PageView.frametransition
solution: Experience Manager
title: PageView.frametransition
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: 19239fa8-65a8-487f-9370-42bb93d862d5
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '126'
ht-degree: 3%

---

# PageView.frametransition{#pageview-frametransition}

[!DNL ` [PageView.|<containerId>_pageView.]frametransition=slide|turn|auto[, *`durata`*]`]

<table id="table_625D0EEDA21B46FEA3F5CF7DDF769B50"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> slide|turn|auto</span> </p> </td> 
   <td colname="col2"> <p> Specifica il tipo di effetto applicato al cambio di fotogramma. </p> <p> 
     <ul id="ul_4224B7C2722A4185A8BD48703D019AA1"> 
      <li id="li_8482037F8E1C4F11A84DF51790A073FE"> <p><span class="codeph"> diapositiva</span> attiva una transizione in cui il vecchio fotogramma scorre in modalità non visibile e il nuovo fotogramma scorre in modalità di visualizzazione. </p> </li> 
      <li id="li_CE9A99564DF348D0A76AB2A5945155A5"> <p><span class="codeph"> girare</span> attiva un effetto di capovolgimento pagina, quando l'utente può trascinare uno dei quattro angoli di visualizzazione ed eseguire un capovolgimento interattivo della pagina. </p> <p>Quando <span class="codeph"> girare</span> viene utilizzato l'aspetto del componente viene controllato con <span class="codeph"> pageturnstyle</span> e <span class="codeph"> .s7pagedivider</span> Classe CSS ignorata. </p> <p>Nota:  <p><span class="codeph"> girare</span> animazione non supportata in Motorola Xoom. </p> </p> </li> 
      <li id="li_79F85B0429CD4B389399FB3823FE767F"> <p> <span class="codeph"> auto</span> imposta la transizione del fotogramma di tornitura sui sistemi desktop e la transizione di scorrimento sui dispositivi touch. </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> durata</span></span> </p> </td> 
   <td colname="col2"> <p>Specifica la durata in secondi di una <span class="codeph"> diapositiva</span> o <span class="codeph"> girare</span> effetto di transizione. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Proprietà {#section-4d25a3f483834d2b9586fa70270ce6bd}

Facoltativo.

## Predefinito {#section-d677f04f1c894966884ce9d77a5ea1c1}

[!DNL `slide,0.3`]

## Esempio {#section-b877011e5f6240718e9451be8f622c02}

[!DNL `frametransition=auto,1`]
