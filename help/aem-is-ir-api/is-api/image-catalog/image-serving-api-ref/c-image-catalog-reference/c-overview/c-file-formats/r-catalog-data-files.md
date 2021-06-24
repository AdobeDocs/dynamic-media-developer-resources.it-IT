---
description: I file di dati del catalogo possono avere qualsiasi nome e suffisso di file (eccetto .ini). Possono essere mantenuti rapidamente utilizzando applicazioni che supportano file di dati di testo delimitati da tabulazioni, come Microsoft Excel e Access.
solution: Experience Manager
title: File di dati del catalogo
feature: Dynamic Media Classic, SDK/API
role: Developer,Business Practitioner
exl-id: 4aa20abe-4f84-470b-b5a1-3d9246ab1792
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '354'
ht-degree: 0%

---

# File di dati del catalogo{#catalog-data-files}

I file di dati del catalogo possono avere qualsiasi nome e suffisso di file (eccetto .ini). Possono essere mantenuti rapidamente utilizzando applicazioni che supportano file di dati di testo delimitati da tabulazioni, come Microsoft Excel e Access.

Essenzialmente una tabella bidimensionale, un file di dati di catalogo è costituito da un record di intestazione che identifica le colonne di dati e qualsiasi numero di record di dati (righe). I campi sia nell’intestazione che nei record di dati sono separati da un singolo `<TAB>` carattere. I record sono separati da una singola `<CR>` (codice ASCII `0xD`), un singolo `<LF>` (codice ASCII `0xA`) o una coppia `<CR><LF>`.

Il record intestazione deve contenere i nomi esatti per ciascun campo dati. I campi vuoti non sono consentiti nella riga di intestazione. I nomi dei campi dati non fanno distinzione tra maiuscole e minuscole. Tutti i nomi di campo devono essere univoci.

I caratteri spazio non possono essere utilizzati come separatori di campo. Nessun spazio consentito nel record di intestazione. Nei record di dati, gli spazi all’inizio o alla fine di un campo di dati sono considerati parte di tale campo di dati.

Nei record di dati, due caratteri adiacenti `<TAB>` indicano un campo vuoto. I campi vuoti possono ereditare valori predefiniti dagli attributi del catalogo o dalle impostazioni predefinite del server.

Facoltativamente, i campi dati possono essere racchiusi tra virgolette doppie. Non devono contenere caratteri `<CR>`, `<LF>` o `<TAB>`, a meno che il valore dei dati non sia di tipo testo e sia racchiuso tra virgolette doppie. I campi dati non devono essere codificati tramite HTTP.

Se non diversamente specificato, più valori di dati nello stesso campo sono separati da virgole.

Colonne i cui nomi iniziano con &quot;.&quot; vengono ignorati. Ciò consente di memorizzare i dati nei cataloghi di immagini, cosa che non interessa Image Serving. Le colonne con nomi di intestazione sconosciuti vengono ignorate e nel file di registro viene scritto un avviso.

I nomi dei campi possono essere composti da qualsiasi combinazione di lettere ASCII, numeri, nonché &quot;-&quot; e &quot;_&quot;.

È possibile utilizzare una o più colonne come chiavi di indice. Se la stessa chiave si verifica più di una volta nello stesso file di dati, prevale l’istanza successiva.
