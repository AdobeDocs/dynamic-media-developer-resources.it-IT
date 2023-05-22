---
title: Variabili personalizzate
description: La porzione query delle richieste e delle stringhe del modificatore di vignettatura può includere variabili definite dall'utente.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 8d26b797-5099-49fb-b7e0-46747f35ab84
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '247'
ht-degree: 0%

---

# Variabili personalizzate{#custom-variables}

La porzione di query delle richieste e delle stringhe di vignettatura::Modifier può includere variabili definite dall&#39;utente.

`$ [!DNL name] = [!DNL value]`

`[!DNL name]` - Nome della variabile. Può essere costituito da qualsiasi combinazione di caratteri alfanumerici, numerici e di sicurezza, esclusi `$`.

`[!DNL value]` - Valore su cui deve essere impostata la variabile (stringa).

Le variabili sono definite in modo simile ad altri comandi server, utilizzando la sintassi precedente. Le variabili devono essere definite prima di poter essere referenziate. Variabili definite in `vignette::Modifier` possono essere indicati nella richiesta URL, e viceversa.

>[!NOTE]
>
>`[!DNL value]` deve essere codificata in URL a passaggio singolo per una trasmissione HTTP sicura. È necessaria la doppia codifica se `[!DNL value]` viene ritrasmesso tramite HTTP. Questa situazione si verifica quando `[!DNL value]` viene sostituito in una richiesta esterna nidificata.

Per fare riferimento alle variabili, incorpora il nome della variabile (racchiuso tra un iniziale e un finale `$`) ovunque nei valori dei comandi. Ad esempio, tra `=`  dopo il nome del comando e il successivo `&` o alla fine della richiesta. Il server sostituisce ogni occorrenza di questo tipo `$ [!DNL name]$` con `[!DNL string]`. Non si verificano sostituzioni in nessun caso di `$ [!DNL name]$` in nomi di comando (prima del segno di uguale di un comando) e nella parte relativa al percorso della richiesta.

Le variabili personalizzate potrebbero non essere nidificate. Qualsiasi occorrenza di `$ [!DNL name]$` entro `[!DNL string]` non vengono sostituiti. Ad esempio, il frammento di richiesta `$var2=apple&$var1=my$var2$tree&text=$var1$` si risolve in `text=my$var2$tree`.

`$` non è un carattere riservato; potrebbe verificarsi altrimenti nella richiesta. Ad esempio: `src=my$texture$file.tif` è un comando valido (supponendo che una voce di catalogo dei materiali o un file di trama denominato `[!DNL my$texture$file.tif]` esiste), mentre `wid=$number$` non lo è, perché `wid=` richiede un argomento numerico.
