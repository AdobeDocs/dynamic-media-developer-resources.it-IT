---
title: Cataloghi di materiali
description: I cataloghi di materiali offrono diverse funzioni.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 502f80f5-fdd1-468b-89a9-64cc9128d655
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '298'
ht-degree: 0%

---

# Cataloghi di materiali {#material-catalogs}

I cataloghi di materiali offrono diverse funzioni.

* Consente la definizione persistente dei materiali, incluse tutte le proprietà dei materiali.

  I materiali definiti nel catalogo dei materiali possono essere referenziati utilizzando un ID semplice, anziché un insieme di proprietà dei materiali.
* Specifica le impostazioni predefinite per alcuni attributi di richiesta, ad esempio la qualità JPEG o una dimensione predefinita per l&#39;immagine di risposta.
* Gestisci le vignettature, i profili ICC e i modelli di richiesta.

Anche se non sono definiti cataloghi di materiale specifici, tutte le caratteristiche dei cataloghi di materiale sono disponibili tramite il catalogo predefinito ( [!DNL default.ini]).

Anche se i materiali di rendering possono essere specificati esplicitamente nelle richieste che utilizzano gli attributi dei materiali, spesso è più opportuno nascondere i dettagli dei materiali dal sito web utilizzando i cataloghi dei materiali. i comandi src= accettano riferimenti di catalogo anziché percorsi di file espliciti. Una voce di catalogo è costituita da ` [ *[!DNL catId]*/] *[!DNL itemId]*`, dove ` *[!DNL catId]*` identifica un catalogo di materiali e ` *[!DNL itemId]*` identifica un record nel catalogo. Se ` *[!DNL catId]*` non è specificato, viene utilizzato il catalogo delle sessioni (vedi sotto).

Un record catalogo viene trovato correttamente se (a) ` *[!DNL catId]*` corrisponde al valore `attribute::RootId` di un catalogo di materiali e (b) ` *[!DNL recId]*` corrisponde al valore catalog::Id nello stesso catalogo. In caso di esito positivo, gli attributi del materiale (incluso `src=`) vengono impostati sui dati del record del catalogo. Se il MSS include attributi aggiuntivi per questo materiale oltre a src=, sovrascriveranno i valori del record catalogo.

Se ` *[!DNL recId]*` non corrisponde a una voce di catalogo, ` *[!DNL catId]*` viene sostituito con `attribute::RootPath` dal catalogo e il percorso risultante viene quindi considerato un percorso di file semplice. Altri attributi predefiniti, ad esempio `attribute::Resolution`, possono essere ereditati dal catalogo dei materiali.

Vignettature e profili ICC possono essere dettagliati in cataloghi di materiali simili ai materiali stessi e date proprietà. Inoltre, la mappa di vignettatura fornisce anche il contenitore per i modelli.

**Vedere anche**

Riferimento catalogo materiali, [`src=`](../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-src.md#reference-62c98abad22149d68d405ed6aaff8272), `attribute::RootId`, `attribute::RootPath`, `attribute::VignettePath`
