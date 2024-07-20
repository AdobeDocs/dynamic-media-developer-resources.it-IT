---
title: Macro dei comandi
description: Le macro dei comandi forniscono scelte rapide denominate per insiemi di comandi.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: dc149977-3ca8-4612-ad05-4d565440d00a
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '248'
ht-degree: 0%

---

# Macro dei comandi{#command-macros}

Le macro dei comandi forniscono scelte rapide denominate per insiemi di comandi.

Le macro vengono definite in file di definizione delle macro separati, che possono essere allegati ai cataloghi di immagini o al catalogo predefinito.

Le macro possono essere richiamate in qualsiasi punto di una richiesta dopo &#39;?&#39; e in qualsiasi punto di un campo `catalog::Modifier`. Le macro possono rappresentare solo uno o più comandi Image Server completi, pertanto devono essere racchiuse tra separatori &#39;&amp;&#39;, tranne quando si trova all&#39;inizio o alla fine della stringa del modificatore.

Le chiamate macro vengono sostituite dalle relative stringhe di sostituzione nelle prime fasi dell&#39;analisi. I comandi all&#39;interno delle macro ignorano gli stessi comandi nella richiesta se si verificano prima della chiamata della macro nella richiesta. Questo flusso è diverso da `catalog::Modifier`, dove i comandi nella stringa di richiesta sovrascrivono sempre i comandi nella stringa `catalog::Modifier`, indipendentemente dalla posizione nella richiesta.

È possibile nidificare le macro. È tuttavia possibile richiamare una macro solo se è già definita al momento dell&#39;analisi della definizione della macro. Questo flusso viene eseguito visualizzando in precedenza lo stesso file di definizione della macro oppure inserendo la definizione di una macro incorporata nel file di definizione della macro di default.

Le macro possono essere utili se gli stessi attributi devono essere applicati a immagini diverse.

[!DNL `http://server/cat/1345?wid=240&fmt=pdf&imageRes=300`]

[!DNL `http://server/cat/1435?wid=240&fmt=pdf&imageRes=300`]

[!DNL `http://server/cat/8243?wid=480&fmt=pdf&imageRes=300`]

È possibile definire una macro per gli attributi comuni:

`view wid=240&fmt=pdf&imageRes=300`

La macro viene utilizzata nel modo seguente:

[!DNL `http://server/cat/1345?$view$`]

[!DNL `http://server/cat/1435?$view$`]

[!DNL `http://server/cat/8243?$view$&wid=480`]

Poiché `wid=` è diverso per la terza richiesta, è sufficiente sostituire il valore *dopo* che la macro viene richiamata (specificando `wid=` *prima* `$view$` non ha alcun effetto).

+ [nome](r-name.md)
