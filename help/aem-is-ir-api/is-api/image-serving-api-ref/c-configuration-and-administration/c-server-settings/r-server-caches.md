---
description: Utilizzate queste impostazioni del server per le cache del server.
seo-description: Utilizzate queste impostazioni del server per le cache del server.
seo-title: Cache server
solution: Experience Manager
title: Cache server
topic: Scene7 Image Serving - Image Rendering API
uuid: 73745363-2011-453f-b7a0-96de4b44186d
translation-type: tm+mt
source-git-commit: e8e5b07329bde3e23ee095d5022da62d67e9478c
workflow-type: tm+mt
source-wordcount: '309'
ht-degree: 0%

---


# Cache server{#server-caches}

Utilizzate queste impostazioni del server per le cache del server.

## PS::cache.rootPaths - Cache Data Folders {#section-f0aa808304d74ecdb0c3644f11906c53}

Le cartelle principali per la cache del disco di Platform Server. Uno o più percorsi di file o percorsi assoluti relativi a *[!DNL install_folder]*, separati da punto e virgola (;). I dati per la cache delle risposte HTTP verranno distribuiti in modo uniforme in tutte le cartelle specificate. Le cache per le cache ausiliarie (cataloghi di immagini compilati e dati di immagini esterne) si troveranno nella cartella cache primaria (la prima cartella dell&#39;elenco).

## PS::cache.maxSize - Dimensione cache dati di risposta {#section-ed2e1e7ba4bd4e13b77bb20c4cacddb4}

La dimensione massima della cache delle risposte HTTP, in byte. Questa impostazione limita la quantità di dati effettivi da memorizzare nella cache; non considera il sovraccarico del file system. (Vedere Cache [dati](../../../../is-api/image-serving-api-ref/c-configuration-and-administration/c-data-caches/c-response-data-cache.md#concept-81ea996c242441f2a69f7e9d9b3a29ca)di risposta.) Se vengono specificate più cartelle di dati della cache, i dati della cache verranno distribuiti in modo uniforme su tutte le cartelle. Il valore di `cache.maxSize` in [!DNL PlatformServer.conf] byte.

## PS::cache.maxEntries - Cache dati di risposta Numero massimo di voci {#section-5603e327e90542a5b50aeeb27b080410}

Il numero di voci allocate per l&#39;indice della cache delle risposte HTTP in memoria.

>[!NOTE]
>
>In Linux, assicurarsi che i nodi i siano allocati sufficienti per la partizione della cache per evitare di esaurire i nodi.

## IS::TempDirectory - Cartella dei file temporanei del server di immagini {#section-42ea1e7a68c444878f7245c5bbcb1672}

Il server immagini a volte deve salvare i dati intermedi sul disco. Il percorso può essere assoluto o relativo a *[!DNL install_folder]*.

>[!NOTE]
>
>Prima di modificare questa impostazione è necessario creare la nuova cartella. Accertatevi che le autorizzazioni di accesso siano impostate in modo che il server immagini disponga del controllo completo della cartella.

## SV::temp - Cartella dei file temporanei del supervisore del server {#section-fd2cd5ef7e814a4bb56aaf5525e1a154}

Il supervisore del server a volte deve salvare i dati intermedi sul disco. Il percorso può essere assoluto o relativo a *[!DNL install_folder]*. Il valore predefinito è [!DNL *[!DNL install_folder]*/temp].

>[!NOTE]
>
>Prima di modificare questa impostazione è necessario creare la nuova cartella. Accertatevi che le autorizzazioni di accesso siano impostate in modo che il Garante server abbia il controllo completo della cartella.

