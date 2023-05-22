---
description: Colora immagine. Colora i dati dell'immagine mantenendo ombre ed evidenziazioni.
solution: Experience Manager
title: op_colorize
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 1abbde32-867a-4596-a46b-12ec50d59170
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '308'
ht-degree: 3%

---

# op_colorize{#op-colorize}

Colora immagine. Colora i dati dell&#39;immagine mantenendo ombre ed evidenziazioni.

` op_colorize= *`colore`*[,off|norm[, *`contrasto`*]]`

<table id="simpletable_768D6CDF3F734E7F89DC7AB2EAAC0C77"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> color </span> </p> </td> 
  <td class="stentry"> <p>Sostituisce il colore RGB. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> disattivato </span> </p> </td> 
  <td class="stentry"> <p>Disattiva la compensazione automatica della luminosità. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> norma </span> </p> </td> 
  <td class="stentry"> <p>Abilita compensazione automatica della luminosità (impostazione predefinita). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> contrasto </span> </p> </td> 
  <td class="stentry"> <p>Intervallo di contrasto (reale 0..100); impostare su 0 per mantenere il contrasto di input. </p> </td> 
 </tr> 
</table>

Il secondo argomento specifica se la luminosità dell&#39;immagine di origine deve essere regolata prima della colorizzazione. Specifica `off` per disattivare la compensazione automatica della luminosità o `norm` per regolare automaticamente la luminosità in modo che il valore mediano sia all&#39;intensità del 50%.

Imposta il *`contrast`* impostate il valore su 0 per mantenere l&#39;intervallo di contrasto dell&#39;immagine di input oppure specificate un intervallo di contrasto desiderato con un valore maggiore di 0. Il valore 100 offre il massimo contrasto. I valori tipici possono essere compresi tra 30 e 70.

Oltre alle regolazioni integrate di luminosità e contrasto, `op_brightness=` e `op_contrast=` può essere utilizzato per mettere ulteriormente a punto l’effetto colorante.

>[!NOTE]
>
>L&#39;algoritmo di colorizzazione utilizza solo le informazioni sulla luminanza nei dati immagine. La conversione in scala di grigi è semplice e non consente la gestione dei colori. `op_colorize` produce sempre dati RGB, anche se l&#39;input è in scala di grigi o CMYK.

## Proprietà {#section-c0f8bd424b864153a1108f384939f55b}

Comando Livello. Si applica al livello corrente o all&#39;immagine composita se `layer=comp`. Ignorato dai livelli degli effetti.

*`color`* deve essere un valore RGB; grigio o CMYK *`color`* valori non supportati.

Il *`contrast`* il valore viene ignorato se la compensazione della luminosità è disattivata.

*`color`* si presume che esista nello spazio colore di lavoro corrispondente al tipo di pixel di *`color`*. *`color`* viene convertita con precisione se l&#39;immagine del livello ha un tipo di pixel diverso al momento dell&#39;unione.

Le immagini CMYK vengono convertite in RGB prima dell&#39;applicazione dell&#39;operazione.

## Predefinito {#section-0c3ea13efbac432c8970862d223e39b3}

`None`, senza colorizzazione. Il secondo e il terzo argomento vengono impostati per impostazione predefinita su `norm,0`, per la compensazione automatica della luminosità e nessun cambiamento del contrasto.

## Esempio {#section-4c418d7b5e97409d9a448b8f08a1eab3}

Regolare dinamicamente luminosità e contrasto prima di colorare un livello immagine:

… `&op_brightness=-15&op_contrast=22&op_colorize=a0b0c0&`…

Utilizza invece la regolazione automatica della luminosità e del contrasto:

… `&op_colorize=a0b0c0,norm,50&`…

## Consultate anche {#section-5581eb0e03014fa795e8f078c60e6c8d}

[colore](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md), [op_brightness=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-brightness.md#reference-edf79dc41ae5411c80bec3ee3731c58a), [op_contrast=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-contrast.md#reference-b26dfa9869fd43bebea0fbb8e9fe743d), [Gestione colore](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-color-management.md#reference-c7e4a72d589145189f7e4bcb6b4544d7)
