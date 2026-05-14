---
title: interactivedata
description: Comando URL per Visualizzatore video interattivo.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: f9f5aa7a-3e0a-434a-8623-b439c9b6f18b
TQID: 'https://experienceleague.adobe.com/xIjjnZZX0Y7wce2TJwN2R228elxxysj0qXB2WELq9xc'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 98
ht-degree: 3%

---

# interactivedata{#interactivedata}

Comando URL per Visualizzatore video interattivo.

`interactivedata= *`file`*`

I dati interattivi associano determinate aree temporali nel contenuto video ai dati del prodotto che vengono successivamente visualizzati in campioni interattivi accanto al video. È anche associato al pannello call-to-action mostrato alla fine della riproduzione video. Inoltre, fornisce un titolo per il video interattivo visualizzato nel pannello call-to-action.

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> file</span> </span> </p> </td> 
   <td colname="col2"> <p> Specifica un URL o un percorso per il contenuto di dati interattivi WebVTT. Il file WebVTT deve essere gestito da Image Server. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Proprietà {#section-f42369774e2740dcb399626a0e4e930e}

Facoltativo.

## Predefinito {#section-d016470e92a74f98a18c4ab3489410a5}

Nessuno.

## Esempio {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

```
interactivedata=is/content/content/dam/mac/aodmarketingna/_VTT/dm-viewers-content/video/Glacier.mp4.svideo.vtt
```
