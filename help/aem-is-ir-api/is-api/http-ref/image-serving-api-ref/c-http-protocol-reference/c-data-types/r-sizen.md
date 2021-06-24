---
description: Dimensione normalizzata. Utilizzato per specificare le dimensioni dell'immagine o del rettangolo, normalizzato rispetto alle dimensioni del livello 0 o di un'altra immagine.
solution: Experience Manager
title: sizeN
feature: Dynamic Media Classic, SDK/API
role: Developer,Business Practitioner
exl-id: 58c2d7da-31fc-49d1-a404-2e4a66ff0e56
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '92'
ht-degree: 0%

---

# sizeN{#sizen}

Dimensione normalizzata. Utilizzato per specificare le dimensioni dell&#39;immagine o del rettangolo, normalizzato rispetto alle dimensioni del livello 0 o di un&#39;altra immagine.

<table id="simpletable_BB36205775D4447084E527E2630D28B9"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> sizeN</span> </span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> nx</span> </span>,  <span class="codeph"><span class="varname"> ny</span></span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> nx</span> </span>,  <span class="codeph"><span class="varname"> ny</span></span> </p></td> 
  <td class="stentry"> <p>larghezza e altezza normalizzate relative a un'altra immagine (reale, reale, maggiore di 0) </p></td> 
 </tr> 
</table>

Sia *nx* che *ny* devono essere maggiori di 0. 0,0 può indicare che è necessario utilizzare una dimensione predefinita specifica. 1,1 specifica una dimensione uguale all&#39;immagine di riferimento.
