---
title: File di dati catalogo
description: I file di dati del catalogo possono avere qualsiasi nome e suffisso di file (eccetto .ini).
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 1fb91795-f699-40b4-a6bc-6eab3e1ecd1d
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '298'
ht-degree: 0%

---

# File di dati catalogo{#catalog-data-files}

I file di dati del catalogo possono avere qualsiasi nome e suffisso di file (eccetto `.ini`).

I file di dati del catalogo possono essere gestiti facilmente utilizzando applicazioni che supportano file di dati di testo delimitati da tabulazioni, ad esempio Microsoft® Excel e Access.

Essenzialmente una tabella bidimensionale, un file di dati di catalogo è costituito da un record di intestazione che identifica le colonne di dati e un numero qualsiasi di record di dati (righe). I campi sia nell&#39;intestazione che nei record di dati sono separati da singoli `<TAB>` caratteri. I record sono separati da un singolo `<CR>` (codice ASCII `0xD`), un singolo `<LF>` (codice ASCII `0xA`) o una coppia `<CR><LF>`.

Il record di intestazione deve contenere i nomi esatti di ciascun campo dati. La riga di intestazione non può contenere campi vuoti. I nomi dei campi dati non fanno distinzione tra maiuscole e minuscole. Tutti i nomi dei campi devono essere univoci.

Nei record di intestazione e dati non sono consentiti spazi vuoti diversi dai separatori di campo `<TAB>`.

Nei record di dati, due caratteri `<TAB>` adiacenti indicano un campo vuoto. I campi vuoti ereditano i valori predefiniti dagli attributi del catalogo o dai valori predefiniti del server.

I campi dati non possono contenere `<CR>`, `<LF>` o `<TAB>` caratteri, a meno che il valore dei dati non sia di tipo testo e sia racchiuso tra virgolette singole o doppie. Non codificare i campi dati tramite HTTP.

Se non diversamente specificato, più valori di dati nello stesso campo sono separati da virgole (&#39;,&#39;).

Colonne i cui nomi iniziano con &quot;.&quot; vengono ignorati; ciò consente di memorizzare i dati in cataloghi di materiali che non sono di alcun interesse per Image Rendering. Le colonne con nomi di intestazione sconosciuti vengono ignorate e viene scritto un avviso nel file di registro.

I nomi dei campi possono essere costituiti da qualsiasi combinazione di lettere ASCII, numeri e &quot;-&quot; e &quot;_&quot;.

È possibile utilizzare una o più colonne come chiavi di indice. Se la stessa chiave si trova più di una volta nello stesso file di dati, prevale l’istanza successiva.
