---
title: Panoramica del catalogo dei materiali
description: I cataloghi di materiali forniscono informazioni su vignette, materiali e dati di supporto, come i profili ICC, al server.
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

I cataloghi di materiali forniscono informazioni su vignette, materiali e dati di supporto, come i profili ICC, al server.

Ogni catalogo di materiali è costituito da un *file di attributi di catalogo* e una serie di *file di dati di catalogo*:

* Il file mappa vignetta, che riproduce vignette e modelli e i relativi metadati associati.
* Il file di dati del materiale, che descrive i materiali e specifica i file di immagine della texture e i metadati associati.
* Il file delle definizioni delle macro, che fornisce le definizioni delle macro delle richieste.
* Il file di mappa del profilo, che descrive i profili di colore ICC.

I file di dati del catalogo sono associati ai cataloghi di materiali tramite riferimenti di file nel file di attributi del catalogo. Lo stesso file di dati di catalogo può essere condiviso da più cataloghi di materiali.

I file di attributi del catalogo devono avere un [!DNL `.ini`] suffisso di file e deve trovarsi nel Image Rendering *cartella di catalogo* ( [!DNL PlatformServer::ir.catalogRootPath]). I file di dati del catalogo possono trovarsi nella stessa cartella o in qualsiasi altra cartella accessibile al server di rendering.

**Aggiornamento dei cataloghi di materiali**

Il server controlla continuamente la cartella del catalogo. Ricarica automaticamente un catalogo di materiali, inclusi i file di dati del catalogo associati, quando rileva che il file di attributi del catalogo principale è stato modificato. Pertanto, per aggiornare i cataloghi di materiali sul server, sostituisci prima tutti i file di dati del catalogo che devono essere modificati e poi sostituisci (o &quot;touch&quot;) il file degli attributi del catalogo per attivare il ricaricamento del catalogo.

**Catalogo predefinito**

Il catalogo predefinito fornisce valori predefiniti per tutti gli attributi del catalogo per tutti i cataloghi di materiali. Se non è possibile trovare un attributo specifico in un catalogo di materiali specifico, il server utilizza invece il valore corrispondente del catalogo predefinito. Analogamente, il catalogo predefinito può essere utilizzato per fornire i valori predefiniti per record di dati di catalogo specifici (materiali e profili ICC). Se non è possibile trovare un record di dati specifico in un catalogo di materiali specifico, il server tenta di trovarlo nel catalogo predefinito. Questo consente di popolare i cataloghi di materiali e semplifica la gestione di attributi e dati globali, come modelli condivisi, macro e font.

Inoltre, il catalogo predefinito fornisce tutti gli attributi e i record di dati (profili ICC) quando non è coinvolto in un&#39;operazione alcun catalogo di materiali specifico.

Per il corretto funzionamento del server di rendering, il file degli attributi del catalogo per il catalogo predefinito deve essere denominato [!DNL default.ini]. Deve anche essere sempre presente nella cartella del catalogo e deve essere compilato con tutti gli attributi richiesti, escludendo `attribute::RootId` e i riferimenti ai vari file di dati del catalogo, tutti facoltativi.

<!-- **See also**

`PlatformServer::ir.catalogRootPath` -->
