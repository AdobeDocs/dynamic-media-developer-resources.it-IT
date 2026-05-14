---
title: SpinView.iconeffect
description: SpinView.iconeffect
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: 473207d2-7e26-4ea3-940e-5a21f29a2b91
TQID: 'https://experienceleague.adobe.com/hZb5SQHHzH8zeR7UoxOp2Oc-MTWvvmGvsvc7mzsP40k'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 120
ht-degree: 4%

---

# SpinView.iconeffect{#spinview-iconeffect}

` [SpinView.|<containerId>_spinView.]iconeffect=0|1[, *`conteggio`*][, *`dissolvenza`*][, *`autoHide`*]`

<table id="table_DF2137DF9C7441B381D2B03CEE4B880A"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0|1</span> </p> </td> 
   <td colname="col2"> <p> Consente la visualizzazione dell'effetto iconeffect <span class="codeph"></span> nella parte superiore dell'immagine quando quest'ultima è in stato di reimpostazione e suggerisce un'azione disponibile per interagire con l'immagine. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> conteggio</span></span> </p> </td> 
   <td colname="col2"> <p> Specifica il numero massimo di volte che l'iconeffect <span class="codeph"></span> viene visualizzato e rivisualizzato. Il valore <span class="codeph"> -1</span> indica che l'icona viene sempre visualizzata indefinitamente. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Dissolvenza <span class="codeph"><span class="varname"></span></span> </p> </td> 
   <td colname="col2"> <p>Specifica la durata dell'animazione mostra/nascondi, in secondi. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> Nascondi automaticamente</span></span> </p> </td> 
   <td colname="col2"> <p>Imposta il numero di secondi in cui l'effetto iconeffect</span> di <span class="codeph"> rimane completamente visibile prima che venga nascosto automaticamente. Ossia, il tempo dopo il completamento dell'animazione di dissolvenza in entrata, ma prima dell'inizio dell'animazione di dissolvenza in uscita. L'impostazione <span class="codeph"> 0</span> disattiva il comportamento Nascondi automatico. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Proprietà {#section-65be9301796240e38f31818229da7acc}

Facoltativo.

## Predefinito {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`1,1,0.3,3`

## Esempio {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`iconeffect=0`
