---
description: I cataloghi dei materiali offrono diverse funzioni.
seo-description: I cataloghi dei materiali offrono diverse funzioni.
seo-title: Cataloghi dei materiali *
solution: Experience Manager
title: Cataloghi dei materiali *
topic: Scene7 Image Serving - Image Rendering API
uuid: 2a2f371e-0982-47c7-b3da-678a5ff6c7a7
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '304'
ht-degree: 0%

---


# Cataloghi dei materiali *{#material-catalogs}

I cataloghi dei materiali offrono diverse funzioni.

* Consente la definizione permanente dei materiali, comprese tutte le proprietà dei materiali.

   I materiali definiti nel catalogo dei materiali possono essere citati utilizzando un ID semplice, anziché un insieme di proprietà del materiale.
* Specificare i valori predefiniti per alcuni attributi di richiesta, ad esempio la qualità JPEG o una dimensione immagine di risposta predefinita.
* Gestire vignettature, profili ICC e modelli di richiesta.

Anche se non sono definiti cataloghi di materiali specifici, tutte le funzioni dei cataloghi di materiali sono disponibili tramite il catalogo predefinito ( [!DNL default.ini]).

Anche se i materiali di rendering possono essere specificati esplicitamente nelle richieste utilizzando gli attributi dei materiali, in molti casi è più opportuno nascondere i dettagli dei materiali dal sito Web utilizzando cataloghi dei materiali. i comandi src= accettano riferimenti a cataloghi invece di percorsi di file espliciti. Una voce di catalogo è costituita da ` [ *[!DNL catId]*/] *[!DNL itemId]*`, dove ` *[!DNL catId]*` identifica un catalogo di materiali e ` *[!DNL itemId]*` identifica un record nel catalogo. Se ` *[!DNL catId]*` non è specificato, viene utilizzato il catalogo delle sessioni (vedere di seguito).

La corrispondenza di un record di catalogo viene eseguita correttamente se (a) ` *[!DNL catId]*` corrisponde al valore `attribute::RootId` di un catalogo di materiali e (b) ` *[!DNL recId]*` corrisponde al valore del catalogo::Id nello stesso catalogo. In caso di corrispondenza positiva, gli attributi del materiale (incluso `src=`) vengono impostati sui dati del record del catalogo. Se MSS include attributi aggiuntivi per questo materiale oltre a src=, sostituiscono i valori dal record del catalogo.

Se non è possibile associare ` *[!DNL recId]*` a una voce di catalogo, ` *[!DNL catId]*` viene sostituito con `attribute::RootPath` dal catalogo e il percorso risultante viene quindi considerato come un semplice percorso di file. Altri attributi predefiniti (ad esempio `attribute::Resolution`) può anche essere ereditata dal catalogo dei materiali.

Le vignettature e i profili ICC possono essere elencati in cataloghi di materiali simili ai materiali stessi e a determinate proprietà. Inoltre, la mappa vignettatura fornisce anche il contenitore per i modelli.

**Consultate anche**

Riferimento catalogo materiali, [ `src=`](../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-src.md#reference-62c98abad22149d68d405ed6aaff8272), `attribute::RootId`, `attribute::RootPath`, `attribute::VignettePath`
