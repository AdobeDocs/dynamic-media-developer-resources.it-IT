---
description: I file di dati del catalogo possono avere qualsiasi nome e suffisso file (eccetto .ini).
seo-description: I file di dati del catalogo possono avere qualsiasi nome e suffisso file (eccetto .ini).
seo-title: File di dati del catalogo
solution: Experience Manager
title: File di dati del catalogo
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 33d991d6-5aa7-4cc6-88d4-10c4bb83d786
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '321'
ht-degree: 0%

---


# File di dati del catalogo{#catalog-data-files}

I file di dati del catalogo possono avere qualsiasi nome e suffisso file (eccetto .ini).

I file di dati del catalogo possono essere mantenuti rapidamente utilizzando applicazioni che supportano file di dati di testo delimitati da tabulazioni, come Microsoft Excel e Access.

Essenzialmente una tabella bidimensionale, un file di dati del catalogo è costituito da un record di intestazione che identifica le colonne di dati e qualsiasi numero di record di dati (righe). I campi sia nell&#39;intestazione che nei record di dati sono separati da caratteri `<TAB>` singoli. I record sono separati da una singola `<CR>` (codice ASCII 0xD), una singola `<LF>` (codice ASCII 0xA) o una coppia `<CR><LF>`.

Il record di intestazione deve contenere i nomi esatti per ciascun campo di dati. I campi vuoti non sono consentiti nella riga di intestazione. I nomi dei campi dati non fanno distinzione tra maiuscole e minuscole. Tutti i nomi dei campi devono essere univoci.

Nei record di intestazione e dati non è consentito spazio vuoto diverso dai separatori di campo `<TAB>`.

Nei record di dati, due caratteri `<TAB>` adiacenti indicano un campo vuoto. I campi vuoti erediteranno i valori predefiniti dagli attributi del catalogo o dalle impostazioni predefinite del server.

I campi dati non devono contenere caratteri `<CR>`, `<LF>` o `<TAB>`, a meno che il valore dei dati non sia di tipo testo e sia racchiuso tra virgolette singole o doppie. I campi dati non devono essere codificati tramite HTTP.

Più valori di dati nello stesso campo sono separati da virgole (&#39;,&#39;), salvo diversa indicazione.

Colonne i cui nomi iniziano con &#39;.&#39; sono ignorate; questo consente di memorizzare i dati nei cataloghi dei materiali che non interessano il rendering delle immagini. Le colonne con nomi di intestazione sconosciuti vengono ignorate e nel file di registro viene scritto un avviso.

I nomi dei campi possono essere composti da qualsiasi combinazione di lettere ASCII, numeri, nonché &quot;-&quot; e &quot;_&quot;.

È possibile utilizzare una o più colonne come chiavi di indice. Se la stessa chiave si verifica più volte nello stesso file di dati, prevarrà l&#39;istanza successiva.
