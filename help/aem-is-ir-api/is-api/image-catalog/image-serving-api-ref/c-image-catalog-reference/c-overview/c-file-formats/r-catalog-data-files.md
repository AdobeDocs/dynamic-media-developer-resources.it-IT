---
description: I file di dati del catalogo possono avere qualsiasi nome e suffisso di file (eccetto .ini). Possono essere gestiti facilmente utilizzando applicazioni che supportano file di dati di testo delimitati da tabulazioni, ad esempio Microsoft Excel e Access.
solution: Experience Manager
title: File di dati catalogo
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 4aa20abe-4f84-470b-b5a1-3d9246ab1792
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '349'
ht-degree: 0%

---

# File di dati catalogo{#catalog-data-files}

I file di dati del catalogo possono avere qualsiasi nome e suffisso di file (eccetto .ini). Possono essere gestiti facilmente utilizzando applicazioni che supportano file di dati di testo delimitati da tabulazioni, ad esempio Microsoft Excel e Access.

Essenzialmente una tabella bidimensionale, un file di dati di catalogo è costituito da un record di intestazione che identifica le colonne di dati e un numero qualsiasi di record di dati (righe). I campi sia nell’intestazione che nei record di dati sono separati da un singolo `<TAB>` caratteri. I record sono separati da un singolo `<CR>` (codice ASCII `0xD`), un singolo `<LF>` (codice ASCII `0xA`) o `<CR><LF>` coppia.

Il record di intestazione deve contenere i nomi esatti di ciascun campo dati. La riga di intestazione non può contenere campi vuoti. I nomi dei campi dati non fanno distinzione tra maiuscole e minuscole. Tutti i nomi dei campi devono essere univoci.

I caratteri di spaziatura non possono essere utilizzati come separatori di campo. Non sono consentiti spazi nel record di intestazione. Nei record di dati, qualsiasi spazio all&#39;inizio o alla fine di un campo di dati è considerato parte di tale campo.

Nei record di dati, due `<TAB>` i caratteri indicano un campo vuoto. I campi vuoti possono ereditare i valori predefiniti dagli attributi del catalogo o dai valori predefiniti del server.

I campi dati possono essere facoltativamente racchiusi tra virgolette doppie. Essi non devono contenere `<CR>`, `<LF>`, o `<TAB>` caratteri, a meno che il valore dei dati non sia di tipo testo e sia racchiuso tra virgolette doppie. I campi dati non devono avere la codifica HTTP.

Se non diversamente specificato, più valori di dati nello stesso campo sono separati da virgole.

Colonne i cui nomi iniziano con &quot;.&quot; vengono ignorati. Questo consente di memorizzare i dati nei cataloghi di immagini, il che non è di alcun interesse per Image Server. Le colonne con nomi di intestazione sconosciuti vengono ignorate e viene scritto un avviso nel file di registro.

I nomi dei campi possono essere costituiti da qualsiasi combinazione di lettere ASCII, numeri, nonché da &quot;-&quot; e &quot;_&quot;.

È possibile utilizzare una o più colonne come chiavi di indice. Se la stessa chiave si trova più di una volta nello stesso file di dati, prevale l’istanza successiva.
