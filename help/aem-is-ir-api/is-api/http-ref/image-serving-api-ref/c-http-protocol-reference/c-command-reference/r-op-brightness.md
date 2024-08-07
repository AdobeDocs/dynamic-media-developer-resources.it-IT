---
title: op_brightness
description: Regola la luminosità. Riduce o aumenta la luminosità dell'immagine.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 390ed812-87ae-41e7-8021-65dd95915ae8
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '75'
ht-degree: 2%

---

# op_brightness{#op-brightness}

Regola la luminosità. Riduce o aumenta la luminosità dell&#39;immagine.

`op_brightness= *`adj`*`

<table id="simpletable_2B5DB95B1FF044C8BD226D4F8311E806"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> adj</span> </p> </td> 
  <td class="stentry"> <p>Regolazione della luminosità (-100...+100 int). </p></td> 
 </tr> 
</table>

## Proprietà {#section-c7e757f63b2c4b5ebaacbadb51c72ce4}

Comando Livello. Si applica al livello corrente o all&#39;immagine composita se `layer=comp`. Ignorato dai livelli degli effetti. Le immagini o i livelli CMYK vengono convertiti in RGB prima dell&#39;applicazione dell&#39;operazione.

## Predefinito {#section-be56be0759634c79b4f264f194a94dbc}

`op_brightness=0`, senza alcuna modifica della luminosità.

## Esempio {#section-c25f952f1b77409abb9ccf885862d75c}

Scurisce leggermente lo sfondo di un’immagine per enfatizzare il contenuto in primo piano:

`http://server/myRootId/myImageId?wid=500&layer=0&maskUse=invert&op_brightness=-10&layer=1&src=myRootId/myImageId`
