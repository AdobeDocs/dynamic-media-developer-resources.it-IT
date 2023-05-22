---
description: Le macro dei comandi forniscono scelte rapide denominate per insiemi di comandi.
solution: Experience Manager
title: Macro dei comandi
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: dc149977-3ca8-4612-ad05-4d565440d00a
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '250'
ht-degree: 0%

---

# Macro dei comandi{#command-macros}

Le macro dei comandi forniscono scelte rapide denominate per insiemi di comandi.

Le macro vengono definite in file di definizione delle macro separati, che possono essere allegati ai cataloghi di immagini o al catalogo predefinito.

Le macro possono essere richiamate in qualsiasi punto di una richiesta dopo il segno &quot;?&quot;, nonché in qualsiasi punto di una `catalog::Modifier` campo. Le macro possono rappresentare solo uno o più comandi Image Server completi, pertanto devono essere racchiuse tra separatori &#39;&amp;&#39;, tranne quando si trova all&#39;inizio o alla fine della stringa del modificatore.

Le chiamate macro vengono sostituite dalle relative stringhe di sostituzione nelle prime fasi dell&#39;analisi. I comandi all&#39;interno delle macro sostituiscono gli stessi comandi nella richiesta se si verificano prima della chiamata della macro nella richiesta. Questo è diverso da `catalog::Modifier`, in cui i comandi nella stringa di richiesta sovrascriveranno sempre i comandi nella `catalog::Modifier` stringa, indipendentemente dalla posizione nella richiesta.

Le macro possono essere nidificate, con la seguente restrizione: una macro può essere richiamata solo se è già definita al momento dell&#39;analisi della definizione della macro, visualizzandola in precedenza nello stesso file di definizione della macro oppure inserendo la definizione di tale macro incorporata nel file di definizione della macro predefinito.

Le macro possono essere utili se gli stessi attributi devono essere applicati a immagini diverse.

[!DNL http://server/cat/1345?wid=240&fmt=pdf&imageRes=300]

[!DNL http://server/cat/1435?wid=240&fmt=pdf&imageRes=300]

[!DNL http://server/cat/8243?wid=480&fmt=pdf&imageRes=300]

È possibile definire una macro per gli attributi comuni:

`view wid=240&fmt=pdf&imageRes=300`

La macro viene utilizzata nel modo seguente:

[!DNL http://server/cat/1345?$view$]

[!DNL http://server/cat/1435?$view$]

[!DNL http://server/cat/8243?$view$&wid=480]

Da `wid=` è diverso per la terza richiesta, il valore viene semplicemente ignorato *dopo* la macro viene richiamata (specificando `wid=`*prima di* `$view$` non avrebbe alcun effetto).

+ [nome](r-name.md)
