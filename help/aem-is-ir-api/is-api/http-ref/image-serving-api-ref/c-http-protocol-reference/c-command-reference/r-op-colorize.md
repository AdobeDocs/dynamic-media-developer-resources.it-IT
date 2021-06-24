---
description: Colorare l'immagine. Colora i dati dell'immagine mantenendo le ombre e le luci.
solution: Experience Manager
title: op_colorize
feature: Dynamic Media Classic, SDK/API
role: Developer,Business Practitioner
exl-id: 1abbde32-867a-4596-a46b-12ec50d59170
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '313'
ht-degree: 3%

---

# op_colorize{#op-colorize}

Colorare l&#39;immagine. Colora i dati dell&#39;immagine mantenendo le ombre e le luci.

` op_colorize= *``*[,off|norm[, *`contrasto di colore`*]]`

<table id="simpletable_768D6CDF3F734E7F89DC7AB2EAAC0C77"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> color </span> </p> </td> 
  <td class="stentry"> <p>Colore RGB sostitutivo. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> off  </span> </p> </td> 
  <td class="stentry"> <p>Disattiva la compensazione automatica della luminosità. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> norma  </span> </p> </td> 
  <td class="stentry"> <p>Abilita compensazione automatica della luminosità (impostazione predefinita). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> contrasto  </span> </p> </td> 
  <td class="stentry"> <p>Intervallo di contrasto (reale 0.100); impostato su 0 per mantenere il contrasto di ingresso. </p> </td> 
 </tr> 
</table>

Il secondo argomento specifica se la luminosità dell&#39;immagine sorgente deve essere regolata prima della colorazione. Specificare `off` per disattivare la compensazione automatica della luminosità o `norm` per regolare automaticamente la luminosità in modo che il valore medio sia a un&#39;intensità del 50%.

Imposta il valore *`contrast`* su 0 per mantenere l&#39;intervallo di contrasto dell&#39;immagine di input o specifica un intervallo di contrasto desiderato con un valore maggiore di 0. Il valore 100 offre il massimo contrasto. I valori tipici potrebbero essere compresi tra 30 e 70.

Oltre alle regolazioni integrate di luminosità e contrasto, è possibile utilizzare `op_brightness=` e `op_contrast=` per perfezionare ulteriormente l&#39;effetto di colorazione.

>[!NOTE]
>
>L’algoritmo di colorazione utilizza solo le informazioni sulla luminanza nei dati dell’immagine. Questa conversione in scala di grigi è semplice e non è gestita tramite colori. `op_colorize` emette sempre i dati RGB, anche se l’input è in scala di grigi o CMYK.

## Proprietà {#section-c0f8bd424b864153a1108f384939f55b}

Livello, comando. Si applica al livello corrente o all&#39;immagine composita se `layer=comp`. Ignorato dai livelli di effetto.

*`color`* deve essere un valore RGB; I  *`color`* valori grigio o CMYK non sono supportati.

Il valore *`contrast`* viene ignorato se la compensazione della luminosità è disattivata.

*`color`* si presume che esista nello spazio colore di lavoro corrispondente al tipo di pixel di  *`color`*. *`color`* viene convertito accuratamente se l&#39;immagine di livello ha un tipo di pixel diverso al momento dell&#39;unione.

Le immagini CMYK vengono convertite in RGB prima dell’applicazione dell’operazione.

## Predefinito {#section-0c3ea13efbac432c8970862d223e39b3}

`None`, senza colorizzazione. Il secondo e il terzo argomento sono predefiniti in `norm,0`, per la compensazione automatica della luminosità e senza modifiche del contrasto.

## Esempio {#section-4c418d7b5e97409d9a448b8f08a1eab3}

Regolare dinamicamente luminosità e contrasto prima di colorare un livello immagine:

... `&op_brightness=-15&op_contrast=22&op_colorize=a0b0c0&`...

Utilizza invece la regolazione automatica della luminosità e del contrasto:

... `&op_colorize=a0b0c0,norm,50&`...

## Consultate anche {#section-5581eb0e03014fa795e8f078c60e6c8d}

[colore](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md),  [op_bright=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-brightness.md#reference-edf79dc41ae5411c80bec3ee3731c58a),  [op_contrasto=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-contrast.md#reference-b26dfa9869fd43bebea0fbb8e9fe743d), gestione  [del colore](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-color-management.md#reference-c7e4a72d589145189f7e4bcb6b4544d7)
