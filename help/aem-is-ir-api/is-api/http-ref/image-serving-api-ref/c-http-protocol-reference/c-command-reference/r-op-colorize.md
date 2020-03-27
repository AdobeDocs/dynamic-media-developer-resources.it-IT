---
description: Colorare l’immagine. Colora i dati dell’immagine preservando le ombre e le luci.
seo-description: Colorare l’immagine. Colora i dati dell’immagine preservando le ombre e le luci.
seo-title: op_colorize
solution: Experience Manager
title: op_colorize
topic: Scene7 Image Serving - Image Rendering API
uuid: e74a85ca-73bf-4c69-ac77-768a58b33d0b
translation-type: tm+mt
source-git-commit: 94a26628ec619076f0942e9278165cc591f1c150

---


# op_colorize{#op-colorize}

Colorare l’immagine. Colora i dati dell’immagine preservando le ombre e le luci.

` op_colorize= *`contrasto di`*[,off|norm[, *`colore`*]]`

<table id="simpletable_768D6CDF3F734E7F89DC7AB2EAAC0C77"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> color </span> </p> </td> 
  <td class="stentry"> <p>Colore RGB sostitutivo. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> off </span> </p> </td> 
  <td class="stentry"> <p>Disattivate la compensazione automatica della luminosità. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> norma </span> </p> </td> 
  <td class="stentry"> <p>Abilita compensazione automatica della luminosità (impostazione predefinita). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> contrasto </span> </p> </td> 
  <td class="stentry"> <p>Intervallo di contrasto (0,100 reale); impostato su 0 per mantenere il contrasto di input. </p> </td> 
 </tr> 
</table>

Il secondo argomento specifica se regolare la luminosità dell’immagine sorgente prima di colorare. Specificate `off` di disattivare la compensazione automatica della luminosità o `norm` di regolare automaticamente la luminosità in modo che il valore medio sia del 50% di intensità.

Set the *`contrast`* value to 0 to preserve the contrast range of the input image, or specify a desired contrast range with a value greater than 0. Il valore 100 offre il massimo contrasto. I valori tipici potrebbero essere compresi tra 30 e 70.

Oltre alle regolazioni integrate di luminosità e contrasto, `op_brightness=` possono essere utilizzati `op_contrast=` per perfezionare ulteriormente l&#39;effetto di colorazione.

>[!NOTE]
>
>L’algoritmo di colorizzazione utilizza solo le informazioni sulla luminanza nei dati immagine. Questa conversione in scala di grigio è semplice e non è gestita tramite il colore. `op_colorize` produce sempre dati RGB, anche se l&#39;input è in scala di grigio o CMYK.

## Proprietà {#section-c0f8bd424b864153a1108f384939f55b}

Livello, comando. Si applica al livello corrente o all’immagine composita, se `layer=comp`. Ignorato dai livelli degli effetti.

*`color`* deve essere un valore RGB; i valori di grigio o CMYK *`color`* non sono supportati.

Il *`contrast`* valore viene ignorato se la compensazione della luminosità è disattivata.

*`color`* si presume che esista nello spazio colore di lavoro corrispondente al tipo di pixel di *`color`*. *`color`* viene convertita accuratamente se l’immagine del livello ha un diverso tipo di pixel al momento dell’unione.

Le immagini CMYK vengono convertite in RGB prima dell’applicazione dell’operazione.

## Predefinito {#section-0c3ea13efbac432c8970862d223e39b3}

`None`, senza colorizzazione. Il secondo e il terzo argomento vengono impostati come predefiniti `norm,0`, per la compensazione automatica della luminosità e per nessun cambiamento di contrasto.

## Esempio {#section-4c418d7b5e97409d9a448b8f08a1eab3}

Regolare la luminosità e il contrasto in modo dinamico prima di colorare un livello immagine:

… `&op_brightness=-15&op_contrast=22&op_colorize=a0b0c0&`…

Utilizzate invece la regolazione automatica della luminosità e del contrasto:

… `&op_colorize=a0b0c0,norm,50&`…

## Consultate anche {#section-5581eb0e03014fa795e8f078c60e6c8d}

[color](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md), [op_bright=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-brightness.md#reference-edf79dc41ae5411c80bec3ee3731c58a), [op_Contrasto=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-contrast.md#reference-b26dfa9869fd43bebea0fbb8e9fe743d), Gestione [del colore](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-color-management.md#reference-c7e4a72d589145189f7e4bcb6b4544d7)
