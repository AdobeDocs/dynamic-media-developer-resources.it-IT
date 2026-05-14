---
title: FlyoutZoomView.frametransition
description: FlyoutZoomView.frametransition
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Flyout
role: Developer,User
exl-id: 0b0a88a0-d736-4ab8-a25f-15d1689b0a48
TQID: 'https://experienceleague.adobe.com/3LIVnhgzngZg4ETUaDgxZ66KeaognJp3SvkETJNSp9Q'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 63
ht-degree: 4%

---

# FlyoutZoomView.frametransition{#flyoutzoomview-frametransition}

` [FlyoutZoomView.|<containerId>_flyout.]frametransition=none|fade[, *`durata`*]`

<table id="table_FC34B37AACFB4E92A37E1D2D93D5F0D2"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> nessuno|dissolvenza</span> </p> </td> 
   <td colname="col2"> <p> Specifica il tipo di effetto applicato alla vista principale al cambiamento di risorsa. <span class="codeph"> none</span> rappresenta nessuna transizione; la modifica della visualizzazione principale avviene immediatamente. Dissolvenza <span class="codeph"></span> attiva la transizione di dissolvenza incrociata tra la scomparsa della prima immagine e la comparsa della nuova immagine </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Durata <span class="codeph"><span class="varname"></span></span> </p> </td> 
   <td colname="col2"> <p> Numero di secondi richiesti per il completamento dell'animazione. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Proprietà {#section-5526a5d19e7e4ee2a35b1c4816ed4202}

Facoltativo.

## Predefinito {#section-a08032f0fcf041c09e63c0238a339fc9}

Nessuno.

## Esempio {#section-0338be21edd04ff1a3bed5c8319b61a4}

`frametransition=fade,1`
