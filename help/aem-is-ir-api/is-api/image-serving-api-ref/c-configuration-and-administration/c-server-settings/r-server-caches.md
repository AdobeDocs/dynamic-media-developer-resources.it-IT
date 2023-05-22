---
description: Utilizza queste impostazioni server per le cache del server.
solution: Experience Manager
title: Cache server
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 6a8d44d3-ecac-4fe0-9f81-28b1cd55e7e1
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '296'
ht-degree: 0%

---

# Cache server{#server-caches}

Utilizza queste impostazioni server per le cache del server.

## PS::cache.rootPaths - Cartelle dati cache {#section-f0aa808304d74ecdb0c3644f11906c53}

Cartelle principali per [!DNL Platform Server]cache del disco di. Uno o più percorsi di file assoluti o relativi a *[!DNL install_folder]*, separati da punto e virgola (;). I dati per la cache di risposta HTTP vengono distribuiti in modo uniforme in tutte le cartelle specificate. Le cache per le cache ausiliarie (cataloghi di immagini compilati e dati di immagini esterne) si trovano nella cartella principale della cache (la prima cartella dell’elenco).

## PS::cache.maxSize - Response Data Cache Size {#section-ed2e1e7ba4bd4e13b77bb20c4cacddb4}

Dimensione massima della cache di risposta HTTP in byte. Questa impostazione limita la quantità di dati effettivi da memorizzare nella cache; non considera il sovraccarico del file system. (vedere [Cache dei dati di risposta](../../../../is-api/image-serving-api-ref/c-configuration-and-administration/c-data-caches/c-response-data-cache.md#concept-81ea996c242441f2a69f7e9d9b3a29ca).) Se si specificano più cartelle di dati della cache, i dati della cache vengono distribuiti in modo uniforme in tutte le cartelle. Il valore di `cache.maxSize` in [!DNL PlatformServer.conf] è in byte.

## PS::cache.maxEntries - Max voci cache dati risposta {#section-5603e327e90542a5b50aeeb27b080410}

Numero di voci allocate per l’indice della cache di risposta HTTP in memoria.

>[!NOTE]
>
>Su Linux, assicurati che siano allocati sufficienti i-nodi per la partizione della cache per evitare l’esaurimento degli i-nodi.

## IS::TempDirectory - Cartella dei file temporanei del server immagini {#section-42ea1e7a68c444878f7245c5bbcb1672}

Occasionalmente Image Server deve salvare su disco i dati intermedi. Il percorso può essere assoluto o relativo a *[!DNL install_folder]*.

>[!NOTE]
>
>È necessario creare la nuova cartella prima di modificare questa impostazione. Assicurarsi che le autorizzazioni di accesso siano impostate in modo che il server immagini abbia il controllo completo della cartella.

## SV::temp - Cartella dei file temporanei di Server Supervisor {#section-fd2cd5ef7e814a4bb56aaf5525e1a154}

Occasionalmente, il Server Supervisor deve salvare i dati intermedi su disco. Il percorso può essere assoluto o relativo a *[!DNL install_folder]*. Impostazione predefinita: [!DNL  *[!DNL install_folder]*/temp].

>[!NOTE]
>
>È necessario creare la nuova cartella prima di modificare questa impostazione. Assicurarsi che le autorizzazioni di accesso siano impostate in modo che il Supervisore server abbia il controllo completo della cartella.
