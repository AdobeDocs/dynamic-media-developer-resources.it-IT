---
description: Il server controlla continuamente la cartella del catalogo e ricarica automaticamente un catalogo immagini, inclusi i file di dati del catalogo associati, quando rileva che il file di attributi del catalogo principale è stato modificato.
solution: Experience Manager
title: Aggiornamento dei cataloghi di immagini
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: b520b4f3-6717-4768-99e2-78a76d1ede24
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '306'
ht-degree: 0%

---

# Aggiornamento dei cataloghi di immagini{#updating-image-catalogs}

Il server controlla continuamente la cartella del catalogo e ricarica automaticamente un catalogo immagini, inclusi i file di dati del catalogo associati, quando rileva che il file di attributi del catalogo principale è stato modificato.

Per aggiornare i cataloghi di immagini sul server, sostituisci innanzitutto tutti i file di dati del catalogo che devono essere modificati, quindi sostituisci (o &quot;tocca&quot; per aggiornare la data del file) il file degli attributi del catalogo per attivare il ricaricamento del catalogo.

## Aggiornamenti incrementali {#section-2c0f2c1b8480486d86920b5f2cfe72d2}

Il caricamento e l’elaborazione di cataloghi di immagini di grandi dimensioni possono caricare notevolmente il server e avere un impatto negativo sulle operazioni live serving. Per ridurre al minimo questo impatto, si consiglia di implementare un meccanismo di aggiornamento incrementale del catalogo, che funzioni come segue:

Un file di catalogo principale contenente tutte le immagini viene caricato di notte nelle ore con traffico ridotto. Se durante il giorno è necessario aggiungere o modificare record nel catalogo immagini, viene creato un altro file di dati immagine contenente solo i record nuovi o modificati. Questo file è registrato come file di dati immagine secondario in `attribute::CatalogFile`. Il server rileva che il file degli attributi del catalogo è stato modificato e quindi controlla quali file di dati del catalogo sono stati modificati. Se il file di dati dell&#39;immagine principale non è stato toccato, il server carica o ricarica solo il file di dati incrementale. Poiché questo file è in genere molto più piccolo del file di catalogo principale, l’impatto sul server è molto ridotto rispetto al ricaricamento del catalogo principale.

Gli aggiornamenti incrementali possono ridurre in modo significativo l’impatto sul server durante il traffico pesante. Si consiglia di unire regolarmente il file di dati di catalogo incrementale nel file di dati di catalogo principale durante le ore con traffico ridotto, per mantenere prestazioni ottimali del server.
