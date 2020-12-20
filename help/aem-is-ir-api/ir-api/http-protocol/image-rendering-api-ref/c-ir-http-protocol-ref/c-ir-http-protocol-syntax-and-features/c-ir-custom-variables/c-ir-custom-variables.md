---
description: La parte query delle richieste e le stringhe Modificatore vignettatura possono includere variabili definite dall'utente.
seo-description: La parte query delle richieste e le stringhe Modificatore vignettatura possono includere variabili definite dall'utente.
seo-title: Variabili personalizzate
solution: Experience Manager
title: Variabili personalizzate
topic: Scene7 Image Serving - Image Rendering API
uuid: 933fba00-759c-4bd3-bada-eec751426d9e
translation-type: tm+mt
source-git-commit: e8e5b07329bde3e23ee095d5022da62d67e9478c
workflow-type: tm+mt
source-wordcount: '260'
ht-degree: 0%

---


# Variabili personalizzate{#custom-variables}

La parte query delle richieste e delle stringhe di vignettatura::Modificatore può includere variabili definite dall&#39;utente.

` $ *[!DNL name]*= *[!DNL value]*`

** *[!DNL name]* **Nome variabile. Può essere costituita da qualsiasi combinazione di caratteri alfa, cifra e sicuri, ad eccezione di &#39;$.&#39;

** *[!DNL value]* ** Valore a cui impostare la variabile (stringa).

Le variabili sono definite in modo simile ad altri comandi del server, utilizzando la sintassi indicata sopra. Le variabili devono essere definite prima di poter fare riferimento a esse. Nella richiesta URL è possibile fare riferimento alle variabili definite in `vignette::Modifier` e viceversa.

>[!NOTE]
>
>*[!DNL value]* devono essere codificati URL a passaggio singolo per una trasmissione HTTP sicura. La doppia codifica è necessaria se *[!DNL value]* viene ritrasmessa via HTTP. Questo è il caso in cui *[!DNL value]* viene sostituito in una richiesta esterna nidificata.

Alle variabili viene fatto riferimento incorporando il nome della variabile (racchiuso da un valore iniziale e finale $) ovunque nei valori dei comandi. Ad esempio, tra &#39;=&#39; che segue il nome del comando e il successivo &#39;&amp;&#39; o la fine della richiesta. Il server sostituisce ogni occorrenza di $ *[!DNL name]*$ con *[!DNL string]*. Non si verificheranno sostituzioni nelle occorrenze di $ *[!DNL name]*$ nei nomi dei comandi (prima del segno uguale di un comando) e nella parte del percorso della richiesta.

Le variabili personalizzate non possono essere nidificate. Tutte le occorrenze di $ *[!DNL name]*$ in *[!DNL string]* non vengono sostituite. Ad esempio, il frammento di richiesta `$var2=apple&$var1=my$var2$tree&text=$var1$` viene risolto in `text=my$var2$tree`.

$ non è un carattere riservato; può verificarsi altrimenti nella richiesta. Ad esempio, `src=my$texture$file.tif` è un comando valido (supponendo che esista una voce di catalogo di materiali o un file di texture denominato [!DNL my$texture$file.tif]), mentre `wid=$number$` non lo è, perché `wid=` richiede un argomento numerico.
