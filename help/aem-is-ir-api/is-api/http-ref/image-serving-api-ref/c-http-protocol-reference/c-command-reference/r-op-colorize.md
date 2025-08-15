---
title: op_colorize
description: Colora immagine. Colora i dati dell'immagine conservandone le zone d'ombra e di luce.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 1abbde32-867a-4596-a46b-12ec50d59170
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '313'
ht-degree: 3%

---

# op_colorize{#op-colorize}

Colora immagine. Colora i dati dell&#39;immagine mantenendo ombre ed evidenziazioni.

` op_colorize= *`Contrasto colore`*[,off|norm[, *` `*]]`

<table id="simpletable_768D6CDF3F734E7F89DC7AB2EAAC0C77"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> Colore </span> </p> </td> 
  <td class="stentry"> <p>Sostituzione RGB colore. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> spento </span> </p> </td> 
  <td class="stentry"> <p>Disattiva la compensazione automatica della luminosità. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> norma </span> </p> </td> 
  <td class="stentry"> <p>Attiva compensazione automatica della luminosità (impostazione predefinita). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> contrasto </span> </p> </td> 
  <td class="stentry"> <p>Intervallo di contrasto (reale 0..100); impostare su 0 per mantenere il contrasto di input. </p> </td> 
 </tr> 
</table>

Il secondo argomento specifica se la luminosità dell&#39;immagine di origine deve essere regolata prima della colorizzazione. Specificare `off` per disattivare la compensazione automatica della luminosità oppure `norm` per regolare automaticamente la luminosità in modo che il valore mediano sia al 50% dell&#39;intensità.

Impostate il *`contrast`* valore su 0 per preservare l&#39;intervallo di contrasto dell&#39;immagine di input oppure specificate l&#39;intervallo di contrasto desiderato con un valore maggiore di 0. Il valore 100 offre il massimo contrasto. I valori tipici potrebbero essere compresi tra 30 e 70.

Oltre alle regolazioni integrate di luminosità e contrasto, `op_brightness=` e `op_contrast=` può essere utilizzato per mettere ulteriormente a punto l&#39;effetto di colorazione.

>[!NOTE]
>
>L&#39;algoritmo di colorazione utilizza solo le informazioni di luminanza nei dati dell&#39;immagine. Questa conversione in scala di grigi è semplice e non gestita dal colore. `op_colorize` Genera sempre RGB dati, lineare se l&#39;input è in scala di grigi o CMYK.

## Proprietà {#section-c0f8bd424b864153a1108f384939f55b}

Comando livello. Si applica al livello corrente o all&#39;immagine composita se `layer=comp`. Ignorato dai livelli degli effetti.

*`color`* deve essere un valore RGB; i valori grigi o CMYK *`color`* non sono supportati.

Il valore *`contrast`* viene ignorato se la compensazione della luminosità è disattivata.

Si presume che *`color`* sia presente nello spazio colore di lavoro corrispondente al tipo di pixel di *`color`*. *`color`* viene convertito con precisione se l&#39;immagine del livello ha un tipo di pixel diverso al momento dell&#39;unione.

CMYK immagini vengono convertite in RGB prima dell&#39;applicazione dell&#39;operazione.

## Predefinito {#section-0c3ea13efbac432c8970862d223e39b3}

`None`, senza colorazione. Il secondo e il terzo argomento vengono impostati automaticamente su `norm,0`, per una compensazione automatica della luminosità e nessuna modifica del contrasto.

## Esempio {#section-4c418d7b5e97409d9a448b8f08a1eab3}

Regolare dinamicamente la luminosità e il contrasto prima di colorare un livello di immagine:

... `&op_brightness=-15&op_contrast=22&op_colorize=a0b0c0&`…

Utilizza invece la regolazione automatica della luminosità e del contrasto:

... `&op_colorize=a0b0c0,norm,50&`...

## Consultate anche {#section-5581eb0e03014fa795e8f078c60e6c8d}

[colore](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md), [luminosità_op=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-brightness.md#reference-edf79dc41ae5411c80bec3ee3731c58a), [contrasto_op=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-contrast.md#reference-b26dfa9869fd43bebea0fbb8e9fe743d), [Gestione colore](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-color-management.md#reference-c7e4a72d589145189f7e4bcb6b4544d7)
