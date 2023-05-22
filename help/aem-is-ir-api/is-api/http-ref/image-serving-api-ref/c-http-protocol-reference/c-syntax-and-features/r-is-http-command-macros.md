---
description: Le macro dei comandi forniscono scelte rapide denominate per insiemi di comandi. Le macro vengono definite in file di definizione delle macro separati, che possono essere allegati ai cataloghi di immagini o al catalogo predefinito.
solution: Experience Manager
title: Macro dei comandi
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 304d93af-3427-4111-882a-35be9ec3aef5
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '312'
ht-degree: 0%

---

# Macro dei comandi{#command-macros}

Le macro dei comandi forniscono scelte rapide denominate per insiemi di comandi. Le macro vengono definite in file di definizione delle macro separati, che possono essere allegati ai cataloghi di immagini o al catalogo predefinito.

`$ *`nome`*$`

<table id="simpletable_A03541622C354F60B5F304B999C4EF8E"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> nome</span></span> </p> </td> 
  <td class="stentry"> <p>Nome macro. </p></td> 
 </tr> 
</table>

`*`nome`*` non fa distinzione tra maiuscole e minuscole e può essere costituito da qualsiasi combinazione di lettere ASCII, numeri, &quot;-&quot;, &quot;_&quot; e &quot;.&quot; caratteri.

Le macro possono essere richiamate in qualsiasi punto di una richiesta dopo il segno &quot;?&quot;, nonché in qualsiasi punto di una `catalog::Modifier` o `catalog::PostModifier` campo. Le macro possono rappresentare solo uno o più comandi Image Server completi e devono essere separate da altri comandi con separatori &#39;&amp;&#39;.

Le chiamate macro vengono sostituite dalle relative stringhe di sostituzione nelle prime fasi dell&#39;analisi. I comandi all&#39;interno delle macro sostituiscono gli stessi comandi nella richiesta se si verificano prima della chiamata della macro nella richiesta. Questo è diverso da `catalog::Modifier`, in cui i comandi nella stringa di richiesta sovrascriveranno sempre i comandi nella `catalog::Modifier` stringa, indipendentemente dalla posizione nella richiesta.

Le macro di comando non possono avere valori di argomento, ma è possibile utilizzare variabili personalizzate per passare i valori dalla richiesta alla macro.

Le macro possono essere nidificate, con la seguente restrizione: Una macro può essere richiamata solo se è già definita al momento dell&#39;analisi della definizione della macro, visualizzandola in precedenza nello stesso file di definizione della macro oppure inserendo la definizione di tale macro incorporata nel file di definizione della macro predefinito.

## Esempio {#section-2f73d36ac8d64254a03bae5afeae2fb9}

Le macro possono essere utili se gli stessi attributi devono essere applicati a immagini diverse.

`http://server/cat/1345?wid=240&fmt=jpeg&qlt=85&op_usm=5,2&bgc=200,200,200&align=-1,-1 http://server/cat/1435?wid=240&fmt=jpeg&qlt=85&op_usm=5,2&bgc=200,200,200&align=-1,-1 http://server/cat/8243?wid=480&fmt=jpeg&qlt=85&op_usm=5,2&bgc=200,200,200&align=-1,-1`

È possibile definire una macro per gli attributi comuni:

`view wid=240&fmt=jpeg&qlt=85&op_usm=5,2&bgc=200,200,200&align=-1,-1`

La macro viene utilizzata nel modo seguente:

`http://server/cat/1345?$view$ http://server/cat/1435?$view$ http://server/cat/8243?$view$&wid=480`

Da `wid=` è diverso per la terza richiesta, il valore viene semplicemente ignorato *dopo* la macro viene richiamata (specificando `wid=`*prima di* `$view$` non avrebbe alcun effetto).

## Consultate anche {#section-8cdba0ed2480444ca61e719e54f8871c}

[catalog::FileMacro](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-macrofile.md#reference-f91d717b3847458ca0f1fe95387554a2) , [catalogo::Modificatore](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-modifier-cat.md), [Riferimento definizione macro](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-macro-definition-reference/c-macro-definition-reference.md#concept-5ec73f7636c1496fba1e94094e694e79)
