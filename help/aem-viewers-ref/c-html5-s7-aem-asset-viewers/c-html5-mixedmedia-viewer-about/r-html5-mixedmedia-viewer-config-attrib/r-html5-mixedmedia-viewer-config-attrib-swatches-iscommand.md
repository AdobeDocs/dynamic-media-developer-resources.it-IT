---
title: Swatches.iscommand
description: Swatches.iscommand
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: 3336c4d2-0d1d-4c6f-8163-8a84a8be8c20
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '61'
ht-degree: 8%

---

# Swatches.iscommand{#swatches-iscommand}

` [Swatches.|<containerId>_swatches.]iscommand= *`isCommand`*`

<table id="table_43A84C1044574A6FAB8CE67D71AAD5EC"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> isCommand</span> </span> </p> </td> 
   <td colname="col2"> <p> Stringa di comando Image Server applicata a tutti i campioni. Se è specificato nell’URL, assicurati di codificare tutte le occorrenze di <span class="codeph"> &amp;</span> e <span class="codeph"> =</span> come <span class="codeph"> %26</span> e <span class="codeph"> %3D</span>, rispettivamente. </p> <p> <p>Nota: I comandi di manipolazione del dimensionamento delle immagini non sono supportati. </p> </p> </td> 
  </tr> 
 </tbody> 
</table>

## Proprietà {#section-65be9301796240e38f31818229da7acc}

Facoltativo.

## Predefinito {#section-bd374ffc5182484faa77a7a3c8fa70f2}

Nessuno.

## Esempio {#section-bd6c4249bccf44aab13fee8552f5a8b3}

Se specificato nell’URL del visualizzatore.

`iscommand=op_sharpen%3d1%26op_colorize%3d0xff0000`

Se specificato nei dati di configurazione.

`iscommand=op_sharpen=1&op_colorize=0xff0000`
