---
description: I cataloghi di materiali forniscono informazioni su vignette, materiali e dati di supporto, come i profili ICC, al server.
solution: Experience Manager
title: Panoramica del catalogo dei materiali *
feature: Dynamic Media Classic, SDK/API
role: Developer,User
exl-id: d26371da-e992-4f63-a5be-190ce60eca2f
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '423'
ht-degree: 0%

---

# Panoramica del catalogo dei materiali *{#material-catalog-overview}

I cataloghi di materiali forniscono informazioni su vignette, materiali e dati di supporto, come i profili ICC, al server.

Ciascun catalogo di materiali è costituito da un file di attributi di catalogo *richiesto* e da un set di file di dati di catalogo *facoltativi*:

* Il file mappa vignetta, che riproduce vignette e modelli e i relativi metadati associati.
* Il file di dati del materiale, che descrive i materiali e specifica i file di immagine della texture e i metadati associati.
* Il file delle definizioni delle macro, che fornisce le definizioni delle macro delle richieste.
* Il file di mappa del profilo, che descrive i profili di colore ICC.

I file di dati del catalogo sono associati ai cataloghi di materiali tramite riferimenti di file nel file di attributi del catalogo. Lo stesso file di dati di catalogo può essere condiviso da più cataloghi di materiali.

I file di attributi del catalogo devono avere un suffisso di file [!DNL .ini] e devono trovarsi nella cartella Image Rendering *catalogo* ( [!DNL PlatformServer::ir.catalogRootPath]). I file di dati del catalogo possono trovarsi nella stessa cartella o in qualsiasi altra cartella accessibile al server di rendering.

**Aggiornamento dei cataloghi di materiali**

Il server controlla continuamente la cartella del catalogo e ricarica automaticamente un catalogo di materiali, inclusi i file di dati del catalogo associati, quando rileva che il file di attributi del catalogo principale è stato modificato. Pertanto, per aggiornare i cataloghi di materiali sul server, sostituisci prima tutti i file di dati del catalogo che devono essere modificati e poi sostituisci (o &quot;touch&quot;) il file degli attributi del catalogo per attivare il ricaricamento del catalogo.

**Catalogo predefinito**

Il catalogo predefinito fornisce valori predefiniti per tutti gli attributi del catalogo per tutti i cataloghi di materiali. Se non è possibile trovare un attributo specifico in un catalogo di materiali specifico, il server utilizzerà invece il valore corrispondente del catalogo predefinito. Analogamente, il catalogo predefinito può essere utilizzato per fornire i valori predefiniti per record di dati di catalogo specifici (materiali e profili ICC). Se non è possibile trovare un record di dati specifico in un catalogo di materiali specifico, il server tenterà di trovarlo nel catalogo predefinito. Questo consente di popolare i cataloghi di materiali e semplifica la gestione di attributi e dati globali, come modelli condivisi, macro, font, ecc.

Inoltre, il catalogo predefinito fornisce tutti gli attributi e i record di dati (profili ICC) quando non è coinvolto in un&#39;operazione alcun catalogo di materiali specifico.

Per il corretto funzionamento del server di rendering, il file degli attributi del catalogo per il catalogo predefinito deve essere denominato [!DNL default.ini], deve sempre esistere nella cartella del catalogo e deve essere compilato con tutti gli attributi richiesti, esclusi `attribute::RootId` e i riferimenti ai vari file di dati del catalogo, tutti facoltativi.

**Consultate anche**

`PlatformServer::ir.catalogRootPath`
