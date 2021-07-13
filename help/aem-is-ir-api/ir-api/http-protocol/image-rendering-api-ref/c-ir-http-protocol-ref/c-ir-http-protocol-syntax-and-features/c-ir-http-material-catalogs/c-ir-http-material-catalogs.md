---
description: I cataloghi di materiali offrono diverse funzioni.
solution: Experience Manager
title: Cataloghi dei materiali *
feature: Dynamic Media Classic, SDK/API
role: Developer,User
exl-id: 502f80f5-fdd1-468b-89a9-64cc9128d655
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '302'
ht-degree: 0%

---

# Cataloghi dei materiali *{#material-catalogs}

I cataloghi di materiali offrono diverse funzioni.

* Consentire la definizione permanente dei materiali, comprese tutte le proprietà dei materiali.

   I materiali definiti nel catalogo dei materiali possono essere referenziati utilizzando un semplice ID, anziché un insieme di proprietà del materiale.
* Specifica i valori predefiniti per alcuni attributi di richiesta, ad esempio la qualità JPEG o una dimensione immagine di risposta predefinita.
* Gestisci vignette, profili ICC e modelli di richiesta.

Anche se non sono definiti cataloghi di materiali specifici, tutte le caratteristiche dei cataloghi di materiali sono disponibili tramite il catalogo predefinito ( [!DNL default.ini]).

Anche se i materiali di rendering possono essere specificati esplicitamente nelle richieste utilizzando gli attributi dei materiali, in molti casi è più opportuno nascondere i dettagli dei materiali dal sito web utilizzando cataloghi di materiali. i comandi src= accettano riferimenti al catalogo invece di percorsi di file espliciti. Una voce di catalogo è costituita da ` [ *[!DNL catId]*/] *[!DNL itemId]*`, dove ` *[!DNL catId]*` identifica un catalogo di materiali e ` *[!DNL itemId]*` identifica un record nel catalogo. Se ` *[!DNL catId]*` non è specificato, viene utilizzato il catalogo di sessione (vedi sotto).

Un record di catalogo viene confrontato correttamente se (a) ` *[!DNL catId]*` corrisponde al valore `attribute::RootId` di un catalogo di materiali e (b) ` *[!DNL recId]*` corrisponde al valore catalog::Id nello stesso catalogo. In caso di esito positivo, gli attributi del materiale (incluso `src=`) vengono impostati sui dati del record del catalogo. Se l&#39;MSS include attributi aggiuntivi per questo materiale oltre a src=, sovrascrivono i valori dal record del catalogo.

Se non è possibile associare ` *[!DNL recId]*` a una voce di catalogo, ` *[!DNL catId]*` viene sostituito da `attribute::RootPath` dal catalogo e il percorso risultante viene quindi considerato come un semplice percorso file. Altri attributi predefiniti (ad esempio `attribute::Resolution`) può anche essere ereditato dal catalogo dei materiali.

Le vignette e i profili ICC possono essere riprodotti in cataloghi di materiali simili ai materiali stessi e a determinate proprietà. Inoltre, la mappa di vignetta fornisce anche il contenitore per i modelli.

**Consultate anche**

Riferimento al catalogo dei materiali, [ `src=`](../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-src.md#reference-62c98abad22149d68d405ed6aaff8272), `attribute::RootId`, `attribute::RootPath`, `attribute::VignettePath`
