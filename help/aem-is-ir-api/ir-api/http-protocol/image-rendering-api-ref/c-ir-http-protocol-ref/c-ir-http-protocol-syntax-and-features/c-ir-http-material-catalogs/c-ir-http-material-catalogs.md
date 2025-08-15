---
title: Cataloghi di materiali
description: I cataloghi dei materiali offrono diverse funzionalità.
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

I cataloghi dei materiali offrono diverse funzionalità.

* Consente la definizione persistente dei materiali, incluse tutte le proprietà del materiale.

  È possibile fare riferimento ai materiali definiti nel catalogo dei materiali utilizzando un semplice ID anziché un insieme di proprietà del materiale.
* Specificate le impostazioni predefinite per determinati attributi richiesta, ad esempio la qualità JPEG o le dimensioni predefinite dell&#39;immagine di risposta.
* Consente di gestire vignettature, profili ICC e modelli richiesta.

Anche se non sono definiti cataloghi di materiali specifici, tutte le funzionalità dei cataloghi di materiali sono disponibili tramite il catalogo predefinito ( [!DNL default.ini]).

Mentre i materiali di rendering possono essere specificati esplicitamente nelle richieste che utilizzano gli attributi del materiale, spesso è più desiderabile nascondere i dettagli dei materiali dal sito Web utilizzando cataloghi di materiali. I comandi src= accettano riferimenti a cataloghi invece di percorsi di file espliciti. Una voce di catalogo è costituita da ` [ *[!DNL catId]*/] *[!DNL itemId]*`, dove ` *[!DNL catId]*` identifica un catalogo di materiali e ` *[!DNL itemId]*` identifica un record nel catalogo. Se ` *[!DNL catId]*` non è specificato, viene utilizzato il catalogo di sessione (vedere di seguito).

Un record di catalogo viene abbinato correttamente se (a) ` *[!DNL catId]*` corrisponde al `attribute::RootId` valore di un catalogo di materiali e (b) ` *[!DNL recId]*` corrisponde al valore catalog::Id nello stesso catalogo. Se esiste una corrispondenza positiva, gli attributi del materiale (incluso `src=`) vengono impostati sui dati dal record del catalogo. Se l&#39;MSS include attributi aggiuntivi per questo materiale oltre a src=, ignorano i valori dal record del catalogo.

Se ` *[!DNL recId]*` non può essere associato a una voce di catalogo, viene ` *[!DNL catId]*` sostituito con `attribute::RootPath` dal catalogo e si presume che il percorso risultante sia un percorso di file semplice. Anche altri attributi predefiniti (ad esempio, `attribute::Resolution`) possono essere ereditati dal catalogo dei materiali.

Le vignettature e i profili ICC possono essere dettagliati in cataloghi di materiali simili ai materiali stessi e le proprietà fornite. Inoltre, la mappa delle vignette funge anche da contenitore per i modelli.

**Vedi anche**

Riferimento al catalogo dei materiali, [`src=`](../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-src.md#reference-62c98abad22149d68d405ed6aaff8272), `attribute::RootId`, `attribute::RootPath`, `attribute::VignettePath`
