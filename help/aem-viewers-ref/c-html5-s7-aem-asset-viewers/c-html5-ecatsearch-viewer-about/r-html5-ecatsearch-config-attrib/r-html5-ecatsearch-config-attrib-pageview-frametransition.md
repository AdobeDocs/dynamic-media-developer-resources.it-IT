---
description: PageView.frametransition
solution: Experience Manager
title: PageView.frametransition
topic: Dynamic media
uuid: 12595a89-bad5-4224-aeff-52ce6bb615ee
translation-type: tm+mt
source-git-commit: bf5873e5a6bdb859e19b15584ba85e9c106f853b
workflow-type: tm+mt
source-wordcount: '126'
ht-degree: 3%

---


# PageView.frametransition{#pageview-frametransition}

[!DNL ` [PageView.|<containerId>_pageView.]frametransition=slide|turn|auto[, *`length`*]`]

<table id="table_625D0EEDA21B46FEA3F5CF7DDF769B50"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> diapositiva|volta|auto</span> </p> </td> 
   <td colname="col2"> <p> Specifica il tipo di effetto applicato alla modifica del fotogramma. </p> <p> 
     <ul id="ul_4224B7C2722A4185A8BD48703D019AA1"> 
      <li id="li_8482037F8E1C4F11A84DF51790A073FE"> <p><span class="codeph"> Consente di </span> attivare una transizione in cui la vecchia cornice scorre fuori dalla vista e la nuova cornice scorre per visualizzarla. </p> </li> 
      <li id="li_CE9A99564DF348D0A76AB2A5945155A5"> <p><span class="codeph"> Attiva </span> un effetto di riflessione della pagina, quando un utente può trascinare uno dei quattro angoli di visualizzazione ed eseguire un Capovolgimento interattivo della pagina. </p> <p>Quando si utilizza <span class="codeph"> Turn</span>, l'aspetto del componente viene controllato con il modificatore <span class="codeph"> pageturnstyle</span> e la classe CSS <span class="codeph"> .s7pagedivider</span> viene ignorata. </p> <p>Nota:  <p><span class="codeph"> L'</span> animazione di tornitura non è supportata in Motorola Xoom. </p> </p> </li> 
      <li id="li_79F85B0429CD4B389399FB3823FE767F"> <p> <span class="codeph"> Consente di </span> impostare automaticamente la transizione del frame di attivazione sui sistemi desktop e la transizione della diapositiva sui dispositivi touch. </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> length</span></span> </p> </td> 
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
