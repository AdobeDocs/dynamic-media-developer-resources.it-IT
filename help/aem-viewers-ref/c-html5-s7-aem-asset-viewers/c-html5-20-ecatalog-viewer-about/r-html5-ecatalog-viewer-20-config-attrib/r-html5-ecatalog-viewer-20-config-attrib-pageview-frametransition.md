---
title: PageView.frametransition
description: PageView.frametransition
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: 026c2fc5-0460-481c-aca9-ddd25371779c
source-git-commit: a919130f0940d81a221b79563b6b3e41533ba788
workflow-type: tm+mt
source-wordcount: '126'
ht-degree: 3%

---

# PageView.frametransition{#pageview-frametransition}

` [PageView.|<containerId>_pageView.]frametransition=slide|turn|auto[, *`durata`*]`

<table id="table_625D0EEDA21B46FEA3F5CF7DDF769B50"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> diapositiva|girare|auto</span> </p> </td> 
   <td colname="col2"> <p> Specifica il tipo di effetto applicato alla modifica del fotogramma. </p> <p> 
     <ul id="ul_4224B7C2722A4185A8BD48703D019AA1"> 
      <li id="li_8482037F8E1C4F11A84DF51790A073FE"> <p><span class="codeph"> diapositiva</span> attiva una transizione in cui la vecchia cornice scorre fuori dalla vista e la nuova cornice scivola nella vista. </p> </li> 
      <li id="li_CE9A99564DF348D0A76AB2A5945155A5"> <p><span class="codeph"> girare</span> attiva un effetto di inversione della pagina quando un utente può trascinare uno dei quattro angoli di visualizzazione ed eseguire un'operazione di capovolgimento della pagina interattiva. </p> <p>Quando <span class="codeph"> girare</span> viene utilizzato per controllare l’aspetto del componente con <span class="codeph"> pageturnstyle</span> modificatore e <span class="codeph"> .s7pagedivider</span> La classe CSS viene ignorata. </p> <p>Nota:  <p><span class="codeph"> girare</span> animazione non supportata in Motorola Xoom. </p> </p> </li> 
      <li id="li_79F85B0429CD4B389399FB3823FE767F"> <p> <span class="codeph"> auto</span> imposta la transizione del fotogramma di turno sui sistemi desktop e la transizione della diapositiva sui dispositivi touch. </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> durata</span></span> </p> </td> 
   <td colname="col2"> <p>Specifica la durata in secondi di un <span class="codeph"> diapositiva</span> o <span class="codeph"> girare</span> effetto di transizione. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Proprietà {#section-4d25a3f483834d2b9586fa70270ce6bd}

Facoltativo.

## Predefinito {#section-d677f04f1c894966884ce9d77a5ea1c1}

`slide,0.3`

## Esempio {#section-b877011e5f6240718e9451be8f622c02}

`frametransition=auto,1`
