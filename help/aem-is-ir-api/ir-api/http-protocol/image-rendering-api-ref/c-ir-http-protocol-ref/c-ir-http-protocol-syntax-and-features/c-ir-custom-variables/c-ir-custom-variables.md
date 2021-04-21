---
description: La porzione query delle richieste e delle stringhe modificatori di vignetta può includere variabili definite dall'utente.
solution: Experience Manager
title: Variabili personalizzate
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '253'
ht-degree: 0%

---


# Variabili personalizzate{#custom-variables}

La porzione query delle richieste e della vignetta::Le stringhe dei modificatori possono includere variabili definite dall&#39;utente.

` $ *[!DNL name]*= *[!DNL value]*`

** *[!DNL name]* **Nome della variabile. Può essere costituita da qualsiasi combinazione di caratteri alfa, cifra e sicuri, escluso &#39;$.&#39;

** *[!DNL value]* ** Valore a cui impostare la variabile (stringa).

Le variabili sono definite in modo simile ad altri comandi del server, utilizzando la sintassi riportata sopra. Prima di poter fare riferimento alle variabili, è necessario definirle. Le variabili definite in `vignette::Modifier` possono essere referenziate nella richiesta URL e viceversa.

>[!NOTE]
>
>*[!DNL value]* devono essere codificati in URL a passa singolo per una trasmissione HTTP sicura. La doppia codifica è necessaria se *[!DNL value]* viene ritrasmessa tramite HTTP. Questo è il caso in cui *[!DNL value]* viene sostituito in una richiesta esterna nidificata.

Per fare riferimento alle variabili, incorpora il nome della variabile (racchiuso da un $ iniziale e finale) in qualsiasi punto dei valori di comando. Ad esempio, tra &#39;=&#39; che segue il nome del comando e il successivo &#39;&amp;&#39; o la fine della richiesta. Il server sostituisce ogni occorrenza di $ *[!DNL name]*$ con *[!DNL string]*. Non si verificherà alcuna sostituzione in caso di occorrenze di $ *[!DNL name]*$ nei nomi dei comandi (prima del segno uguale di un comando) e nella parte del percorso della richiesta.

Le variabili personalizzate potrebbero non essere nidificate. Tutte le occorrenze di $ *[!DNL name]*$ all&#39;interno di *[!DNL string]* non vengono sostituite. Ad esempio, il frammento di richiesta `$var2=apple&$var1=my$var2$tree&text=$var1$` viene risolto in `text=my$var2$tree`.

$ non è un carattere riservato; potrebbe verificarsi altrimenti nella richiesta. Ad esempio, `src=my$texture$file.tif` è un comando valido (supponendo che esista una voce di catalogo dei materiali o un file di texture denominato [!DNL my$texture$file.tif] esiste), mentre `wid=$number$` non lo è, perché `wid=` richiede un argomento numerico.
