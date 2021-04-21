---
description: PageView.frametransition
solution: Experience Manager
title: PageView.frametransition
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '137'
ht-degree: 3%

---


# PageView.frametransition{#pageview-frametransition}

[!DNL ` [PageView.|<containerId>_pageView.]frametransition=slide|turn|auto[, *`durata`*]`]

<table id="table_625D0EEDA21B46FEA3F5CF7DDF769B50"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> diapositiva|girare|auto</span> </p> </td> 
   <td colname="col2"> <p> Specifica il tipo di effetto applicato alla modifica del fotogramma. </p> <p> 
     <ul id="ul_4224B7C2722A4185A8BD48703D019AA1"> 
      <li id="li_8482037F8E1C4F11A84DF51790A073FE"> <p><span class="codeph"> </span> consente di attivare una transizione in cui la vecchia cornice scorre fuori dalla vista e la nuova cornice scorre nella visualizzazione. </p> </li> 
      <li id="li_CE9A99564DF348D0A76AB2A5945155A5"> <p><span class="codeph"> </span> attiva l’effetto di capovolgimento della pagina quando un utente può trascinare uno dei quattro angoli di visualizzazione ed eseguire un capovolgimento interattivo della pagina. </p> <p>Quando si utilizza <span class="codeph"> volta</span>, l’aspetto del componente viene controllato con il modificatore <span class="codeph"> pageturnstyle</span> e la classe CSS <span class="codeph"> .s7pagedivider</span> viene ignorata. </p> <p>Nota:  <p><span class="codeph"> </span> l’animazione a turnino non è supportata in Motorola Xoom. </p> </p> </li> 
      <li id="li_79F85B0429CD4B389399FB3823FE767F"> <p> <span class="codeph"> </span> imposta automaticamente la transizione del fotogramma di turno sui sistemi desktop e la transizione della diapositiva sui dispositivi touch. </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> durata</span></span> </p> </td> 
   <td colname="col2"> <p>Specifica la durata in secondi di un effetto di transizione <span class="codeph"> slide</span> o <span class="codeph"> volta</span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Proprietà {#section-4d25a3f483834d2b9586fa70270ce6bd}

Facoltativo.

## Predefinito {#section-d677f04f1c894966884ce9d77a5ea1c1}

[!DNL `slide,0.3`]

## Esempio {#section-b877011e5f6240718e9451be8f622c02}

[!DNL `frametransition=auto,1`]
