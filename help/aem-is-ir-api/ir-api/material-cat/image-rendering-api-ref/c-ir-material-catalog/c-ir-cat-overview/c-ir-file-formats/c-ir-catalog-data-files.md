---
description: I file di dati del catalogo possono avere qualsiasi nome e suffisso file (eccetto .ini).
seo-description: I file di dati del catalogo possono avere qualsiasi nome e suffisso file (eccetto .ini).
seo-title: File di dati del catalogo
solution: Experience Manager
title: File di dati del catalogo
topic: Scene7 Image Serving - Image Rendering API
uuid: 33d991d6-5aa7-4cc6-88d4-10c4bb83d786
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# File di dati del catalogo{#catalog-data-files}

I file di dati del catalogo possono avere qualsiasi nome e suffisso file (eccetto .ini).

I file di dati del catalogo possono essere mantenuti rapidamente utilizzando applicazioni che supportano file di dati di testo delimitati da tabulazioni, come Microsoft Excel e Access.

Essenzialmente una tabella bidimensionale, un file di dati del catalogo è costituito da un record di intestazione che identifica le colonne di dati e qualsiasi numero di record di dati (righe). I campi sia nell’intestazione che nei record di dati sono separati da `<TAB>` caratteri singoli. I record sono separati da un singolo `<CR>` (codice ASCII 0xD), un singolo `<LF>` (codice ASCII 0xA) o una `<CR><LF>` coppia.

Il record di intestazione deve contenere i nomi esatti per ciascun campo di dati. I campi vuoti non sono consentiti nella riga di intestazione. I nomi dei campi dati non fanno distinzione tra maiuscole e minuscole. Tutti i nomi dei campi devono essere univoci.

Nei record di intestazione e dati non è consentito spazio vuoto diverso dai `<TAB>` separatori di campo.

Nei record di dati, due `<TAB>` caratteri adiacenti indicano un campo vuoto. I campi vuoti erediteranno i valori predefiniti dagli attributi del catalogo o dalle impostazioni predefinite del server.

I campi dati non devono contenere `<CR>`, `<LF>`o `<TAB>` caratteri, a meno che il valore dei dati non sia di tipo testo e sia racchiuso tra virgolette singole o doppie. I campi dati non devono essere codificati tramite HTTP.

Più valori di dati nello stesso campo sono separati da virgole (&#39;,&#39;), salvo diversa indicazione.

Colonne i cui nomi iniziano con &#39;.&#39; sono ignorate; questo consente di memorizzare i dati nei cataloghi dei materiali che non interessano il rendering delle immagini. Le colonne con nomi di intestazione sconosciuti vengono ignorate e nel file di registro viene scritto un avviso.

I nomi dei campi possono essere composti da qualsiasi combinazione di lettere ASCII, numeri, nonché &quot;-&quot; e &quot;_&quot;.

È possibile utilizzare una o più colonne come chiavi di indice. Se la stessa chiave si verifica più volte nello stesso file di dati, prevarrà l&#39;istanza successiva.
