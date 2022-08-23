---
title: File di dati del catalogo
description: I file di dati del catalogo possono avere qualsiasi nome e suffisso di file (eccetto .ini).
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 1fb91795-f699-40b4-a6bc-6eab3e1ecd1d
source-git-commit: 8454991568374ecd1c4babdd3210250ea7988c4c
workflow-type: tm+mt
source-wordcount: '298'
ht-degree: 0%

---

# File di dati del catalogo{#catalog-data-files}

I file di dati del catalogo possono avere qualsiasi nome e suffisso di file (eccetto `.ini`).

I file di dati del catalogo possono essere mantenuti rapidamente utilizzando applicazioni che supportano file di dati di testo delimitati da tabulazioni, come Microsoft® Excel e Access.

Essenzialmente una tabella bidimensionale, un file di dati di catalogo è costituito da un record di intestazione che identifica le colonne di dati e qualsiasi numero di record di dati (righe). I campi sia nell’intestazione che nei record di dati sono separati da un singolo `<TAB>` caratteri. I record sono separati da un singolo `<CR>` (codice ASCII) `0xD`), un singolo `<LF>` (codice ASCII) `0xA`) o un `<CR><LF>` coppia.

Il record intestazione deve contenere i nomi esatti per ciascun campo dati. I campi vuoti non sono consentiti nella riga di intestazione. I nomi dei campi dati non fanno distinzione tra maiuscole e minuscole. Tutti i nomi di campo devono essere univoci.

Nessun spazio bianco diverso dal `<TAB>` i separatori di campo sono consentiti nei record di intestazione e dati.

Nei record di dati, due `<TAB>` i caratteri indicano un campo vuoto. I campi vuoti ereditano i valori predefiniti dagli attributi del catalogo o dai valori predefiniti del server.

I campi dati non devono contenere `<CR>`, `<LF>`oppure `<TAB>` caratteri, a meno che il valore dei dati non sia di tipo testo e non sia racchiuso tra virgolette singole o doppie. Non codificare i campi dati HTTP.

Se non diversamente specificato, più valori di dati nello stesso campo sono separati da virgole (&#39;,&#39;).

Colonne i cui nomi iniziano con &#39;.&#39; sono ignorati; questo consente di memorizzare i dati in cataloghi di materiali che non sono di interesse per Image Rendering. Le colonne con nomi di intestazione sconosciuti vengono ignorate e nel file di registro viene scritto un avviso.

I nomi dei campi possono essere composti da qualsiasi combinazione di lettere ASCII, numeri e &quot;-&quot; e &quot;_&quot;.

È possibile utilizzare una o più colonne come chiavi di indice. Se la stessa chiave si verifica più di una volta nello stesso file di dati, prevale l’istanza successiva.
