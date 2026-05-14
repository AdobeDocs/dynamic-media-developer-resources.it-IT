---
title: Campioni.iscommand
description: Campioni.iscommand
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: e375f3ec-82f3-441d-9e01-d0ea5605bd25
TQID: 'https://experienceleague.adobe.com/1ykmrNE-E7Gjb5jHKl82l8ULP3RJKC8QcHG2tDTPVEU'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 63
ht-degree: 4%

---

# Campioni.iscommand{#swatches-iscommand}

` [Swatches.|<containerId>_swatches.]iscommand= *`isCommand`*`

<table id="table_43A84C1044574A6FAB8CE67D71AAD5EC"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> isCommand</span> </span> </p> </td> 
   <td colname="col2"> <p> Stringa di comando Image Server applicata a tutti i campioni. Se è specificato nell'URL, assicurarsi di codificare tutte le occorrenze di <span class="codeph"> &amp;</span> e <span class="codeph"> =</span> come <span class="codeph"> %26</span> e <span class="codeph"> %3D</span>, rispettivamente. </p> <p> <p>Nota: i comandi di manipolazione del ridimensionamento delle immagini non sono supportati. </p> </p> </td> 
  </tr> 
 </tbody> 
</table>

## Proprietà {#section-1e637b22e8a44d759d588e47576891e6}

Facoltativo.

## Predefinito {#section-71fb773f814649b2885aefee68073641}

Nessuno.

## Esempio {#section-bce98c31f08a4a0ab262fab7f95ba020}

Se specificato nell’URL del visualizzatore.

`iscommand=op_sharpen%3d1%26op_colorize%3d0xff0000`

Se specificato nei dati di configurazione.

`iscommand=op_sharpen=1&op_colorize=0xff0000`
