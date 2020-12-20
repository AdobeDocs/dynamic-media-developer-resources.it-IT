---
description: Dimensione normalizzata. Viene usato per specificare le dimensioni dell’immagine o del rettangolo, normalizzato rispetto alle dimensioni del livello 0 o di un’altra immagine.
seo-description: Dimensione normalizzata. Viene usato per specificare le dimensioni dell’immagine o del rettangolo, normalizzato rispetto alle dimensioni del livello 0 o di un’altra immagine.
seo-title: sizeN
solution: Experience Manager
title: sizeN
topic: Scene7 Image Serving - Image Rendering API
uuid: 6fc05654-6f0d-499f-97bc-6b7134024e1f
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '109'
ht-degree: 0%

---


# sizeN{#sizen}

Dimensione normalizzata. Viene usato per specificare le dimensioni dell’immagine o del rettangolo, normalizzato rispetto alle dimensioni del livello 0 o di un’altra immagine.

<table id="simpletable_BB36205775D4447084E527E2630D28B9"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> sizeN</span> </span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> nx</span> </span>,  <span class="codeph"><span class="varname"> ny</span></span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> nx</span> </span>,  <span class="codeph"><span class="varname"> ny</span></span> </p></td> 
  <td class="stentry"> <p>larghezza e altezza normalizzate relative a un’altra immagine (reale, reale, maggiore di 0) </p></td> 
 </tr> 
</table>

Sia *nx* che *ny* devono essere maggiori di 0. 0,0 può indicare che deve essere utilizzata una specifica dimensione predefinita. 1,1 specifica una dimensione uguale all’immagine di riferimento.
