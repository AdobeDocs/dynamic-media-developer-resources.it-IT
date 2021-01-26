---
description: Le macro di comandi forniscono collegamenti denominati per set di comandi. Le macro sono definite in file di definizione delle macro separati, che possono essere allegati ai cataloghi di immagini o al catalogo predefinito.
seo-description: Le macro di comandi forniscono collegamenti denominati per set di comandi. Le macro sono definite in file di definizione delle macro separati, che possono essere allegati ai cataloghi di immagini o al catalogo predefinito.
seo-title: Macro di comandi
solution: Experience Manager
title: Macro di comandi
topic: Dynamic Media Image Serving - Image Rendering API
uuid: a6ff5642-6716-484f-b37e-066994362a9b
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '342'
ht-degree: 1%

---


# Macro comandi{#command-macros}

Le macro di comandi forniscono collegamenti denominati per set di comandi. Le macro sono definite in file di definizione delle macro separati, che possono essere allegati ai cataloghi di immagini o al catalogo predefinito.

`$ *`name`*$`

<table id="simpletable_A03541622C354F60B5F304B999C4EF8E"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> name</span></span> </p> </td> 
  <td class="stentry"> <p>Nome della macro. </p></td> 
 </tr> 
</table>

`*`Il `*` nome non fa distinzione tra maiuscole e minuscole e può essere composto da qualsiasi combinazione di lettere ASCII, numeri, &#39;-&#39;, &#39;_&#39; e &#39;.&#39; caratteri.

Le macro possono essere invocate in qualsiasi punto di una richiesta dopo &#39;?&#39;, nonché ovunque all&#39;interno di un campo `catalog::Modifier` o `catalog::PostModifier`. Le macro possono rappresentare solo uno o più comandi Image Server completi e devono essere separate da altri comandi con separatori &#39;&amp;&#39;.

Le chiamate delle macro vengono sostituite dalle relative stringhe di sostituzione nelle prime fasi dell&#39;analisi. I comandi all&#39;interno delle macro sostituiscono gli stessi comandi nella richiesta se si verificano prima della chiamata alla macro nella richiesta. Questo è diverso da `catalog::Modifier`, dove i comandi nella stringa di richiesta sostituiranno sempre i comandi nella stringa `catalog::Modifier`, indipendentemente dalla posizione nella richiesta.

Le macro dei comandi non possono avere valori di argomento, ma è possibile utilizzare variabili personalizzate per trasmettere valori dalla richiesta alla macro.

Le macro possono essere nidificate, con le seguenti limitazioni: È possibile richiamare una macro solo se è già definita al momento dell&#39;analisi della definizione della macro, visualizzandola in precedenza nello stesso file di definizione della macro oppure inserendo la definizione di tale macro incorporata nel file di definizione della macro predefinita.

## Esempio {#section-2f73d36ac8d64254a03bae5afeae2fb9}

Le macro possono essere utili se gli stessi attributi devono essere applicati a immagini diverse.

`http://server/cat/1345?wid=240&fmt=jpeg&qlt=85&op_usm=5,2&bgc=200,200,200&align=-1,-1 http://server/cat/1435?wid=240&fmt=jpeg&qlt=85&op_usm=5,2&bgc=200,200,200&align=-1,-1 http://server/cat/8243?wid=480&fmt=jpeg&qlt=85&op_usm=5,2&bgc=200,200,200&align=-1,-1`

È possibile definire una macro per gli attributi comuni:

`view wid=240&fmt=jpeg&qlt=85&op_usm=5,2&bgc=200,200,200&align=-1,-1`

La macro viene utilizzata come segue:

`http://server/cat/1345?$view$ http://server/cat/1435?$view$ http://server/cat/8243?$view$&wid=480`

Poiché `wid=` è diverso per la terza richiesta, è sufficiente sostituire il valore *dopo* che la macro viene richiamata (specificando `wid=`*before* `$view$` non avrebbe alcun effetto).

## Consultate anche {#section-8cdba0ed2480444ca61e719e54f8871c}

[catalogo::MacroFile](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-macrofile.md#reference-f91d717b3847458ca0f1fe95387554a2) ,  [catalogo::Modificatore](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-modifier-cat.md), Riferimento definizione  [macro](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-macro-definition-reference/c-macro-definition-reference.md#concept-5ec73f7636c1496fba1e94094e694e79)
