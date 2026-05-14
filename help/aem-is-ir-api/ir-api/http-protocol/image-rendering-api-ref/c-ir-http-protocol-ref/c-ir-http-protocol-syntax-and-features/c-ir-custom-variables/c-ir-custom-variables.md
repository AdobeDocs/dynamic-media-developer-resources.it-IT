---
title: Variabili personalizzate
description: La porzione query delle richieste e delle stringhe del modificatore di vignettatura può includere variabili definite dall'utente.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 8d26b797-5099-49fb-b7e0-46747f35ab84
TQID: 'https://experienceleague.adobe.com/1-o3GqgzwvPYV8UDBuZu5udOiG-p8Tue3Fo-ft8-QhI'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 251
ht-degree: 0%

---

# Variabili personalizzate{#custom-variables}

La porzione di query delle richieste e delle stringhe di vignettatura::Modifier può includere variabili definite dall&#39;utente.

`$ [!DNL name] = [!DNL value]`

`[!DNL name]` - Nome variabile. Può essere costituito da qualsiasi combinazione di caratteri alfanumerici, numerici e di sicurezza, escluso `$`.

`[!DNL value]` - Valore su cui deve essere impostata la variabile (stringa).

Le variabili sono definite in modo simile ad altri comandi server, utilizzando la sintassi precedente. Le variabili devono essere definite prima di poter essere referenziate. Le variabili definite in `vignette::Modifier` possono essere referenziate nella richiesta dell&#39;URL e viceversa.

>[!NOTE]
>
>`[!DNL value]` deve avere un URL con codifica single-pass per una trasmissione HTTP sicura. È necessaria la doppia codifica se `[!DNL value]` viene ritrasmesso tramite HTTP. Ciò si verifica quando `[!DNL value]` viene sostituito in una richiesta esterna nidificata.

Per fare riferimento alle variabili, incorpora il nome della variabile (racchiuso tra `$` iniziale e finale) ovunque nei valori del comando. Ad esempio, tra `=` dopo il nome del comando e il successivo `&` o la fine della richiesta. Il server sostituisce ogni occorrenza di `$ [!DNL name]$` con `[!DNL string]`. Nessuna sostituzione eseguita per le occorrenze di `$ [!DNL name]$` nei nomi dei comandi (prima del segno di uguale di un comando) e nella parte relativa al percorso della richiesta.

Le variabili personalizzate potrebbero non essere nidificate. Eventuali occorrenze di `$ [!DNL name]$` in `[!DNL string]` non vengono sostituite. Ad esempio, il frammento di richiesta `$var2=apple&$var1=my$var2$tree&text=$var1$` viene risolto in `text=my$var2$tree`.

`$` non è un carattere riservato. È possibile che la richiesta non contenga alcun carattere riservato. `src=my$texture$file.tif`, ad esempio, è un comando valido (supponendo che esista una voce di catalogo dei materiali o un file di trama denominato `[!DNL my$texture$file.tif]`), mentre `wid=$number$` non lo è, perché `wid=` richiede un argomento numerico.
