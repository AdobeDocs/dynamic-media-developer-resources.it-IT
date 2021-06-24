---
description: SearchPanel.iscommand
solution: Experience Manager
title: SearchPanel.iscommand
feature: Dynamic Media Classic,Visualizzatori,SDK/API,Ricerca eCatalog
role: Developer,Business Practitioner
exl-id: 4e843866-75a5-4543-a275-e134b3aee75a
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '57'
ht-degree: 8%

---

# SearchPanel.iscommand{#searchpanel-iscommand}

[!DNL `[SearchPanel.|<containerId>_searchPanel.]iscommand= *`isCommand`*`]

<table id="table_9E7BB12BF371419F88DD4D24EF04632C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> isCommand</span></span> </p> </td> 
   <td colname="col2"> <p> Stringa di comando Image Server applicata a tutte le miniature. Se specificato nell'URL, tutte le occorrenze di <span class="codeph"> &amp;</span> e <span class="codeph"> =</span> devono essere codificate per HTTP rispettivamente come <span class="codeph"> %26</span> e <span class="codeph"> %3D</span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Proprietà {#section-df5a0604766b4ac2b9a6742b377e427c}

Facoltativo.

## Predefinito {#section-9f2bf4c418e5441c9fff3eb755f7bda6}

Nessuno.

## Esempio {#section-813de2905d6c44c0991cfe0931581462}

Se specificato nell’URL del visualizzatore.

[!DNL `iscommand=op_sharpen%3d1%26op_colorize%3d0xff0000`]

Se specificato nei dati di configurazione.

[!DNL `iscommand=op_sharpen=1&op_colorize=0xff0000`]
