---
title: Campioni.iscommand
description: Campioni.iscommand
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Flyout
role: Developer,User
exl-id: ed587082-3306-4914-916f-db37a823e199
TQID: 'https://experienceleague.adobe.com/e-WkYeq1Mtye5XR-fvOM-qdUx7u7NB6DQX9LHEf6aKo'
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

## Proprietà {#section-5526a5d19e7e4ee2a35b1c4816ed4202}

Facoltativo.

## Predefinito {#section-a08032f0fcf041c09e63c0238a339fc9}

Nessuno.

## Esempio {#section-0338be21edd04ff1a3bed5c8319b61a4}

Se specificato nell’URL del visualizzatore:

`iscommand=op_sharpen%3d1%26op_colorize%3d0xff0000`

Se specificato nei dati di configurazione:

`iscommand=op_sharpen=1&op_colorize=0xff0000`
