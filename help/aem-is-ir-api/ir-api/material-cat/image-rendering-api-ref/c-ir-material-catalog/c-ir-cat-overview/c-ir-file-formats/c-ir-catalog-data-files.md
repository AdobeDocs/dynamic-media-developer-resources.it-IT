---
description: I file di dati del catalogo possono avere qualsiasi nome e suffisso di file (eccetto .ini).
seo-description: I file di dati del catalogo possono avere qualsiasi nome e suffisso di file (eccetto .ini).
seo-title: File di dati del catalogo
solution: Experience Manager
title: File di dati del catalogo
uuid: 33d991d6-5aa7-4cc6-88d4-10c4bb83d786
feature: Dynamic Media Classic, SDK/API
role: Sviluppatore, Business Practices
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '329'
ht-degree: 0%

---


# File di dati del catalogo{#catalog-data-files}

I file di dati del catalogo possono avere qualsiasi nome e suffisso di file (eccetto .ini).

I file di dati del catalogo possono essere mantenuti rapidamente utilizzando applicazioni che supportano file di dati di testo delimitati da tabulazioni, come Microsoft Excel e Access.

Essenzialmente una tabella bidimensionale, un file di dati di catalogo è costituito da un record di intestazione che identifica le colonne di dati e qualsiasi numero di record di dati (righe). I campi sia nell’intestazione che nei record di dati sono separati da un singolo `<TAB>` carattere. I record sono separati da una singola `<CR>` (codice ASCII 0xD), un singolo `<LF>` (codice ASCII 0xA) o una coppia `<CR><LF>`.

Il record intestazione deve contenere i nomi esatti per ciascun campo dati. I campi vuoti non sono consentiti nella riga di intestazione. I nomi dei campi dati non fanno distinzione tra maiuscole e minuscole. Tutti i nomi di campo devono essere univoci.

Nei record di intestazione e dati non è consentito usare spazi bianchi diversi dai separatori di campo `<TAB>` .

Nei record di dati, due caratteri adiacenti `<TAB>` indicano un campo vuoto. I campi vuoti erediteranno i valori predefiniti dagli attributi del catalogo o dalle impostazioni predefinite del server.

I campi dati non devono contenere caratteri `<CR>`, `<LF>` o `<TAB>`, a meno che il valore dei dati non sia di tipo testo e non sia racchiuso tra virgolette singole o doppie. I campi dati non devono essere codificati tramite HTTP.

Se non diversamente specificato, più valori di dati nello stesso campo sono separati da virgole (&#39;,&#39;).

Colonne i cui nomi iniziano con &#39;.&#39; sono ignorati; questo consente di memorizzare i dati in cataloghi di materiali che non sono di interesse per Image Rendering. Le colonne con nomi di intestazione sconosciuti vengono ignorate e nel file di registro viene scritto un avviso.

I nomi dei campi possono essere composti da qualsiasi combinazione di lettere ASCII, numeri, nonché &quot;-&quot; e &quot;_&quot;.

È possibile utilizzare una o più colonne come chiavi di indice. Se la stessa chiave si verifica più di una volta nello stesso file di dati, prevarrà l&#39;istanza successiva.
