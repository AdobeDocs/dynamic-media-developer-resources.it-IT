---
description: Le macro di comando forniscono collegamenti denominati per set di comandi.
solution: Experience Manager
title: Macro di comando *
feature: Dynamic Media Classic, SDK/API
role: Sviluppatore, Business Practices
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '244'
ht-degree: 1%

---


# Macro di comando *{#command-macros}

Le macro di comando forniscono collegamenti denominati per set di comandi.

`$ *[!DNL name]*$`

** *[!DNL name]* ** Nome macro

Le macro sono definite in file di definizione macro separati, che possono essere allegati ai cataloghi di materiali o al catalogo predefinito.

*[!DNL name]* non distingue tra maiuscole e minuscole e può essere costituito da qualsiasi combinazione di lettere ASCII, numeri, &#39;-&#39;, &#39;_&#39; e &#39;.&#39; caratteri.

Richiama le macro in qualsiasi punto di una richiesta dopo &#39;?&#39; o in qualsiasi punto all&#39;interno di un campo `vignette::Modifier`. Le macro possono rappresentare solo uno o più comandi Image Rendering completi e devono essere separate da altri comandi con i separatori &#39;&amp;&#39;.

Le chiamate macro vengono sostituite dalle relative stringhe di sostituzione all&#39;inizio dell&#39;analisi. I comandi all’interno delle macro sostituiscono gli stessi comandi nella richiesta se si verificano prima della chiamata della macro nella richiesta. Questo è diverso da `vignette::Modifier`, dove i comandi nella stringa di richiesta sovrascrivono sempre i comandi nella stringa `vignette::Modifier`, indipendentemente dalla posizione nella richiesta.

Le macro dei comandi non possono avere valori di argomento, ma è possibile utilizzare variabili personalizzate per passare i valori dalla richiesta alla macro.

Le macro potrebbero non essere nidificate.

**Esempio**

Le macro possono essere utili se gli stessi comandi o attributi devono essere applicati a diverse immagini sottoposte a rendering.

`http://server/ir/render/cat/vig0?fmt=jpeg&qlt=80&sharpen=1&src=cat/matA&res=40 http://server/ir/render/cat/vig1?fmt=jpeg&qlt=80&sharpen=1&src=cat/matB&res=40 http://server/ir/render/cat/vig2?fmt=jpeg&qlt=95&sharpen=1&src=cat/matC&res=40`

È possibile definire una macro per gli attributi comuni:

`render vignette=cat/$vig$&fmt=jpg&qlt=80&sharpen=1&src=cat/$mat$&res=40`

La macro viene utilizzata come segue:

`http://server/ir/render/cat/vig0?$mat=matc&$render$ http://server/ir/render/cat/vig0?$mat=matc&$render$ http://server/ir/render/cat/vig0?$mat=matc&$render$&qlt=95`

Poiché `qlt=` è diverso per la terza richiesta, sovrascriviamo semplicemente il valore dopo la chiamata della macro (specificare `qlt=`*prima* `$render$`non avrebbe alcun effetto).

**Consultate anche**

`catalog::MacroFile`,  `catalog::Modifier`, Riferimento alla definizione delle macro

<!--<a id="section_297B7FCB285F4891AA76DF8393089931"></a>-->

