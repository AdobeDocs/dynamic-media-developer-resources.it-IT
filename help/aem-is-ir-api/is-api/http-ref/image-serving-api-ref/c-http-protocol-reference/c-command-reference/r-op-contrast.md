---
title: op_contrast
description: Regola il contrasto. Regola il contrasto dell'immagine aumentando la luminosità dei pixel con una luminosità superiore al 50% e riducendo la luminosità dei pixel con una luminosità inferiore al 50%.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 0216f22e-a3b3-4dda-89c2-9c6c2c81cab3
TQID: 'https://experienceleague.adobe.com/Ob098G38TFXX0HzB3JQOCcdD9ZnrYWrMum6XEQSmGRU'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 143
ht-degree: 1%

---

# op_contrast{#op-contrast}

Regola il contrasto. Regola il contrasto dell&#39;immagine aumentando la luminosità dei pixel con una luminosità superiore al 50% e riducendo la luminosità dei pixel con una luminosità inferiore al 50%.

`op_contrast= *`adj`*`

<table id="simpletable_8246802C74424A68A7A2EA5B50A89D42"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> adj</span> </p> </td> 
  <td class="stentry"> <p>Regolazione del contrasto in percentuale (-100...100 int). </p></td> 
 </tr> 
</table>

## Proprietà {#section-d319ed55057344eab0a3c93f720acdbf}

Comando Livello. Si applica al livello corrente o all&#39;immagine composita se `layer=comp`. Ignorato dai livelli degli effetti.

## Predefinito {#section-896d1b1f7f084e929355a4684f3e833b}

`op_contrast=0`, senza alcuna modifica al contrario. Le immagini o i livelli CMYK vengono convertiti in RGB prima dell&#39;applicazione dell&#39;operazione.

## Esempio {#section-94bc4348b4bc4f0e9768ea1c45ca8340}

Diminuisci il contrasto e la nitidezza di un livello di immagine di qualità superiore per abbinarlo visivamente a una foto di sfondo di bassa qualità:

... `&op_blur=3&op_contrast=-12&`

Una versione futura potrebbe utilizzare la luminosità mediana dell&#39;immagine invece di una luminosità fissa del 50%.
