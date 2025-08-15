---
description: I file di dati del catalogo possono avere qualsiasi nome e suffisso (eccetto .ini). Possono essere mantenuti facilmente utilizzando applicazioni che supportano file di dati di testo delimitati da scheda, come Microsoft Excel e Access.
solution: Experience Manager
title: File di dati del catalogo
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 4aa20abe-4f84-470b-b5a1-3d9246ab1792
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '349'
ht-degree: 0%

---

# File di dati del catalogo{#catalog-data-files}

I file di dati del catalogo possono avere qualsiasi nome e suffisso (eccetto .ini). Possono essere mantenuti facilmente utilizzando applicazioni che supportano file di dati di testo delimitati da scheda, come Microsoft Excel e Access.

Essenzialmente una tabella bidimensionale, un file di dati del catalogo è costituito da un record di intestazione che identifica le colonne di dati e qualsiasi numero di record di dati (righe). I campi nei record di intestazione e di dati sono separati da caratteri singoli `<TAB>` . I record sono separati da un singolo `<CR>` (codice `0xD`ASCII), un singolo `<LF>` (codice `0xA`ASCII) o una `<CR><LF>` coppia.

Il record di intestazione deve contenere i nomi esatti per ogni campo dati. I campi vuoti non sono consentiti nella riga di intestazione. I nomi dei campi di dati non fanno distinzione tra maiuscole e minuscole. Tutti i nomi dei campi devono essere univoci.

Gli spazi non possono essere utilizzati come separatori di campo. Non sono consentiti spazi nel record dell&#39;intestazione. Nei record di dati, tutti gli spazi all&#39;inizio o alla fine di un campo dati sono considerati parte di tale campo dati.

Nei record di dati, due caratteri adiacenti `<TAB>` indicano un campo vuoto. I campi vuoti possono ereditare i valori predefiniti dagli attributi del catalogo o dai valori predefiniti del server.

Se necessario, i campi dati possono essere racchiusi tra virgolette doppie. Non devono contenere `<CR>`, `<LF>`o `<TAB>` caratteri, a meno che il valore dei dati non sia di tipo testo e sia racchiuso tra virgolette doppie. I campi di dati non devono avere la codifica HTTP.

Se non diversamente specificato, più valori di dati nello stesso campo sono separati da virgole.

Colonne i cui nomi iniziano con &quot;.&quot; vengono ignorati. Ciò consente di memorizzare i dati in cataloghi di immagini, il che non è di alcuna interesse per Immagine Serving. Le colonne con nomi di intestazione sconosciuti vengono ignorate e viene scritta un&#39;avvertenza nel file di registro.

I nomi di campo possono essere costituiti da qualsiasi combinazione di lettere ASCII, numeri, nonché da &quot;-&quot; e &quot;_&quot;.

Una o più colonne possono essere utilizzate come chiavi indice. Se la stessa chiave si verifica più di una volta nello stesso file di dati, prevale il istanza successivo.
