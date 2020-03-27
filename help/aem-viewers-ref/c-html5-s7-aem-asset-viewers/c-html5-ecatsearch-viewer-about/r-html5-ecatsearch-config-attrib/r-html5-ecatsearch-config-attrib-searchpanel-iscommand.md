---
description: 'null'
seo-description: 'null'
seo-title: SearchPanel.iscommand
solution: Experience Manager
title: SearchPanel.iscommand
topic: Dynamic media
uuid: 7496fea1-8a69-4749-ab4b-ae6d375441b8
translation-type: tm+mt
source-git-commit: 2bd5b17e473ec53844b4bbcb4f13580b2d6bfaf4

---


# SearchPanel.iscommand{#searchpanel-iscommand}

[!DNL `[SearchPanel.|<containerId>_searchPanel.]iscommand= *`isCommand`*`]

<table id="table_9E7BB12BF371419F88DD4D24EF04632C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> isCommand</span></span> </p> </td> 
   <td colname="col2"> <p> Stringa di comando Image Server applicata a tutte le miniature. Se specificate nell’URL, tutte le occorrenze di <span class="codeph"> &amp;</span> e <span class="codeph"> =</span> devono essere codificate rispettivamente in HTTP come <span class="codeph"> %26</span> e <span class="codeph"> %3D</span>. </p> </td> 
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
