---
description: Utilizza queste impostazioni del server per le cache del server.
solution: Experience Manager
title: Cache server
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '309'
ht-degree: 0%

---


# Cache del server{#server-caches}

Utilizza queste impostazioni del server per le cache del server.

## PS::cache.rootPaths - Cartelle dati cache {#section-f0aa808304d74ecdb0c3644f11906c53}

Le cartelle principali per la cache del disco del server Platform. Uno o più percorsi di file assoluti o percorsi relativi a *[!DNL install_folder]*, separati da punto e virgola (;). I dati per la cache di risposta HTTP verranno distribuiti in modo uniforme in tutte le cartelle specificate. Le cache per le cache ausiliarie (cataloghi di immagini compilati e dati di immagini esterne) si troveranno nella cartella cache primaria (la prima cartella nell’elenco).

## PS::cache.maxSize - Response Data Cache Size {#section-ed2e1e7ba4bd4e13b77bb20c4cacddb4}

Dimensione massima della cache di risposta HTTP in byte. Questa impostazione limita la quantità di dati effettivi da memorizzare nella cache; non considera il sovraccarico del file system. (Consulta [Cache dei dati di risposta](../../../../is-api/image-serving-api-ref/c-configuration-and-administration/c-data-caches/c-response-data-cache.md#concept-81ea996c242441f2a69f7e9d9b3a29ca).) Se vengono specificate più cartelle di dati della cache, i dati della cache verranno distribuiti in modo uniforme in tutte le cartelle. Il valore di `cache.maxSize` in [!DNL PlatformServer.conf] è espresso in byte.

## PS::cache.maxEntries - Voci massime cache dati di risposta {#section-5603e327e90542a5b50aeeb27b080410}

Il numero di voci allocate per l&#39;indice della cache di risposta HTTP nella memoria.

>[!NOTE]
>
>Su Linux, assicurati che siano allocati sufficienti i-nodi per la partizione di cache per evitare di esaurire i-nodes.

## IS::TempDirectory - Cartella dei file temporanei del server di immagini {#section-42ea1e7a68c444878f7245c5bbcb1672}

Talvolta, il server di immagini deve salvare i dati intermedi sul disco. Il percorso può essere assoluto o relativo a *[!DNL install_folder]*.

>[!NOTE]
>
>È necessario creare la nuova cartella prima di modificare questa impostazione. Assicurati che le autorizzazioni di accesso siano impostate in modo che Image Server abbia il controllo completo della cartella.

## SV::temp - Cartella dei file temporanei del supervisore del server {#section-fd2cd5ef7e814a4bb56aaf5525e1a154}

Talvolta, il Server Supervisore deve salvare i dati intermedi sul disco. Il percorso può essere assoluto o relativo a *[!DNL install_folder]*. Valori predefiniti in [!DNL *[!DNL install_folder]*/temp].

>[!NOTE]
>
>È necessario creare la nuova cartella prima di modificare questa impostazione. Assicurati che le autorizzazioni di accesso siano impostate in modo che il Server Supervisore abbia il controllo completo della cartella.

