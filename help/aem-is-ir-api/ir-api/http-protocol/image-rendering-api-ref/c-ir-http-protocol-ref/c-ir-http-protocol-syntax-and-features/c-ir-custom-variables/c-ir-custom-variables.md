---
title: Variabili personalizzate
description: La porzione query delle richieste e delle stringhe modificatori di vignetta può includere variabili definite dall'utente.
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

La porzione query delle richieste e della vignetta::Le stringhe dei modificatori possono includere variabili definite dall&#39;utente.

`$ [!DNL name] = [!DNL value]`

`[!DNL name]` - Nome della variabile. Può essere costituita da qualsiasi combinazione di caratteri alfa, cifra e sicuri, esclusi `$`.

`[!DNL value]` - Valore a cui impostare la variabile (stringa).

Le variabili sono definite in modo simile ad altri comandi del server, utilizzando la sintassi riportata sopra. Prima di poter fare riferimento alle variabili, è necessario definirle. Variabili definite in `vignette::Modifier` possono essere referenziati nella richiesta URL e viceversa.

>[!NOTE]
>
>`[!DNL value]` devono essere codificati in URL a passa singolo per una trasmissione HTTP sicura. La doppia codifica è necessaria se `[!DNL value]` viene ritrasmesso tramite HTTP. Questa situazione si verifica quando `[!DNL value]` viene sostituito in una richiesta esterna nidificata.

Per fare riferimento alle variabili, incorpora il nome della variabile (racchiuso da un iniziale e da un finale `$`) in qualsiasi punto dei valori dei comandi. Ad esempio, tra `=`  seguendo il nome del comando e il successivo `&` o la fine della richiesta. Il server sostituisce ogni occorrenza di `$ [!DNL name]$` con `[!DNL string]`. Non si verificano sostituzioni in caso di `$ [!DNL name]$` nei nomi dei comandi (prima del segno uguale di un comando) e nella parte del percorso della richiesta.

Le variabili personalizzate potrebbero non essere nidificate. Qualsiasi occorrenza di `$ [!DNL name]$` entro `[!DNL string]` non sono sostituiti. Ad esempio, il frammento di richiesta `$var2=apple&$var1=my$var2$tree&text=$var1$` risolve in `text=my$var2$tree`.

`$` non è un carattere riservato; potrebbe verificarsi altrimenti nella richiesta. Ad esempio: `src=my$texture$file.tif` è un comando valido (supponendo che una voce del catalogo dei materiali o un file di texture denominato `[!DNL my$texture$file.tif]` esiste), mentre `wid=$number$` non è perché `wid=` richiede un argomento numerico.
