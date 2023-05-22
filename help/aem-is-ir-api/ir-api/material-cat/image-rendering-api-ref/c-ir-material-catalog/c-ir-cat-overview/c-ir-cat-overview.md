---
title: Panoramica del catalogo dei materiali
description: I cataloghi dei materiali forniscono al server informazioni su vignettature, materiali e dati di supporto, ad esempio profili ICC.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: d26371da-e992-4f63-a5be-190ce60eca2f
source-git-commit: 8454991568374ecd1c4babdd3210250ea7988c4c
workflow-type: tm+mt
source-wordcount: '413'
ht-degree: 0%

---

# Panoramica del catalogo dei materiali{#material-catalog-overview}

I cataloghi dei materiali forniscono al server informazioni su vignettature, materiali e dati di supporto, ad esempio profili ICC.

Ogni catalogo dei materiali è costituito da un *file attributo catalogo* e una serie di opzioni *file di dati di catalogo*:

* Il file di mappa vignettatura, che elenca in dettaglio vignettature e modelli e i metadati associati.
* Il file di dati dei materiali, che descrive i materiali e specifica i file di immagine della trama e i metadati associati.
* Il file delle definizioni delle macro, che fornisce le definizioni per le macro di richiesta.
* Il file di mappa del profilo, che specifica i profili colore ICC.

I file di dati del catalogo sono associati ai cataloghi di materiale tramite riferimenti di file nel file di attributi del catalogo. Lo stesso file di dati di catalogo può essere condiviso da più cataloghi di materiale.

I file degli attributi del catalogo devono avere [!DNL `.ini`] suffisso del file e deve trovarsi in Image Rendering *cartella catalogo* ( [!DNL PlatformServer::ir.catalogRootPath]). I file di dati del catalogo possono trovarsi nella stessa cartella o in qualsiasi altra cartella accessibile al server di rendering.

**Aggiornamento dei cataloghi di materiale**

Il server controlla continuamente la cartella del catalogo. Ricarica automaticamente un catalogo dei materiali, inclusi i file di dati del catalogo associati, quando rileva che il file di attributi del catalogo principale è stato modificato. Pertanto, per aggiornare i cataloghi di materiale sul server, sostituisci prima tutti i file di dati del catalogo che devono essere modificati, quindi sostituisci (o &quot;tocca&quot;) il file degli attributi del catalogo per attivare il ricaricamento del catalogo.

**Catalogo predefinito**

Il catalogo predefinito fornisce i valori predefiniti per tutti gli attributi del catalogo per tutti i cataloghi di materiale. Se non è possibile trovare un attributo specifico in un catalogo dei materiali specifico, il server utilizza il valore corrispondente del catalogo predefinito. Analogamente, il catalogo predefinito può essere utilizzato per fornire valori predefiniti per record di dati di catalogo specifici (materiali e profili ICC). Se non è possibile trovare un record di dati specifico in un catalogo di materiali specifico, il server tenta di trovarlo nel catalogo predefinito. Ciò consente di compilare i cataloghi di materiale in modo limitato e semplifica la gestione di attributi e dati globali, ad esempio modelli condivisi, macro e font.

Inoltre, il catalogo predefinito fornisce tutti gli attributi e i record di dati (profili ICC) quando non è coinvolto alcun catalogo di materiale specifico in un&#39;operazione.

Per il corretto funzionamento del server di rendering, è necessario denominare il file degli attributi del catalogo predefinito [!DNL default.ini]. Deve inoltre esistere sempre nella cartella del catalogo e deve essere compilato completamente con tutti gli attributi richiesti, esclusi `attribute::RootId` e i riferimenti ai vari file di dati di catalogo, tutti facoltativi.

<!-- **See also**

`PlatformServer::ir.catalogRootPath` -->
