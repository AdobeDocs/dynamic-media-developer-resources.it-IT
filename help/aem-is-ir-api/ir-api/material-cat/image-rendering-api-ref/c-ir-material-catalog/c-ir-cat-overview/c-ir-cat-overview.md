---
description: I cataloghi dei materiali forniscono informazioni sulle vignettature, i materiali e i dati di supporto, come i profili ICC, al server.
seo-description: I cataloghi dei materiali forniscono informazioni sulle vignettature, i materiali e i dati di supporto, come i profili ICC, al server.
seo-title: Panoramica del catalogo dei materiali *
solution: Experience Manager
title: Panoramica del catalogo dei materiali *
topic: Scene7 Image Serving - Image Rendering API
uuid: f2128b64-8caf-4a59-b11f-604fe62bae69
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Panoramica del catalogo dei materiali *{#material-catalog-overview}

I cataloghi dei materiali forniscono informazioni sulle vignettature, i materiali e i dati di supporto, come i profili ICC, al server.

Ciascun catalogo di materiali è costituito da un file *di attributi di* catalogo richiesto e da un set di file *di dati di* catalogo opzionali:

* Il file di mappa vignettatura, che riassume vignettature e modelli e i relativi metadati.
* Il file di dati del materiale, che elenca i materiali e specifica i file immagine e i metadati della texture associati.
* Il file delle definizioni delle macro, che fornisce le definizioni per le macro delle richieste.
* Il file della mappa del profilo, che rappresenta i profili colore ICC.

I file di dati del catalogo sono associati ai cataloghi dei materiali in base ai riferimenti ai file presenti nel file di attributi del catalogo. Lo stesso file di dati del catalogo può essere condiviso da più cataloghi di materiali.

I file di attributi del catalogo devono avere un suffisso di [!DNL .ini] file e devono trovarsi nella cartella *del* catalogo di rendering delle immagini ( [!DNL PlatformServer::ir.catalogRootPath]). I file di dati del catalogo possono trovarsi nella stessa cartella o in qualsiasi altra cartella accessibile al server di rendering.

**Aggiornamento dei cataloghi dei materiali**

Il server controlla continuamente la cartella del catalogo e ricarica automaticamente un catalogo di materiali, inclusi i file di dati del catalogo associati, quando rileva che il file di attributi del catalogo principale è stato modificato. Pertanto, per aggiornare i cataloghi dei materiali sul server, sostituite prima tutti i file di dati del catalogo che devono essere modificati, quindi sostituite (o &quot;toccate&quot;) il file degli attributi del catalogo per attivare il ricaricamento del catalogo.

**Catalogo predefinito**

Il catalogo predefinito fornisce valori predefiniti per tutti gli attributi del catalogo per tutti i cataloghi di materiali. Se non è possibile trovare un attributo specifico in un catalogo materiale specifico, il server utilizzerà il valore corrispondente dal catalogo predefinito. Analogamente, il catalogo predefinito può essere utilizzato per fornire i valori predefiniti per record di dati del catalogo specifici (materiali e profili ICC). Se non è possibile trovare un record di dati specifico in un catalogo di materiali specifico, il server tenterà di trovarlo nel catalogo predefinito. Questo consente di compilare i cataloghi dei materiali in modo sparso e semplifica la gestione di attributi e dati globali, come modelli condivisi, macro, font ecc.

Inoltre, il catalogo predefinito fornisce tutti gli attributi e i record di dati (profili ICC) quando nessun catalogo di materiali specifico è coinvolto in un&#39;operazione.

Per il corretto funzionamento del server di rendering, il file degli attributi del catalogo per il catalogo predefinito deve essere denominato [!DNL default.ini], deve sempre esistere nella cartella del catalogo e deve essere compilato con tutti gli attributi richiesti, ad eccezione `attribute::RootId` e dei riferimenti ai vari file di dati del catalogo, tutti facoltativi.

**Consultate anche**

`PlatformServer::ir.catalogRootPath`
