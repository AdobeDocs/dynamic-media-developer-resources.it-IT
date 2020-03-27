---
description: I file di dati del catalogo possono avere qualsiasi nome e suffisso file (eccetto .ini). È possibile mantenerli rapidamente utilizzando applicazioni che supportano file di dati di testo delimitati da tabulazioni, come Microsoft Excel e Access.
seo-description: I file di dati del catalogo possono avere qualsiasi nome e suffisso file (eccetto .ini). È possibile mantenerli rapidamente utilizzando applicazioni che supportano file di dati di testo delimitati da tabulazioni, come Microsoft Excel e Access.
seo-title: File di dati del catalogo
solution: Experience Manager
title: File di dati del catalogo
topic: Scene7 Image Serving - Image Rendering API
uuid: 0f66e2fe-5b8a-43d3-bf2e-8dd79da6a581
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# File di dati del catalogo{#catalog-data-files}

I file di dati del catalogo possono avere qualsiasi nome e suffisso file (eccetto .ini). È possibile mantenerli rapidamente utilizzando applicazioni che supportano file di dati di testo delimitati da tabulazioni, come Microsoft Excel e Access.

Essenzialmente una tabella bidimensionale, un file di dati del catalogo è costituito da un record di intestazione che identifica le colonne di dati e qualsiasi numero di record di dati (righe). I campi sia nell’intestazione che nei record di dati sono separati da `<TAB>` caratteri singoli. I record sono separati da un singolo `<CR>` (codice ASCII `0xD`), un singolo `<LF>` (codice ASCII `0xA`) o una `<CR><LF>` coppia.

Il record di intestazione deve contenere i nomi esatti per ciascun campo di dati. I campi vuoti non sono consentiti nella riga di intestazione. I nomi dei campi dati non fanno distinzione tra maiuscole e minuscole. Tutti i nomi dei campi devono essere univoci.

I caratteri spazio non possono essere utilizzati come separatori di campo. Non sono consentiti spazi nel record di intestazione. Nei record di dati, tutti gli spazi all&#39;inizio o alla fine di un campo di dati sono considerati parte di tale campo.

Nei record di dati, due `<TAB>` caratteri adiacenti indicano un campo vuoto. I campi vuoti possono ereditare i valori predefiniti dagli attributi del catalogo o dalle impostazioni predefinite del server.

Facoltativamente, i campi dati possono essere racchiusi tra virgolette doppie. Non devono contenere `<CR>`, `<LF>`o `<TAB>` caratteri, a meno che il valore dei dati non sia di tipo testo e sia racchiuso tra virgolette doppie. I campi dati non devono essere codificati tramite HTTP.

Più valori di dati nello stesso campo sono separati da virgole, se non diversamente specificato.

Colonne i cui nomi iniziano con &quot;.&quot; vengono ignorate. Questo consente di memorizzare i dati nei cataloghi delle immagini, cosa che non interessa Image Server. Le colonne con nomi di intestazione sconosciuti vengono ignorate e nel file di registro viene scritto un avviso.

I nomi dei campi possono essere composti da qualsiasi combinazione di lettere ASCII, numeri, nonché &quot;-&quot; e &quot;_&quot;.

È possibile utilizzare una o più colonne come chiavi di indice. Se la stessa chiave si verifica più volte nello stesso file di dati, prevale l&#39;istanza successiva.
