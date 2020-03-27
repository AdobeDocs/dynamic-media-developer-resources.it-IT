---
description: Le macro di comandi forniscono collegamenti denominati per set di comandi.
seo-description: Le macro di comandi forniscono collegamenti denominati per set di comandi.
seo-title: Macro di comandi *
solution: Experience Manager
title: Macro di comandi *
topic: Scene7 Image Serving - Image Rendering API
uuid: 0a131488-6296-4c7f-9bc7-3053df908899
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef

---


# Macro di comandi *{#command-macros}

Le macro di comandi forniscono collegamenti denominati per set di comandi.

`$ *[!DNL name]*$`

** *[!DNL name]* ** Nome macro

Le macro sono definite in file di definizione delle macro separati, che possono essere allegati ai cataloghi dei materiali o al catalogo predefinito.

*[!DNL name]* non fa distinzione tra maiuscole e minuscole e può essere costituita da qualsiasi combinazione di lettere ASCII, numeri, &#39;-&#39;, &#39;_&#39; e &#39;.&#39; caratteri.

Richiamare le macro in un punto qualsiasi di una richiesta dopo &#39;?&#39; o in un punto qualsiasi all&#39;interno di un `vignette::Modifier` campo. Le macro possono rappresentare solo uno o più comandi di rendering immagini completi e devono essere separate da altri comandi con separatori &#39;&amp;&#39;.

Le chiamate delle macro vengono sostituite dalle relative stringhe di sostituzione nelle prime fasi dell&#39;analisi. I comandi all&#39;interno delle macro sostituiscono gli stessi comandi nella richiesta se si verificano prima della chiamata alla macro nella richiesta. Questo è diverso da `vignette::Modifier`, dove i comandi nella stringa di richiesta sostituiranno sempre i comandi nella `vignette::Modifier` stringa, indipendentemente dalla posizione nella richiesta.

Le macro dei comandi non possono avere valori di argomento, ma è possibile utilizzare variabili personalizzate per trasmettere valori dalla richiesta alla macro.

Le macro potrebbero non essere nidificate.

**Esempio**

Le macro possono essere utili se gli stessi comandi o attributi devono essere applicati a diverse immagini sottoposte a rendering.

`http://server/ir/render/cat/vig0?fmt=jpeg&qlt=80&sharpen=1&src=cat/matA&res=40 http://server/ir/render/cat/vig1?fmt=jpeg&qlt=80&sharpen=1&src=cat/matB&res=40 http://server/ir/render/cat/vig2?fmt=jpeg&qlt=95&sharpen=1&src=cat/matC&res=40`

È possibile definire una macro per gli attributi comuni:

`render vignette=cat/$vig$&fmt=jpg&qlt=80&sharpen=1&src=cat/$mat$&res=40`

La macro viene utilizzata come segue:

`http://server/ir/render/cat/vig0?$mat=matc&$render$ http://server/ir/render/cat/vig0?$mat=matc&$render$ http://server/ir/render/cat/vig0?$mat=matc&$render$&qlt=95`

Poiché `qlt=` è diverso per la terza richiesta, è sufficiente sostituire il valore dopo che la macro viene chiamata (specificando `qlt=`*prima *non`$render$`avrebbe alcun effetto).

**Consultate anche**

`catalog::MacroFile`, `catalog::Modifier`Riferimento Definizione Macro

<!--<a id="section_297B7FCB285F4891AA76DF8393089931"></a>-->

