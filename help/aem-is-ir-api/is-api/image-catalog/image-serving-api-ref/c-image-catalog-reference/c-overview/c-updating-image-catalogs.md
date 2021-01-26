---
description: Il server controlla continuamente la cartella del catalogo e ricarica automaticamente un catalogo immagini, inclusi i file di dati del catalogo associati, quando rileva che il file attributo del catalogo principale è stato modificato.
seo-description: Il server controlla continuamente la cartella del catalogo e ricarica automaticamente un catalogo immagini, inclusi i file di dati del catalogo associati, quando rileva che il file attributo del catalogo principale è stato modificato.
seo-title: Aggiornamento dei cataloghi di immagini
solution: Experience Manager
title: Aggiornamento dei cataloghi di immagini
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 7e2557c4-1155-429b-a630-a2aff6725a3b
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '340'
ht-degree: 0%

---


# Aggiornamento dei cataloghi di immagini{#updating-image-catalogs}

Il server controlla continuamente la cartella del catalogo e ricarica automaticamente un catalogo immagini, inclusi i file di dati del catalogo associati, quando rileva che il file attributo del catalogo principale è stato modificato.

Per aggiornare i cataloghi di immagini sul server, sostituite prima tutti i file di dati del catalogo che devono essere modificati, quindi sostituite (o &quot;touch,&quot; per aggiornare la data del file) il file di attributi del catalogo per attivare il ricaricamento del catalogo.

## Aggiornamenti incrementali {#section-2c0f2c1b8480486d86920b5f2cfe72d2}

Il caricamento e l&#39;elaborazione di cataloghi di immagini di grandi dimensioni possono causare un notevole carico sul server e possono avere un impatto negativo sulle operazioni di trasmissione live. Per ridurre al minimo questo impatto, si consiglia di implementare un meccanismo di aggiornamento del catalogo incrementale, che funziona come segue:

Un file di catalogo primario contenente tutte le immagini viene caricato ogni notte durante le ore di traffico ridotte. Se durante il giorno è necessario aggiungere o modificare record nel catalogo immagini, viene creato un altro file di dati immagine che contiene solo i record nuovi o modificati. Questo file è registrato come file di dati immagine secondario in `attribute::CatalogFile`. Il server rileva che il file dell&#39;attributo del catalogo è stato modificato e quindi verifica quali file di dati del catalogo sono stati modificati. Se il file di dati immagine principale non è stato toccato, il server carica o ricarica solo il file di dati incrementale. Poiché in genere questo file è molto più piccolo del file catalogo principale, l&#39;impatto sul server è molto ridotto, rispetto al ricaricamento del catalogo principale.

Gli aggiornamenti incrementali possono ridurre notevolmente l&#39;impatto sul server durante il traffico pesante. Si consiglia di unire regolarmente il file di dati del catalogo incrementale nel file di dati del catalogo principale durante le ore di traffico ridotto per mantenere prestazioni ottimali del server.
