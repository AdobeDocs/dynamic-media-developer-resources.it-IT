---
description: Le macro di comando forniscono collegamenti denominati per set di comandi.
solution: Experience Manager
title: Macro di comando
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '258'
ht-degree: 0%

---


# Macro di comando{#command-macros}

Le macro di comando forniscono collegamenti denominati per set di comandi.

Le macro sono definite in file di definizione macro separati, che possono essere allegati ai cataloghi di immagini o al catalogo predefinito.

Le macro possono essere richiamate in qualsiasi punto di una richiesta dopo &#39;?&#39;, nonché in qualsiasi punto all&#39;interno di un campo `catalog::Modifier`. Le macro possono rappresentare solo uno o più comandi Image Serving completi, pertanto devono essere racchiusi tra i separatori &#39;&amp;&#39; (tranne quando all&#39;inizio o alla fine della stringa del modificatore).

Le chiamate macro vengono sostituite dalle relative stringhe di sostituzione all&#39;inizio dell&#39;analisi. I comandi all’interno delle macro sostituiranno gli stessi comandi nella richiesta se si verificano prima della chiamata della macro nella richiesta. Questo è diverso da `catalog::Modifier`, dove i comandi nella stringa di richiesta sovrascrivono sempre i comandi nella stringa `catalog::Modifier`, indipendentemente dalla posizione nella richiesta.

Le macro possono essere nidificate con le seguenti limitazioni: è possibile richiamare una macro solo se è già definita al momento dell&#39;analisi della definizione della macro, visualizzandola in precedenza nello stesso file di definizione della macro oppure inserendo la definizione di tale macro incorporata nel file di definizione della macro predefinita.

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

Poiché `wid=` è diverso per la terza richiesta, sovrascriviamo semplicemente il valore *dopo* la macro viene richiamata (specificare `wid=`*prima* `$view$` non avrebbe alcun effetto).

+ [name](r-name.md)
