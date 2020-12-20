---
description: Regolare la luminosità. Riduce o aumenta la luminosità dell’immagine.
seo-description: Regolare la luminosità. Riduce o aumenta la luminosità dell’immagine.
seo-title: op_bright
solution: Experience Manager
title: op_bright
topic: Scene7 Image Serving - Image Rendering API
uuid: 751ec9e5-4a70-438d-950c-deff4db034b1
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '85'
ht-degree: 3%

---


# op_bright{#op-brightness}

Regolare la luminosità. Riduce o aumenta la luminosità dell’immagine.

`op_brightness= *`adj`*`

<table id="simpletable_2B5DB95B1FF044C8BD226D4F8311E806"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> adj</span> </p> </td> 
  <td class="stentry"> <p>Regolazione della luminosità (-100...+100 int). </p></td> 
 </tr> 
</table>

## Proprietà {#section-c7e757f63b2c4b5ebaacbadb51c72ce4}

Livello, comando. Si applica al livello corrente o all&#39;immagine composita se `layer=comp`. Ignorato dai livelli degli effetti. Le immagini o i livelli CMYK vengono convertiti in RGB prima dell’applicazione dell’operazione.

## Predefinito {#section-be56be0759634c79b4f264f194a94dbc}

`op_brightness=0`, per non modificare la luminosità.

## Esempio {#section-c25f952f1b77409abb9ccf885862d75c}

Scurisci leggermente lo sfondo di un’immagine per evidenziare il contenuto in primo piano:

`http://server/myRootId/myImageId?wid=500&layer=0&maskUse=invert&op_brightness=-10&layer=1&src=myRootId/myImageId`
