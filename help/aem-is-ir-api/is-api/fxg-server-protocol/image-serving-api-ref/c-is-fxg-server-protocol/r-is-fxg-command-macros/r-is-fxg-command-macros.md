---
description: Le macro di comandi forniscono collegamenti denominati per set di comandi.
seo-description: Le macro di comandi forniscono collegamenti denominati per set di comandi.
seo-title: Macro di comandi
solution: Experience Manager
title: Macro di comandi
topic: Scene7 Image Serving - Image Rendering API
uuid: f90d5132-aa5b-424f-a123-838723ed891a
translation-type: tm+mt
source-git-commit: 4169757880407b62addd0a70ef1807d8b195820b

---


# Macro di comandi{#command-macros}

Le macro di comandi forniscono collegamenti denominati per set di comandi.

Le macro sono definite in file di definizione delle macro separati, che possono essere allegati ai cataloghi di immagini o al catalogo predefinito.

Le macro possono essere invocate in qualsiasi punto di una richiesta dopo &#39;?&#39;, nonché ovunque all&#39;interno di un `catalog::Modifier` campo. Le macro possono rappresentare solo uno o più comandi Image Server completi, pertanto devono essere racchiusi tra separatori &#39;&amp;&#39; (tranne quando all&#39;inizio o alla fine della stringa del modificatore).

Le chiamate delle macro vengono sostituite dalle relative stringhe di sostituzione nelle prime fasi dell&#39;analisi. I comandi all&#39;interno delle macro sostituiscono gli stessi comandi nella richiesta se si verificano prima della chiamata alla macro nella richiesta. Questo è diverso da `catalog::Modifier`, dove i comandi nella stringa di richiesta sostituiranno sempre i comandi nella `catalog::Modifier` stringa, indipendentemente dalla posizione nella richiesta.

Le macro possono essere nidificate, con le seguenti limitazioni: una macro può essere invocata solo se è già definita al momento dell&#39;analisi della definizione della macro, apparendo in precedenza nello stesso file di definizione della macro oppure inserendo la definizione di tale macro incorporata nel file di definizione della macro predefinita.

Le macro possono essere utili se gli stessi attributi devono essere applicati a immagini diverse.

[!DNL http://server/cat/1345?wid=240&fmt=pdf&imageRes=300]

[!DNL http://server/cat/1435?wid=240&fmt=pdf&imageRes=300]

[!DNL http://server/cat/8243?wid=480&fmt=pdf&imageRes=300]

È possibile definire una macro per gli attributi comuni:

`view wid=240&fmt=pdf&imageRes=300`

La macro viene utilizzata come segue:

[!DNL http://server/cat/1345?$view$]

[!DNL http://server/cat/1435?$view$]

[!DNL http://server/cat/8243?$view$&wid=480]

Poiché `wid=` è diverso per la terza richiesta, è sufficiente sostituire il valore *dopo* che la macro viene chiamata (specificando `wid=`*prima *`$view$`non avrebbe alcun effetto).

+ [name](r-name.md)
