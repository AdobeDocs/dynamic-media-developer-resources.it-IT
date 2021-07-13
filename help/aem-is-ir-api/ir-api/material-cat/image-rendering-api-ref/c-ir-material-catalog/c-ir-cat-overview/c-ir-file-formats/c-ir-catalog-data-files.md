---
description: I file di dati del catalogo possono avere qualsiasi nome e suffisso di file (eccetto .ini).
solution: Experience Manager
title: File di dati del catalogo
feature: Dynamic Media Classic, SDK/API
role: Developer,User
exl-id: 1fb91795-f699-40b4-a6bc-6eab3e1ecd1d
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '311'
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
